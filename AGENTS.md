## AGENTS.md

**Generated:** 2026-01-05
**Commit:** 7276287
**Branch:** main

### OVERVIEW

Personal Obsidian knowledge base (Zettelkasten-style). Several markdown notes covering neuroscience, consciousness, ML, software engineering, and philosophy.

**Primary Goal**: Maximise interdisciplinary thinking through densely connected notes that bridge multiple competencies. The vault should function as a synthesis engine for consciousness engineering—connecting computational neurophenomenology, mathematical physics, AI, applied neuroscience, and theoretical neurosurgery into a unified framework.

### STRUCTURE

```
Notes/
├── 000_inbox/        # Staging: attachments, prompts, sketches (gitignored except attachments)
├── 001_private/      # Personal learning: books, videos, papers, articles, social, etc. media
├── 002_profession/   # Work: blue brain project, eightsix science, finalspark, idun, etc.
├── 003_education/    # Formal: kings college, epfl, buckingham, etc.
├── 004_subsidiary/   # Side: carboncopies, courses (datacamp, three.js)
└── 005_public/       # Empty for now
```

**Numbered prefixes** = priority/visibility. Lower = more active.

### WHERE TO LOOK

| Task | Location | Notes |
|------|----------|-------|
| Add new concept from learning | `001_private/{source_type}/{source_name}/` | e.g., `001_private/books/The Feeling of Life Itself/` |
| Add work-related note | `002_profession/{company}/` | Match existing company folders |
| Add course material | `003_education/{institution}/{module}/` | Match existing module naming |
| Store image/attachment | `000_inbox/attachments/` | Only folder not gitignored in inbox |
| AI prompt logs | `000_inbox/prompts/` | Auto-generated filenames with timestamps |

### CONVENTIONS

#### Note Structure (MANDATORY)

```markdown
#category/subcategory

![[optional-image.png]]

Brief definition or explanation in bold for key terms.

## Sections as needed
- Content
```

#### Tagging System

Three-tier hierarchy at **line 1** of every note:

| Tier | Purpose | Examples |
|------|---------|----------|
| `#lead/` | Unique positioning / frontier work | `consciousnessengineering` |
| `#core/` | Main competencies | `computationalneurophenomenology`, `mathematicalphysics`, `theoreticalneurosurgery`, `appliedneuroscience`, `artificialintelligence`, `softwaredevelopment`, `interactiondesign` |
| `#fundamental/` | Foundational skills | `logic`, `communication`, `creativity` |

Multiple tags allowed: `#core/artificialintelligence #core/mathematicalphysics`

#### Linking

- **Internal links**: Wikilinks `[[Note Title]]`
- **Images**: Obsidian embed `![[image.png]]`
- Images stored in `000_inbox/attachments/`

#### Naming

- **Notes**: Title case with spaces (e.g., `Bayes' theorem.md`)
- **Folders**: Descriptive, spaces allowed
- **"_ general knowledge"**: Prefix underscore for miscellaneous concepts within a category

#### Spelling

- **British English**: Use British spelling throughout (e.g., `behaviour`, `organisation`, `colour`, `centre`)
- **-ise over -ize**: Prefer `organise`, `realise`, `specialise` (not American `-ize`)
- **Scientific terms**: Follow standard scientific nomenclature regardless of regional spelling

### ANTI-PATTERNS

- **DO NOT** create notes without tags at line 1
- **DO NOT** use markdown image syntax `![](path)` - use Obsidian `![[]]`
- **DO NOT** store attachments outside `000_inbox/attachments/`
- **DO NOT** commit `000_inbox/` content (except attachments) - gitignored
- **DO NOT** use kebab-case or snake_case for note names

### UNIQUE STYLES

- **Source-based organisation**: Notes grouped by where learned (book, video, paper, podcast, social media)
- **Institution nesting**: Education notes nested by school then module number
- **Register/Sketches**: `000_inbox/register/` and `000_inbox/sketches/` mirror main folder structure for drafts

### COMMANDS

```bash
# Tooling: opencode + Oh My OpenCode (omo) in Obsidian's integrated terminal
# No build/test commands - knowledge base, not code project
```

### SKILLS

Available opencode skills for this workspace:

| Skill | Use Case |
|-------|----------|
| `obsidian-markdown` | Wikilinks, embeds, callouts, frontmatter, tags — enforces vault conventions |
| `git-master` | Commits, history search, blame |

### NOTES

- `.obsidian/` contains Obsidian app config (gitignored)
- `.smart-env/` is plugin data (gitignored)
- `piecesdb.json` is external tool data (gitignored)
