Rules: direct, minimal, imperative.

Rule format:
When [situation]:
- Do X
- Never do Y
- If Z, then W

Example: [concrete case if necessary]

Rule numbering:
- 01-29: Reserved for base rules from this repository
- 30+: Project-specific rules

When creating new rule:
- Identify specific problem
- Create file: XX-descriptive-name.md (XX = next number after last existing file)
- If base rule: use 01-29 range
- If project-specific rule: start from 30
- Use format above
- Add to 00-rules-index.md

When updating rule:
- Keep minimal
- Update examples

When removing content from rules:
- Never remove content without human supervision
- Only delete if explicitly requested by user
- Ask for confirmation before removing any rule content

When content overlaps between rules:
- Keep detailed content in one file
- Reference it from other files using: "See XX-filename.md for detailed rules"
- Never duplicate the same content in multiple files

Example: If rule 06 and 08 both cover copying, keep details in 08, reference from 06.