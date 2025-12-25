---
allowed-tools: Read, Write, Edit, Glob, Grep
description: Examine session for mistakes, extract lessons for mnemosyne
model: opus
---

# Skepsis Command

Analyze the current session to identify corrections and distill into lessons.

## What to Look For

Scan the conversation for:
1. **Direct corrections**: "No, that's wrong", "Actually...", "Not quite"
2. **Redirections**: User interrupted or changed approach
3. **Failed attempts**: Code that errored, plans rejected
4. **Explicit feedback**: "The issue was...", "This broke because..."
5. **Misunderstandings**: Initial interpretation missed the mark

## Workflow

1. **Scan session**: Review conversation from the beginning
2. **Identify corrections**: Find instances matching patterns above
3. **Extract lessons**: For each correction, distill into a concise rule
4. **Categorize**: Which mnemosyne file does this belong to?
   - Check existing files: `ls ~/.claude/skills/mnemosyne/`
   - Suggest new file if no match
5. **Draft lesson**: Format using standard template
6. **Present for approval**: Show proposed lesson(s)
7. **On approval**: Append to appropriate file

## Output Format

For each lesson identified:

```markdown
## Proposed Lesson

**File**: mnemosyne/[category].md
**Entry**: - **[Title]**: [Concise actionable guidance]

Add this lesson?
```

## Guidelines

- Only extract genuine lessons, not typos
- Generalize: turn specific errors into reusable wisdom
- One correction might yield multiple lessons (or none)
- If unsure about category, ask the user
