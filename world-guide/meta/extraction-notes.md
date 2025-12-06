# HPMOR World Guide Extraction Notes

## Methodology

### Extraction Approach

This world guide was created through a systematic multi-phase extraction process:

1. **Phase 1: Breadth Survey** - All 124 chapters read to create content index
2. **Phase 2A: Magic System** - Deep extraction of magical rules and mechanics
3. **Phase 2B: Characters** - Detailed profiling of major characters
4. **Phase 3: World Structure** - Organizations, locations, and timeline
5. **Phase 4: Meta Analysis** - Cosmology, themes, and writing reference
6. **Phase 5: Quality & Cross-Reference** - Verification and linking
7. **Phase 6: Final Assembly** - Statistics and completion

### LaTeX Processing

Source material is in LaTeX format. All formatting was stripped for this guide:
- `\chapter{}`, `\lettrine{}`, `\partchapter{}` → Removed
- `\emph{}`, `\textit{}` → Converted to `*italic*`
- `\textbf{}` → Converted to `**bold**`
- `\spell{}`, `\parsel{}`, `\shout{}` → Content preserved, markup removed
- Chapter opening quotes and author notes → Removed
- All other LaTeX commands → Stripped

Output is pure Markdown suitable for embedding in applications.

### Confidence Level Definitions

**[EXPLICIT]** - Directly stated in the source text
- Often includes a direct quote
- No interpretation required
- Example: "Time-Turners can't send information more than six hours back" [Ch. 17]

**[IMPLIED]** - Strongly suggested by the text, clear from context
- Not explicitly stated but clearly intended
- Reasonable readers would agree
- Example: Harry's parents being academics influences his thinking [Ch. 1-5]

**[INFERRED]** - Reasonable conclusion from multiple data points
- Requires synthesizing information across chapters
- Logical deduction from evidence
- Example: Quirrell's teaching methods suggest specific pedagogical philosophy [Ch. 22-30]

**[AMBIGUOUS]** - Deliberately unclear or contradictory
- May be intentionally left mysterious
- Different interpretations possible
- Important for writers to know what's *not* established
- Example: Exact nature of magic's source [Various chapters]

### Citation Format

- `[Ch. 42]` - Single chapter reference
- `[Ch. 42-45]` - Continuous range
- `[Ch. 7, 15, 23]` - Multiple specific chapters
- `[Ch. 42:p.5]` - Specific page in printed edition (rarely used)

All claims should include chapter citations for verification.

## Key Decisions Made

### Canon Divergences

Focus is on **HPMOR canon only**, not Harry Potter canon. When HP canon is relevant for comparison, it's noted explicitly in:
- Character profiles (HPMOR vs Canon section)
- `writing-reference/canon-divergences.md`

### Character Selection

**Major characters** (10 full profiles):
- Those appearing in 20+ chapters
- Critical to main plot
- High fanfiction usage

**Secondary characters** (brief profiles):
- Significant but fewer appearances
- May be expanded in future

**Background characters** (mentions only):
- Named but minimal development
- Listed in source index

### Magic System Organization

Magic documented by **concept** rather than strictly by type:
- `fundamental-rules.md` covers cross-cutting principles
- Specific magics get dedicated files (Time-Turners, Transfiguration, etc.)
- `spells-catalog.md` is alphabetical reference
- Cross-references connect related concepts

### Voice Documentation

Character voice samples selected to show:
- Normal/baseline speech
- Emotional extremes (angry, stressed, joyful)
- Explanatory/teaching mode
- Interactions with specific other characters

Variety is prioritized over quantity.

### Ambiguities & Open Questions

When source material is deliberately unclear, this is **documented explicitly** rather than resolved through inference. Writers benefit from knowing what's open for interpretation.

## Challenges Encountered

### LaTeX Complexity

Some chapters use complex LaTeX structures:
- McGonagall's whiteboard (formatted tables)
- Newspaper headlines (special fonts)
- Parseltongue (marked with `\parsel{}`)
- Spell incantations (marked with `\spell{}`)

Solution: Preserved content, stripped formatting, noted special formatting in context.

### Chapter Numbering

Chapters 11 and 64 are "Omake Files" (bonus content):
- Main text jumps from Ch. 10 to Ch. 12
- Omakes included in source index but noted as non-canon sidestories

### Timeline Reconstruction

HPMOR doesn't always provide explicit dates. Timeline built from:
- Explicit time markers when given
- Time-Turner usage (6-hour windows)
- Seasonal/holiday references
- Event sequencing

Some dates remain approximate.

### Character Knowledge vs Reader Knowledge

Especially for Quirrell/Voldemort:
- What Harry knows vs what readers know
- When revelations occur
- Foreshadowing vs explicit confirmation

Documented separately to avoid spoiling the reveal structure.

## Extraction Statistics

### Source Material
- Chapters processed: 124
- Total words: ~636,000
- Total lines: ~41,000
- File format: LaTeX (.tex)

### Output
- Total files created: [Updated as phases complete]
- Total guide words: [Updated as phases complete]
- Average file size: [Updated as phases complete]

### Progress Tracking
See `extraction-progress.json` for detailed phase-by-phase status.

## Future Expansion Possibilities

- Additional character profiles (secondary cast)
- Chapter-by-chapter summaries (beyond index)
- Thematic analysis by part
- Comparative analysis with HP canon
- Fan theory documentation (clearly marked as non-canon)

## Unresolved Ambiguities

[To be populated during extraction - things that remain unclear even after thorough reading]

## Cross-Reference Notes

[To be populated during Phase 5 - patterns in how concepts connect]

---

*Document Status: Initialized in Phase 0, to be updated throughout extraction*
*Last Updated: [Date of last modification]*
