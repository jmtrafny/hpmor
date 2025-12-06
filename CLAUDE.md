# HPMOR World Guide Extraction Task

## Project Goal

Build a comprehensive world guide from the Harry Potter and the Methods of Rationality (HPMOR) source text. This guide will later power an interactive writing assistant app for fanfiction authors. The goal is to extract, organize, and condense all world-relevant information from the source material into structured, searchable documents.

## Source Material

The repository contains the full HPMOR text. Familiarize yourself with the file structure before beginning extraction. The story is approximately 122 chapters.

## Output Structure

Create a `world-guide/` directory with the following structure:

```
world-guide/
├── README.md                    # Overview and usage guide
├── meta/
│   ├── extraction-notes.md      # Your notes on ambiguities, decisions made
│   └── source-index.md          # Chapter-by-chapter content summary
│
├── magic/
│   ├── fundamental-rules.md     # Core laws and limits of magic
│   ├── interdict-of-merlin.md   # The Interdict and its implications
│   ├── time-turners.md          # Time travel rules and paradox conditions
│   ├── transfiguration.md       # Including Partial Transfiguration
│   ├── patronus.md              # Patronus 2.0 and requirements
│   ├── dark-arts.md             # Horcruxes, Unforgivables, etc.
│   ├── spells-catalog.md        # All named spells with effects and limitations
│   └── magical-items.md         # Artifacts, objects, devices
│
├── cosmology/
│   ├── source-of-magic.md       # Atlantis, the "hack" theory, origins
│   ├── death-and-dementors.md   # Nature of dementors, afterlife questions
│   ├── prophecy-mechanics.md    # How prophecy works in HPMOR
│   └── mysteries-unsolved.md    # Deliberately unexplained elements
│
├── characters/
│   ├── _template.md             # Template for character entries
│   ├── harry-james-potter-evans-verres.md
│   ├── quirinus-quirrell.md     # Defense Professor / Voldemort
│   ├── hermione-granger.md
│   ├── draco-malfoy.md
│   ├── albus-dumbledore.md
│   ├── severus-snape.md
│   ├── minerva-mcgonagall.md
│   ├── lucius-malfoy.md
│   ├── petunia-evans-verres.md
│   ├── michael-verres-evans.md
│   └── [other significant characters].md
│
├── organizations/
│   ├── hogwarts.md              # Structure, rules, houses
│   ├── wizengamot.md            # Political structure, procedures
│   ├── ministry-of-magic.md     # Government structure
│   ├── death-eaters.md          # History, members, methods
│   ├── order-of-phoenix.md      # If mentioned
│   └── noble-houses.md          # Malfoy, Bones, Longbottom, etc.
│
├── locations/
│   ├── hogwarts-geography.md    # Rooms, passages, notable locations
│   ├── diagon-alley.md
│   ├── azkaban.md
│   └── other-locations.md
│
├── timeline/
│   ├── backstory.md             # Events before story begins
│   ├── year-one-timeline.md     # Chronological chapter events
│   └── post-story-state.md      # World state at story's end
│
├── themes/
│   ├── rationality-concepts.md  # Bayesian reasoning, cognitive biases, etc.
│   ├── scientific-method.md     # Harry's experimental approaches
│   └── ethical-frameworks.md    # Consequentialism, heroic responsibility
│
└── writing-reference/
    ├── voice-guides.md          # How major characters speak
    ├── canon-divergences.md     # Key differences from HP canon
    ├── common-pitfalls.md       # Mistakes to avoid in fanfic
    └── loose-threads.md         # Unexplored story hooks for writers
```

## Extraction Guidelines

### For Each Entry

1. **Cite Sources**: Include chapter references for every claim. Format: `[Ch. 42]` or `[Ch. 42-45]` for spans.

2. **Distinguish Confidence Levels**:
   - **EXPLICIT**: Directly stated in text (quote if concise)
   - **STRONGLY IMPLIED**: Clear from context, not directly stated
   - **INFERRED**: Reasonable conclusion from multiple data points
   - **AMBIGUOUS**: Deliberately unclear or contradictory in source

