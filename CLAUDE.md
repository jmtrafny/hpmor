# The Weight of Atlantis - Novella Project

## Project Overview

This repository contains the development materials for "The Weight of Atlantis," an HPMOR-adjacent dual-protagonist novella exploring the origins of wizard-Muggle separation through the eyes of Arthur Pendragon and Merlin.

**Core Premise**: A 14-year-old rationalist king who believes all knowledge should be free confronts a 500-year-old wizard who knows that some truths are too dangerous to share.

## Repository Structure

```
hpmor/
├── .claude/commands/           # Multi-agent workflow definitions
│   └── novella/                # Story-specific agents
│
├── novella/                    # All story development files
│   ├── reference/              # Source materials & decisions
│   │   ├── ARTHUR_STORY_BIBLE.md
│   │   ├── MERLIN_STORY_BIBLE.md
│   │   ├── COMBINED.md
│   │   └── STORY_DECISIONS.md  # Human Gate 0 approved decisions
│   │
│   ├── development/            # Phase outputs
│   │   ├── STORY_ARCHITECTURE.md   # Phase 0 output
│   │   ├── CHARACTER_PROFILES.md   # Phase 1 output
│   │   ├── WORLD_BIBLE.md          # Phase 1 output
│   │   ├── FOUNDATION_SYNTHESIS.md # Phase 1 synthesis
│   │   ├── PLOT_OUTLINE.md         # Phase 2 output (25-chapter outline)
│   │   ├── CONTINUITY_BIBLE.md     # Phase 2 output (timeline/tracking)
│   │   └── VOICE_CALIBRATION_REPORT.md # Phase 3A voice analysis
│   │
│   ├── chapters/               # Draft chapters and scenes
│   │   ├── CHAPTER_ONE.md          # Original draft
│   │   ├── CHAPTER_ONE_REVISED.md  # Phase 3A revision (use this)
│   │   ├── CHAPTER_TWO.md          # Phase 3A draft (Merlin POV)
│   │   ├── CHAPTER_THREE.md        # Phase 3A draft (Healer's Refusal)
│   │   ├── CHAPTER_IDEA_PENDRAGON.md
│   │   ├── THE_MIRROR_SHOWS_ARTHUR.md
│   │   └── MIDPOINT_CRUX.md
│   │
│   └── workflow/               # Process documentation
│       ├── NOVELLA_WORKFLOW_DESIGN.md
│       └── HOW_TO_USE_MULTI_AGENT.md
│
├── hpmor-world-guide/                # HPMOR canon reference (complete)
│   ├── magic/                  # Magic system rules
│   ├── cosmology/              # Atlantis, Source of Magic
│   ├── characters/             # HPMOR character profiles
│   └── ...                     # Other reference categories
│
└── other_works/                # Other story ideas (reference)
```

## Multi-Agent Workflow

This project uses a structured multi-agent workflow with human validation gates. See `novella/workflow/NOVELLA_WORKFLOW_DESIGN.md` for full details.

### Phases
- **Phase 0**: Story Architecture (COMPLETE - approved at Human Gate 0)
- **Phase 1**: Foundation (COMPLETE - Character Profiles + World Bible)
- **Phase 2**: Structure (COMPLETE - Plot Outline + Continuity Bible)
- **Phase 3A**: Opening Chapters 1-3 (COMPLETE - under revision)
- **Phase 3B**: Middle Chapters 4-10 (NEXT - parallel Arthur/Merlin streams)
- **Phase 3C**: Convergence Chapters 11-25 (pending)
- **Phase 4**: Polish (Editor + Final Review)

### Available Agents
Located in `.claude/commands/novella/`:
- `/novella/orchestrator` - Workflow coordinator
- `/novella/story-architect` - Story assessment and planning
- `/novella/character-designer` - Character profiles and voice guides
- `/novella/world-builder` - Setting and world bible
- `/novella/plot-developer` - Chapter outlines and scene beats
- `/novella/scene-writer` - Prose drafting
- `/novella/dialogue-specialist` - Dialogue and voice
- `/novella/editor` - Polish and consistency
- `/novella/continuity-keeper` - Canon compliance

## Key Story Elements

### Protagonists
- **Arthur Pendragon** (14-15): Peasant-born rationalist king, idealistic, believes knowledge should be free
- **Merlin** (500+ years): Ancient wizard bearing the weight of Atlantis's secret, choosing restriction daily

### Core Conflict
Arthur's rationalist principles clash with Merlin's terrible knowledge: the last civilization that democratized magic destroyed itself completely.

### HPMOR Integration
- The Interdict is scar tissue from Atlantis's destruction, not a spell Merlin cast
- Magic is a living, wounded force that learned wariness
- The Mirror of Erised survived because it was the epicenter of the catastrophe
- Compatible with all established HPMOR canon

### Approved Decisions (Human Gate 0)
- **Frame Story**: Pure historical (no Harry frame)
- **Arthur's Age**: 14-15 (boy-king prodigy)
- **Ending**: The binding that begins wizard-Muggle separation
- **Lancelot**: Enemies-to-friends arc, Arthur's closest confidant

## Working with This Project

### For Development
1. Reference `novella/development/` for current character/world specs
2. Check `novella/reference/STORY_DECISIONS.md` for approved creative choices
3. Consult `world-guide/` for HPMOR canon compatibility

### For Writing
1. Use voice guides in `CHARACTER_PROFILES.md`
2. Reference `WORLD_BIBLE.md` for setting details and atmosphere
3. Follow sensory palette and tonal guidelines

### For Agents
1. Read the relevant development documents before generating content
2. Maintain consistency with approved decisions
3. Flag any potential canon conflicts

## Current Status

**Phase 3A Complete** - Opening chapters 1-3 drafted and under human revision.

### What's Done:
- Chapters 1-3 drafted (CHAPTER_ONE_REVISED.md, CHAPTER_TWO.md, CHAPTER_THREE.md)
- Voice calibration report completed
- 25-chapter plot outline in PLOT_OUTLINE.md
- Timeline/continuity tracking in CONTINUITY_BIBLE.md

### Next Step (Phase 3B):
Write chapters 4-10 using parallel streams:
- **Arthur Stream**: Chapters 4-7 (Lancelot intro, plague politics, Saxon wizard)
- **Merlin Stream**: Interludes 2-4 (memory fragments, watching Arthur)

To resume: Read PLOT_OUTLINE.md for chapter specifications, CHARACTER_PROFILES.md for voice guides.
