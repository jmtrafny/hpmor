# Novella Multi-Agent Workflow

A sophisticated multi-agent system for collaboratively writing novellas using specialized AI agents.

## Overview

This system coordinates multiple specialized agents to produce complete, polished novellas through a structured creative workflow. Each agent is an expert in one aspect of storytelling, and together they create works that would be difficult for any single agent to produce.

## Quick Start

```bash
# Start the full guided workflow
/novella/orchestrator I want to write a novella about [your concept]

# Or specify a workflow pattern
/novella/orchestrator Use hybrid pattern for a mystery novella

# Or use individual agents
/novella/story-architect
/novella/character-designer
/novella/scene-writer
```

## Available Agents

| Agent | Command | Purpose |
|-------|---------|---------|
| **Orchestrator** | `/novella/orchestrator` | Coordinates the full workflow |
| **Story Architect** | `/novella/story-architect` | Designs premise, themes, structure |
| **Character Designer** | `/novella/character-designer` | Creates compelling characters |
| **World Builder** | `/novella/world-builder` | Crafts settings and atmosphere |
| **Plot Developer** | `/novella/plot-developer` | Structures the narrative |
| **Scene Writer** | `/novella/scene-writer` | Writes actual prose |
| **Dialogue Specialist** | `/novella/dialogue-specialist` | Crafts authentic dialogue |
| **Editor** | `/novella/editor` | Reviews and improves |
| **Continuity Keeper** | `/novella/continuity-keeper` | Maintains consistency |

## Workflow Patterns

### 1. Sequential (Best for Learning)
Linear progression through all phases. Maximum control, clearest process.

```
Story Architect → Character Designer → World Builder → Plot Developer → Scene Writer → Editor
```

**Use when:** First time using the system, complex experimental work, maximum control needed

### 2. Hybrid (Recommended)
Sequential phases with parallel execution within phases. Best balance of speed and quality.

```
Concept (Sequential) → Foundation (Parallel) → Structure → Writing (Hybrid) → Polish (Parallel)
```

**Use when:** Most projects, familiar with the system, want efficiency without sacrificing quality

### 3. Parallel (Maximum Speed)
Maximize concurrent execution. Fastest but requires synthesis work.

**Use when:** Experienced user, time-constrained, story concept is very clear

### 4. Iterative (Discovery Writers)
Cycle through design-write-reflect loops. Write to discover the story.

```
Minimal Design → Write → Reflect → Expand Design → Write More → ...
```

**Use when:** You find stories by writing them, character-driven work, experimental approaches

## The Novella Format

Novellas are typically 20,000-50,000 words, longer than short stories but shorter than novels. This format demands:

- **Focused scope** - Usually one main plot, limited subplots
- **Smaller cast** - 3-7 main characters typical
- **Tighter timeline** - Often compressed compared to novels
- **Efficient storytelling** - Every scene must earn its place
- **Unity of effect** - Working toward a single powerful impression

## Workflow Phases

### Phase 1: Concept
**Agent:** Story Architect

Establishes the foundation everything else builds on:
- Premise and logline
- Themes
- Narrative structure
- Scope parameters

### Phase 2: Foundation
**Agents:** Character Designer, World Builder

Creates the people and places:
- Character profiles with arcs
- World bible with settings
- Relationship dynamics
- Atmospheric elements

### Phase 3: Structure
**Agent:** Plot Developer

Maps the complete narrative:
- Chapter breakdown
- Scene-level detail
- Tension map
- Information revelation schedule

### Phase 4: Writing
**Agents:** Scene Writer, Dialogue Specialist

Produces the actual prose:
- Chapter drafts
- Polished dialogue
- Ongoing continuity tracking

### Phase 5: Polish
**Agents:** Editor, Continuity Keeper

Refines and verifies:
- Structural editing
- Line editing
- Consistency verification
- Final revisions

## Human Validation Gates

The workflow includes checkpoints where human approval is required:

```markdown
## 🚦 CREATIVE CHECKPOINT

**Phase Completed:** [Phase Name]
**Summary:** [What was created]

**Please Review and Respond:**
- ✅ Approved - Proceed
- 📝 Revisions Needed - [Specify]
- ❓ Questions - [Ask first]
```

Gates ensure:
- Creative vision stays aligned
- Quality meets standards
- Human control is maintained
- Course correction happens early

## Example Workflow

```markdown
User: /novella/orchestrator I want to write a psychological thriller
      novella about a chess prodigy who discovers their opponent in
      a major tournament is using AI to cheat.

Orchestrator: I'll help create this novella. Based on your concept,
I recommend the Hybrid workflow pattern...

[Phase 1: Story Architect develops premise, themes, structure]
[Gate: User approves concept]

[Phase 2: Character Designer + World Builder work in parallel]
[Gate: User approves characters and world]

[Phase 3: Plot Developer creates detailed outline]
[Gate: User approves plot]

[Phase 4: Scene Writers draft chapters]
[Gates: After each act]

[Phase 5: Editor + Continuity Keeper polish]
[Gate: Final approval]

Result: Complete, polished novella manuscript
```

## Time Estimates

| Workflow | Estimated Time | Best For |
|----------|----------------|----------|
| Sequential | 7-8 hours | Learning, control |
| Hybrid | 5-6 hours | Most projects |
| Parallel | 4-5 hours | Speed priority |
| Iterative | 8-10 hours | Discovery writers |

*Active agent time. Calendar time will be longer due to human review.*

## Directory Structure

```
.claude/commands/novella/
├── orchestrator.md           # Main coordinator
├── story-architect.md        # Concept & themes
├── character-designer.md     # Character creation
├── world-builder.md          # Setting & atmosphere
├── plot-developer.md         # Story structure
├── scene-writer.md           # Prose composition
├── dialogue-specialist.md    # Dialogue craft
├── editor.md                 # Review & editing
├── continuity-keeper.md      # Consistency tracking
├── README.md                 # This file
├── patterns/
│   ├── sequential-workflow.md
│   ├── hybrid-workflow.md
│   ├── parallel-workflow.md
│   └── iterative-workflow.md
└── coordinators/
    ├── creative-synthesizer.md
    └── chapter-coordinator.md
```

## Tips for Success

### Before Starting
- Have a concept, even if rough
- Know your genre and tone preferences
- Consider your target length
- Think about themes you want to explore

### During the Process
- Engage with the gates - they're for your benefit
- Don't be afraid to request revisions
- Trust the specialized agents
- Keep notes on decisions and preferences

### For Best Results
- Start with Hybrid if unsure
- Let agents do their specialized work
- Focus your feedback on what matters most
- Remember: revision is part of the process

## Customization

Each agent can be invoked independently:

```bash
# Just need character help
/novella/character-designer [context]

# Just need dialogue polish
/novella/dialogue-specialist [scene]

# Just need editing
/novella/editor [manuscript]
```

Combine agents as needed for your specific workflow.

## Integration with Main Workflow System

This novella system follows the same patterns as the main multi-agent development workflow:

- Same orchestration principles
- Same parallel execution mechanics
- Same human gate patterns
- Same coordination approaches

If you're familiar with the software development workflow, the novella workflow will feel natural.

## Getting Help

- `/novella/orchestrator help` - Workflow guidance
- Review individual agent files for detailed capabilities
- Check pattern files for workflow details

---

**Ready to write?**

```bash
/novella/orchestrator [Your story concept here]
```

Let's create something wonderful.
