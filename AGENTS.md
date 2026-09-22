## AGENTS.md

**Updated:** 2026-09-22
**Branch:** main

### OVERVIEW

Public, personal Obsidian knowledge base (Zettelkasten-style). Several markdown notes covering neuroscience, consciousness, ML, software engineering, and philosophy.

**Primary Goal**: Maximise interdisciplinary thinking through densely connected notes that bridge multiple competencies. The vault should function as a synthesis engine across all skill categories: lead, core, and fundamental. The lead tier forms a deliberate continuum. Computational philosophy makes abstract thought and pure knowledge more precise. Venture engineering turns those foundations into research, technologies, and interventions through venture building. Experimental medicine works at the most hands-on end, experimenting with living systems and humans to understand and repair biological faults. These leads draw on core disciplines including evolutionary panmemetics, [biomimetic neuromorphics](002_profession/eightsix/biomimetic_neuromorphics.md), mathematical physics, theoretical neurosurgery, applied neuroscience, artificial intelligence, software development, and interaction design. [Consciousness engineering](001_private/_general/consciousness_engineering.md) is one integrative direction emerging from their combination.

### STRUCTURE

```txt
Notes/
├── _inbox/           # Staging: prompts, sketches (fully gitignored)
├── 001_private/      # Personal learning taxonomy: books, videos, papers, articles, social, etc.
├── 002_profession/   # Work: blue brain project, eightsix science, finalspark, idun, etc.
├── 003_education/    # Formal: kings college, epfl, buckingham, etc.
├── 004_subsidiary/   # Side: carboncopies, courses (datacamp, three.js), Synconetics
└── 005_public/       # Public-facing notes and site assets (Obsidian Publish)
```

**Numbered prefixes** = priority/visibility. Lower = more active.

**Privacy boundary:** `001_private/` is a personal organisational label, not a confidentiality boundary. Its tracked content belongs to the public parent Notes repository. Daniel's private meta-level planning, prompts, sketches, and provisional information belong in the gitignored `_inbox/`; credentials and organisation records belong in their own controlled systems, not this vault.

**Source boundary:** Track public-source learning and publishable personal synthesis only. Do not copy internal records, unpublished organisation results, private correspondence or private repository locations into notes, attachments, metadata or commit messages.

### WHERE TO LOOK

| Task                          | Location                                   | Notes                                                 |
| ----------------------------- | ------------------------------------------ | ----------------------------------------------------- |
| Add new concept from learning | `001_private/{source_type}/{source_name}/` | e.g., `001_private/books/the_feeling_of_life_itself/` |
| Add professional learning note | `002_profession/{company}/`              | Public sources and publishable synthesis only          |
| Public-facing note / site asset | `005_public/`                            | Publishable material and diagrams used by the README  |
| Add course material           | `003_education/{institution}/{module}/`    | Match existing module naming                          |
| Add Buckingham material       | `003_education/buckingham/`                | Flat exception: notes at root, files in `_attachments/` |
| Add EPFL material             | `003_education/epfl/`                      | Notes at root; images in `_attachments/`; slides remain separately nested |
| Store image/attachment        | `{note_dir}/_attachments/`                 | Keep each attachment near the note that references it |
| AI prompt logs                | `_inbox/prompts/`                          | Auto-generated filenames with timestamps              |

**Convention scope:** These conventions apply only to files owned by this public repository. Separately controlled repositories follow their own instructions and must not inherit this vault's personal taxonomy.

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

| Tier            | Purpose                            | Examples                                                                                                                                                                                                                    |
| --------------- | ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `#lead/`        | Unique positioning / frontier work | `computationalphilosophy`, `ventureengineering`, `experimentalmedicine`                                                                                                                                                           |
| `#core/`        | Main competencies                  | `evolutionarypanmemetics`, `biomimeticneuromorphics`, `mathematicalphysics`, `theoreticalneurosurgery`, `appliedneuroscience`, `artificialintelligence`, `softwaredevelopment`, `interactiondesign` |
| `#fundamental/` | Foundational skills                | `communication`, `creativity`, `logic`                                                                                                                                                                                      |

Multiple tags allowed: `#core/artificialintelligence #core/mathematicalphysics`

Tags are not mutually exclusive. Add each category that is substantively developed in a note, but do not tag passing mentions, examples, or links.

#### Linking

- **Internal links**: Standard markdown `[Note Title](relative/path/to/note.md)`
- **Images**: Standard markdown `![alt text](relative/path/to/image.png)`
- Images stored in the nearest local `_attachments/` folder relative to each note

#### Naming

- **Notes**: Lowercase with underscores (e.g., `bayes_theorem.md`)
- **Folders**: Lowercase with underscores (e.g., `the_feeling_of_life_itself/`). Existing hyphens are preserved (e.g., `taxonomy_and_metaphysics_of_mind-uploading/`)
- **`_general`**: Prefix underscore for miscellaneous concepts within a category

#### Spelling

- **British English**: Use British spelling throughout (e.g., `behaviour`, `organisation`, `colour`, `centre`)
- **-ise over -ize**: Prefer `organise`, `realise`, `specialise` (not American `-ize`)
- **Scientific terms**: Follow standard scientific nomenclature regardless of regional spelling