3. **Include Direct Quotes**: For rules, laws, and key characterizations, include the actual text in blockquotes. Keep quotes concise (1-3 sentences) and always cite.

4. **Note Contradictions**: If the text contradicts itself or leaves something unclear, document this explicitly.

### Character Entry Template

Use this structure for each character file:

```markdown
# [Character Name]

## Basic Information
- **Full Name**: 
- **House**: (if applicable)
- **Role**: 
- **First Appearance**: [Ch. X]

## HPMOR vs Canon Divergences
[Key differences from original Harry Potter]

## Personality & Motivations
[Core drives, values, fears, blind spots]
- Include confidence level tags
- Cite specific scenes that demonstrate traits

## Key Relationships
[How they relate to other major characters]

## Character Arc
[How they change over the story, major turning points]

## Voice & Speech Patterns
- Vocabulary level:
- Common phrases/verbal tics:
- What references do they make:
- Sample dialogue: [with chapter citations]

## Notable Scenes
[List of chapters where they feature prominently]

## Writer Notes
[Practical advice for writing this character faithfully]
```

### Magic System Entries

For each magical concept, document:
- What it does
- Known limitations (VERY IMPORTANT)
- Cost or requirements
- Who can/can't use it
- How Harry's understanding differs from traditional wizard understanding
- Direct quotes establishing rules
- Edge cases or ambiguities

### Conciseness Guidelines

The final guide should be **information-dense but scannable**. This will be embedded in an app, so:

- Use bullet points for quick reference
- Put detailed analysis in collapsible sections or clearly marked "Deep Dive" subsections
- Front-load the most important information
- Avoid redundancy across files (cross-reference instead)
- Target approximately 500-2000 words per file depending on complexity

## Processing Approach

### Phase 1: Survey
Read through the source material and create `meta/source-index.md` with a chapter-by-chapter summary noting which world guide topics each chapter addresses.

### Phase 2: Extract by Category
Work through each category systematically:
1. Magic system rules first (they inform everything else)
2. Cosmology and mysteries
3. Characters (major first, then supporting)
4. Organizations and locations
5. Timeline
6. Writing reference materials

### Phase 3: Cross-Reference
Review all files and:
- Add cross-references between related entries
- Ensure no contradictions between files
- Fill gaps discovered during extraction

### Phase 4: Quality Pass
- Verify all citations
- Ensure confidence levels are tagged
- Check that direct quotes are accurate
- Confirm writer-relevant information is present

## Special Considerations

### The Interdict of Merlin
This is crucial for plot logic. Document thoroughly:
- Exact wording of the limitation
- What counts as "powerful" magic
- How this affects what ancient knowledge can be recovered
- Implications for plot devices in fanfiction

### Time-Turner Rules
Document the paradox conditions exhaustively. This is one of the most common sources of plot holes in fanfiction.

### Quirrell/Voldemort
Handle carefully:
- Document what's known at each point in the story
- Separate "what Harry knows" from "what readers know"
- Track the deception and revelation timeline

### Harry's Voice
This is critical for fanfiction writers. Document:
- His speech patterns at different emotional states
- What pop culture/science references he makes
- How he explains concepts to others
- His internal monologue style

## Output Format

All files should be **Markdown** with:
- Clear hierarchical headers
- Blockquotes for direct citations
- Inline tags for confidence levels: `[EXPLICIT]`, `[IMPLIED]`, `[INFERRED]`, `[AMBIGUOUS]`
- Cross-references as relative links: `[See Transfiguration](../magic/transfiguration.md)`

## Success Criteria

The finished world guide should allow a fanfiction writer to:
1. Quickly check if a magical ability is possible within HPMOR rules
2. Write dialogue that sounds like the actual characters
3. Understand character motivations and likely responses
4. Know what's been established vs. what's open for interpretation
5. Avoid common mistakes and contradictions with source material
6. Find story hooks and unexplored threads to develop

## Begin

Start by exploring the repository structure to understand how the source text is organized, then proceed with Phase 1.
