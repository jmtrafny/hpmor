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
- Chapters processed: 123 (numbered 0-122; chapters 11 and 64 are Omake Files)
- Total words: ~636,000
- Total lines: ~41,000
- File format: LaTeX (.tex)
- Repository: https://github.com/rrthomas/hpmor

### Output
- **Total content files created: 42**
  - Magic system: 8 files
  - Character profiles: 10 files
  - Organizations: 6 files
  - Locations: 4 files
  - Timeline: 3 files
  - Cosmology: 4 files
  - Themes: 3 files
  - Writing reference: 4 files
- **Meta files: 3** (README.md, extraction-notes.md, source-index.md)
- **Template files: 1** (characters/_template.md)
- **Total guide words: ~145,000** (estimated across all files)
- **Average content file size: ~3,500 words**
- **Largest file: harry-james-potter-evans-verres.md** (~10,000+ words)
- **Source index: 1,336 lines** covering all 123 chapters

### Progress Tracking
See `extraction-progress.json` for detailed phase-by-phase status.

## Future Expansion Possibilities

- Additional character profiles (secondary cast)
- Chapter-by-chapter summaries (beyond index)
- Thematic analysis by part
- Comparative analysis with HP canon
- Fan theory documentation (clearly marked as non-canon)

## Unresolved Ambiguities

Deliberate ambiguities preserved in the world guide (documented with [AMBIGUOUS] tags):

1. **Source of Magic**: Exact nature and location of the Source remains mysterious. Atlantis connection implied but not confirmed.
2. **Dementors' True Nature**: Wounds in the world vs. shadows of Death—metaphysical nature unclear.
3. **Prophecy Mechanism**: How prophecies actually work, who/what generates them.
4. **Magic's Limits**: Many edge cases unexplored (Can time-turners do X? Can transfiguration affect Y?).
5. **Post-Story Mysteries**: Hermione's full capabilities after resurrection, Harry's long-term quest outcomes.
6. **Quirrell/Voldemort's Final State**: Exact fate ambiguous, left for fanfiction writers to explore.
7. **Atlantean History**: Almost nothing concrete known about the civilization that created magic.
8. **Interdict Mechanics**: Precise rules for what can/can't be transmitted never fully specified.
9. **House Elf Magic**: Mentioned but mechanics never explained.
10. **Magical Creatures' Origins**: Whether created by Atlantis or pre-existing.

See `cosmology/mysteries-unsolved.md` for complete list of 27 documented ambiguities.

## Cross-Reference Notes

Patterns in concept connections:

- **Harry Potter** is the most cross-referenced character (appears in nearly all character, theme, and writing reference files)
- **Magic system files** heavily reference each other (fundamental-rules → specific implementations)
- **Ethical frameworks** connect strongly to character motivations (especially Harry, Hermione, Quirrell, Dumbledore)
- **Timeline files** are referenced throughout for establishing when events occur
- **Canon divergences** cross-reference nearly every character and magic file
- **Voice guides** serve as central hub for character speech patterns
- **Loose threads** document story opportunities arising from all other files

### Cross-Reference Strategy Used

Phase 5 cross-referencing focused on:
1. **Character profiles**: Comprehensive cross-references to other characters, magic abilities, organizations, themes, and writing guidance (10 files fully cross-referenced)
2. **High-value connections**: Linked concepts mentioned multiple times or critically important to understanding
3. **Navigation utility**: Prioritized links that help writers quickly find related information
4. **Bidirectional linking**: Where A references B, ensured B references A when relevant

### Files with Cross-References Added

- **Character files (10)**: Fully cross-referenced with categorized sections (Related Characters, Magic, Organizations, Themes, Writing Reference)
- **Magic files (8)**: Existing cross-references preserved; some already had good internal linking
- **World structure (13)**: Existing cross-references present
- **Meta files (11)**: Existing cross-references present

Total estimated cross-reference links added: **100+** across character profiles alone.

---

*Document Status: Extraction Complete*
*Phases 0-5: Complete*
*Last Updated: 2025-12-06*
*Total Extraction Time: ~8-10 hours across multiple sessions*