### ANTI-PATTERNS

- **DO NOT** create notes without tags at line 1
- **DO NOT** revert to Obsidian-only embeds `![[image.png]]`
- **DO NOT** store active note attachments in `_inbox/` (use local `_attachments/` folders)
- **DO NOT** commit or publish `_inbox/` content - it is the gitignored private meta-level planning and staging layer
- **DO NOT** use Title Case, spaces, or special characters (`& , . ( )`) in file or folder names
- **DO NOT** convert existing hyphens to underscores -- both are allowed
- **DO NOT** link public notes to private repositories or restricted records. Keep separately controlled knowledge self-contained.
- **DO NOT** include private or independently governed local checkouts in Obsidian Publish. They require their own publication approval.

### UNIQUE STYLES

- **Source-based organisation**: Notes grouped by where learned (book, video, paper, podcast, social media)
- **Institution nesting**: Education notes are normally nested by school then module number; Buckingham and EPFL notes are intentionally flat within their institution folders
- **Register/Sketches**: `_inbox/register/` and `_inbox/sketches/` mirror main folder structure for drafts

### COMMANDS

```bash
# Knowledge base, not a code project. No build or test commands.

# Obsidian CLI -- requires Obsidian to be open
obsidian read file="note_name"                          # Read a note by wikilink name
obsidian create name="new_note" content="..." silent    # Create note (silent = don't open it)
obsidian append file="note_name" content="New content"  # Append to existing note
obsidian search query="term" limit=10                   # Full-text search across vault
obsidian tags sort=count counts                          # List all tags with counts
obsidian backlinks file="note_name"                     # Show all notes linking to a note
obsidian property:set name="status" value="done" file="note_name"  # Set a property
obsidian daily:append content="- New entry"             # Append to today's daily note
```

### SKILLS

Available skills for this vault:

| Skill               | Use Case                                                                                     |
| ------------------- | -------------------------------------------------------------------------------------------- |
| `obsidian-markdown` | Wikilinks, embeds, callouts, frontmatter, tags -- enforces vault conventions                  |
| `obsidian-cli`      | Read, create, append, search, and manage notes live via Obsidian CLI (Obsidian must be open) |
| `obsidian-bases`    | Create and edit `.base` database views with filters, formulas, table/cards/list layouts      |
| `json-canvas`       | Create and edit `.canvas` files with nodes, edges, groups -- mind maps, flowcharts, visual canvases |
| `defuddle`          | Extract clean markdown from web pages -- removes clutter, saves tokens over WebFetch          |
| `perplexity`        | AI-powered research via Perplexity API -- literature discovery, paper summaries, fact-checking with citations |

### AGENT WORKFLOW

When working with notes:

- **README discovery**: When traversing into any folder, check for `README.md` and read it -- subfolders and separately governed local checkouts often contain their own context, conventions, and instructions
- **Embedded images**: If a note contains `![alt text](relative/path/to/image.png)` embeds, locate the image via the note's nearest `_attachments/` folder (or other relative image path) and visually examine it using `look_at` to better understand the note's content before refining or expanding
- **Live vault operations**: Use the `obsidian-cli` skill when Obsidian is open to read, create, or search notes through the live vault rather than raw file tools -- CLI reflects Obsidian's current state (plugins, linter, resolved links)
- **Creating notes**: Prefer `obsidian create` over writing files directly when Obsidian is running -- it triggers linter and plugin hooks automatically
- **Searching content**: Use `obsidian search` for full-text vault search; use `rg` for pattern/regex searches across raw files
- **Graph scope**: The parent vault remains Obsidian-first, using links, tags, backlinks and search. Do not add a parent-wide Nanograph index or treat another workspace's graph as authoritative here. Separately governed repositories own their records and any future graph; this vault is not their index.
- **TODO tracking**: Create `TODO.md` in the vault root when actionable tasks need tracking; remove the file when no tasks remain
- **Database views**: Use the `obsidian-bases` skill to create `.base` files for structured views (e.g., tables of notes by tag, folder, or property)
- **Publishing boundary**: Before publishing from Obsidian, verify that `_inbox/` and every private or independently governed local checkout are excluded from the site's publish selection. Git ignores alone do not enforce publication exclusions.

### NOTES

- `.agents/` contains agent skills (`obsidian-markdown`, `obsidian-cli`, `obsidian-bases`, `json-canvas`, `defuddle`, `perplexity`)
- `.obsidian/` contains Obsidian app config (gitignored)
- `.smart-env/` is plugin data (gitignored)
- `piecesdb.json` is external tool data (gitignored)
- **Obsidian CLI requires Obsidian to be running** -- CLI commands will fail if the app is closed
- **`_inbox/`** is Daniel's private meta-level planning, prompting, sketch, and provisional-information layer. It is ignored by Git and excluded from Obsidian Publish, while remaining available through the private Obsidian vault and its sync layer.
- **Obsidian Publish** covers curated material from this public repository only. `_inbox/` and private or independently governed local checkouts must remain excluded.
