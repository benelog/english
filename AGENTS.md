# AGENTS.md

Rules to follow when adding pages to this repository (Benelog English, an English study notebook built with MkDocs Material).

## Directory layout

Place new pages in one of the following directories based on topic.

- `docs/situtaions/` — Expressions used in specific situations (restaurant, airplane, shopping, etc.). The typo in the directory name is intentional; keep it as-is.
- `docs/grammar/` — Grammar topics (modal verbs, prepositions, voice, etc.)
- `docs/expressions/` — Topical expression collections (emotions, food, greetings, etc.)
- `docs/reading/` — Reading material notes (article summaries, etc.)
- `docs/lyrics/` — Song lyrics

Only create a new directory when the topic does not fit any of the five categories above. In that case, also add a new section to `nav:` in `mkdocs.yml`.

## File naming

- Lowercase kebab-case `.md` filenames (e.g. `body-issues.md`, `online-meeting.md`).
- Do not use Korean filenames.
- Use `-` instead of spaces.

## Registering in `mkdocs.yml` (required)

Every new page must be added to the `nav:` section of `mkdocs.yml`. Pages that are not registered will not appear in the sidebar. Add the entry next to other pages in the same directory.

## Page structure

1. The first line is the H1 title.
    - For Korean-context pages (emotions, grammar explanations, etc.) use a Korean title, e.g. `# 감정`, `# 전치사`.
    - For pages where an English keyword is natural (situations, reading, lyrics) use an English title, e.g. `# Restaurant`, `# Warning`.
2. The body is a bullet list (`*`) of expressions or sentences.
3. Put supplementary notes (example sentences, Korean glosses, comparison notes) as indented nested bullets.

    ```markdown
    * I'm so annoyed. : 나 완전 짜증나
        * My brother is so annoying. (내 남동생 완전 사람 짜증나게 해)
    ```

4. When subdividing a page further, use `##` or `###` headings (e.g. `### 메뉴 고르는 중`, `### 먹고 나서` on the restaurant page).
5. Reading pages use `[Article title](URL)` as the top-level bullet, with excerpts/summary sentences as nested bullets.

## Notation rules

- Attach Korean meanings or nuance notes after the English sentence with `:` or in parentheses.
    - `* I'm scared. : 무서워`
    - `* Are you mad? : 너 삐졌어?`
- Organize word comparisons as indented bullets.
    - For pairs with subtle differences like `thankful` vs `grateful`, write one line per word.
- Use `<br>` for forced line breaks. Do not use GitBook-style backslash line breaks (`\`); see commit `4d3b9e9`.
- Feel free to use Material for MkDocs / pymdownx extensions such as code fences, tables, and admonitions. See `markdown_extensions` in `mkdocs.yml`.

## Content principles

- Keep each bullet short — ideally a single utterance you would actually say out loud.
- If a page's topic becomes too broad, split it; if a page is too narrow and overlaps with another, merge them. Reflect any split or merge in `mkdocs.yml` as well (see commit `6390b6b`).
- If new content fits an existing page, append to that page instead of creating a new one.

## Review checklist

After adding or editing a page, verify:

1. The page is registered in `mkdocs.yml`.
2. There is exactly one H1 title.
3. The filename is kebab-case.
4. The directory matches the topic.
