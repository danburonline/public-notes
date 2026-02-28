## AGENTS.md

**Generated:** 2026-01-05
**Commit:** 7276287
**Branch:** main

### OVERVIEW

Personal Obsidian knowledge base (Zettelkasten-style). Several markdown notes covering neuroscience, consciousness, ML, software engineering, and philosophy.

**Primary Goal**: Maximise interdisciplinary thinking through densely connected notes that bridge multiple competencies. The vault should function as a synthesis engine for [consciousness engineering](001_private/_%20general/Consciousness%20Engineering.md)—connecting quantum cosmology, computational [phenomenology](003_education/kings-college/03%20Mental%20Health%20in%20the%20Community/Phenomenology.md), [biomimetic neuromorphics](002_profession/eightsix-science/Biomimetic%20neuromorphics.md), mathematical physics, AI, applied neuroscience, and theoretical neurosurgery into a unified framework.

### STRUCTURE

```
Notes/
├── _inbox/           # Staging: attachments, prompts, sketches (gitignored except attachments)
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
| Store image/attachment | `_inbox/attachments/` | Only folder not gitignored in inbox |
| AI prompt logs | `_inbox/prompts/` | Auto-generated filenames with timestamps |

### CONVENTIONS

#### Note Structure (MANDATORY)

```markdown
#category/subcategory

![optional-image](relative/path/to/image.png)

Brief definition or explanation in bold for key terms.

## Sections as needed
- Content
```

#### Tagging System

Three-tier hierarchy at **line 1** of every note:

| Tier | Purpose | Examples |
|------|---------|----------|
| `#lead/` | Unique positioning / frontier work | `consciousnessengineering` |
| `#core/` | Main competencies | `quantumcosmology`, `syntheticphenomenology`, `biomimeticneuromorphics`, `computationalmathematics`, `theoreticalneurosurgery`, `appliedneuroscience`, `artificialintelligence`, `softwaredevelopment`, `interactiondesign` |
| `#fundamental/` | Foundational skills | `logic`, `communication`, `creativity` |

Multiple tags allowed: `#core/artificialintelligence #core/computationalmathematics`

#### Linking

- **Internal links**: Standard markdown `[Note Title](relative/path/to/Note.md)`
- **Images**: Standard markdown `![alt text](relative/path/to/image.png)`
- Images stored in `_inbox/attachments/`

#### Naming

- **Notes**: Title case with spaces (e.g., `[Bayes' theorem].md`)
- **Folders**: Descriptive, spaces allowed
- **"_ general knowledge"**: Prefix underscore for miscellaneous concepts within a category

#### Spelling

- **British English**: Use British spelling throughout (e.g., `behaviour`, `organisation`, `colour`, `centre`)
- **-ise over -ize**: Prefer `organise`, `realise`, `specialise` (not American `-ize`)
- **Scientific terms**: Follow standard scientific nomenclature regardless of regional spelling

### ANTI-PATTERNS

- **DO NOT** create notes without tags at line 1
- **DO NOT** revert to Obsidian-only embeds `![[image.png]]`
- **DO NOT** store attachments outside `_inbox/attachments/`
- **DO NOT** commit `_inbox/` content (except attachments) - gitignored
- **DO NOT** use kebab-case or snake_case for note names

### UNIQUE STYLES

- **Source-based organisation**: Notes grouped by where learned (book, video, paper, podcast, social media)
- **Institution nesting**: Education notes nested by school then module number
- **Register/Sketches**: `_inbox/register/` and `_inbox/sketches/` mirror main folder structure for drafts

### COMMANDS

```bash
# Tooling: opencode + Oh My OpenCode (omo) in Obsidian's integrated terminal
# No build/test commands - knowledge base, not code project

# Obsidian CLI — requires Obsidian to be open
obsidian read file="Note Name"                          # Read a note by wikilink name
obsidian create name="New Note" content="..." silent    # Create note (silent = don't open it)
obsidian append file="Note Name" content="New content"  # Append to existing note
obsidian search query="term" limit=10                   # Full-text search across vault
obsidian tags sort=count counts                          # List all tags with counts
obsidian backlinks file="Note Name"                     # Show all notes linking to a note
obsidian property:set name="status" value="done" file="Note Name"  # Set a property
obsidian daily:append content="- New entry"             # Append to today's daily note
```

### SKILLS

Available opencode skills for this workspace:

| Skill | Use Case |
|-------|----------|
| `obsidian-markdown` | Wikilinks, embeds, callouts, frontmatter, tags — enforces vault conventions |
| `obsidian-cli` | Read, create, append, search, and manage notes live via Obsidian CLI (Obsidian must be open) |
| `obsidian-bases` | Create and edit `.base` database views with filters, formulas, table/cards/list layouts |
| `git-master` | Commits, history search, blame |

### AGENT WORKFLOW

When working with notes:

- **Embedded images**: If a note contains `![alt text](relative/path/to/image.png)` embeds, locate the image in `_inbox/attachments/` and visually examine it using `look_at` to better understand the note's content before refining or expanding
- **Live vault operations**: Use the `obsidian-cli` skill when Obsidian is open to read, create, or search notes through the live vault rather than raw file tools — CLI reflects Obsidian's current state (plugins, linter, resolved links)
- **Creating notes**: Prefer `obsidian create` over writing files directly when Obsidian is running — it triggers linter and plugin hooks automatically
- **Searching content**: Use `obsidian search` for full-text vault search; use `mcp_grep` for pattern/regex searches across raw files
- **Database views**: Use the `obsidian-bases` skill to create `.base` files for structured views (e.g., tables of notes by tag, folder, or property)

### NOTES

- `.agents/` contains agent skills (`obsidian-markdown`, `obsidian-cli`, `obsidian-bases`)
- `.obsidian/` contains Obsidian app config (gitignored)
- `.smart-env/` is plugin data (gitignored)
- `piecesdb.json` is external tool data (gitignored)
- **Obsidian CLI requires Obsidian to be running** — CLI commands will fail if the app is closed
