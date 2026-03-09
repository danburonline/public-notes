---
name: perplexity
description: AI-powered research assistant using Perplexity API directly. Use for literature discovery, paper summaries, research synthesis, and answering scientific questions with web-grounded citations.
---

# Perplexity Research Assistant (Direct API)

## Overview

This skill provides direct Perplexity API access via HTTP calls. No MCP server required — uses `curl` to call Perplexity's chat completions API directly.

## Prerequisites

- `PERPLEXITY_API_KEY` environment variable must be set in shell
- `curl` and `jq` must be available

## API Endpoint

```
POST https://api.perplexity.ai/chat/completions
```

## Available Models

| Model | Best For | Speed |
|-------|----------|-------|
| `sonar` | Quick Q&A, summaries | Fast |
| `sonar-pro` | Detailed answers with citations | Medium |
| `sonar-reasoning-pro` | Step-by-step analysis | Medium |
| `sonar-deep-research` | Literature reviews, comprehensive overviews | Slow (30s+) |

## Required Workflow

**Follow these steps in order. Do not skip steps.**

### Step 1: Identify Query Type

Match your research need to the appropriate model:

| Research Need | Model | Example |
|---------------|-------|---------|
| Quick fact check | `sonar` | "What is the main claim of IIT 4.0?" |
| Paper summary | `sonar-pro` | "Summarise Tononi 2024 on integrated information" |
| Compare theories | `sonar-reasoning-pro` | "Compare IIT vs Global Workspace Theory" |
| Literature review | `sonar-deep-research` | "Review of bioelectric morphogenesis 2020-2025" |

### Step 2: Execute Query

Use the `perplexity` bash function defined below. Call it via the `bash` tool:

```bash
# Quick query
perplexity "Your question here"

# With specific model
perplexity "Your question" sonar-deep-research

# With recency filter (last month)
perplexity "Latest papers on consciousness" sonar-pro month
```

### Step 3: Parse Response

The function returns JSON. Extract:
- `choices[0].message.content` — the answer text
- `citations` — list of source URLs (if present)

### Step 4: Integrate with Knowledge Graph

After Perplexity research:
1. Identify relevant papers not yet in collection
2. Add new papers to `_graph/seed.jsonl` with Paper nodes
3. Run `nanograph load _graph/readings.nano --data _graph/seed.jsonl --mode merge`

## Bash Function

Add this to your execution context. The function is called via the `bash` tool:

```bash
perplexity() {
  local query="$1"
  local model="${2:-sonar-pro}"
  local recency="${3:-}"
  
  local search_options=""
  if [ -n "$recency" ]; then
    search_options=", \"search_recency_filter\": \"$recency\""
  fi
  
  curl -s "https://api.perplexity.ai/chat/completions" \
    -H "Authorization: Bearer $PERPLEXITY_API_KEY" \
    -H "Content-Type: application/json" \
    -d "{
      \"model\": \"$model\",
      \"messages\": [{\"role\": \"user\", \"content\": \"$query\"}]$search_options
    }" | jq -r '.choices[0].message.content'
}
```

## Practical Workflows

### Literature Discovery
```bash
# Broad overview
perplexity "Comprehensive review of bioelectric morphogenesis research 2020-2025" sonar-deep-research

# Extract papers from response, then find DOIs
perplexity "Find DOI for Tononi integrated information theory 2024" sonar
```

### Author Research Programme
```bash
perplexity "Michael Levin's research programme on collective intelligence and morphogenesis" sonar-deep-research
```

### Concept Clarification
```bash
perplexity "What is the difference between integrated information and causal emergence?" sonar-reasoning-pro
```

### Quick Fact Check
```bash
perplexity "What journal published Tononi's IIT 4.0 paper?" sonar
```

## Full Response with Citations

To get citations, modify the jq filter:

```bash
# Get full JSON response
curl -s "https://api.perplexity.ai/chat/completions" \
  -H "Authorization: Bearer $PERPLEXITY_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model": "sonar-pro", "messages": [{"role": "user", "content": "Your question"}]}' \
  | jq '{content: .choices[0].message.content, citations: .citations}'
```

## Tips for Maximum Productivity

- **Use sonar-deep-research sparingly** — it's slow and expensive
- **Batch simple queries** — run multiple `sonar` calls in parallel
- **Extract citations** — always check the sources
- **Cross-reference with knowledge graph** — avoid duplicating what you already have

## Troubleshooting

- **401 Unauthorized**: Check `PERPLEXITY_API_KEY` is set: `echo $PERPLEXITY_API_KEY`
- **Empty response**: Model may be unavailable — try `sonar` or `sonar-pro`
- **Timeout**: Deep research can take 60s+ — wait longer
- **Rate limits**: Space out rapid queries

## Integration with Nanograph

Perplexity excels at discovery and synthesis. Nanograph excels at structured storage and querying. Use them together:

1. **Perplexity → Nanograph**: Discover papers → add to graph
2. **Nanograph → Perplexity**: Query graph for gaps → research to fill them
3. **Cross-validation**: Compare Perplexity citations against graph relations
