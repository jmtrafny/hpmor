# Hybrid Workflow Pattern for Novella Writing

This workflow combines sequential phases with parallel execution within phases, offering the best balance of efficiency and quality control for creative writing projects.

## Pattern Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                    NOVELLA HYBRID WORKFLOW                      │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  PHASE 1: CONCEPT (Sequential)                                  │
│  ┌─────────────────────┐                                        │
│  │   Story Architect   │ → Story Architecture Document          │
│  └─────────────────────┘                                        │
│            │                                                    │
│            ▼ [Human Gate: Approve Concept]                      │
│                                                                 │
│  PHASE 2: FOUNDATION (Parallel)                                 │
│  ┌─────────────────────┐                                        │
│  │ Character Designer  │──┐                                     │
│  └─────────────────────┘  │                                     │
│  ┌─────────────────────┐  ├──→ Synthesize → Foundation Docs     │
│  │    World Builder    │──┘                                     │
│  └─────────────────────┘                                        │
│            │                                                    │
│            ▼ [Human Gate: Approve Foundation]                   │
│                                                                 │
│  PHASE 3: STRUCTURE (Sequential)                                │
│  ┌─────────────────────┐                                        │
│  │   Plot Developer    │ → Complete Plot Outline                │
│  └─────────────────────┘                                        │
│            │                                                    │
│            ▼ [Human Gate: Approve Plot]                         │
│                                                                 │
│  PHASE 4: WRITING (Hybrid - Sequential Acts, Parallel Chapters) │
│  ┌─────────────────────────────────────────────────────────┐    │
│  │  ACT 1: Write Ch.1 → Write Ch.2 → Write Ch.3            │    │
│  │         [Human Gate: Approve Opening]                    │    │
│  │                                                          │    │
│  │  ACT 2: ┌── Ch.4 ──┐                                     │    │
│  │         │── Ch.5 ──│ (Parallel batches)                  │    │
│  │         └── Ch.6 ──┘                                     │    │
│  │         [Human Gate: Approve Middle]                     │    │
│  │                                                          │    │
│  │  ACT 3: Write Ch.7 → Write Ch.8 (climax) → Ch.9          │    │
│  │         [Human Gate: Approve Draft]                      │    │
│  └─────────────────────────────────────────────────────────┘    │
│            │                                                    │
│            ▼                                                    │
│                                                                 │
│  PHASE 5: POLISH (Parallel)                                     │
│  ┌─────────────────────┐                                        │
│  │       Editor        │──┐                                     │
│  └─────────────────────┘  │                                     │
│  ┌─────────────────────┐  ├──→ Synthesize → Final Revisions     │
│  │  Continuity Keeper  │──┘                                     │
│  └─────────────────────┘                                        │
│            │                                                    │
│            ▼ [Human Gate: Final Approval]                       │
│                                                                 │
│  ╔═════════════════════════════════════════════════════════╗    │
│  ║               COMPLETED NOVELLA                         ║    │
│  ╚═════════════════════════════════════════════════════════╝    │
└─────────────────────────────────────────────────────────────────┘
```

## Why Hybrid for Novella Writing?

### Sequential Benefits
- Clear phase progression
- Human gates at natural stopping points
- Creative vision stays coherent
- Easy to track progress

### Parallel Benefits
- Characters and world developed together (share inspiration)
- Multiple chapters written efficiently
- Editor and Continuity Keeper work simultaneously
- Faster overall completion

### The Balance
- Concept must come first (everything depends on it)
- Foundation elements can develop together
- Plot needs foundation complete
- Writing has some parallel opportunity
- Polish benefits from multiple perspectives at once

## Phase Details

### Phase 1: Concept (Sequential)

**Why Sequential:** Everything flows from the concept. There's nothing to parallelize yet.

**Agent:** Story Architect

**Duration:** 1 agent session

**Deliverables:**
- Story Architecture Document
  - Premise and logline
  - Themes
  - Narrative structure
  - Scope parameters

**Human Gate Questions:**
- Is this the story you want to write?
- Do the themes resonate?
- Is the scope appropriate?

---

### Phase 2: Foundation (Parallel)

**Why Parallel:** Characters and world can be developed simultaneously—they inform each other but don't block each other.

**Agents (Parallel):**
- Character Designer
- World Builder

**How to Execute:**

```markdown
Launch both agents in a single message:

Task(
    subagent_type="general-purpose",
    prompt="[Character Designer prompt with Story Architecture context]"
)

Task(
    subagent_type="general-purpose",
    prompt="[World Builder prompt with Story Architecture context]"
)
```

**Synthesis Required:**
After both complete, ensure:
- Characters fit the world
- World serves character stories
- No contradictions between outputs
- Shared elements are consistent (e.g., if both mention the same location)

**Deliverables:**
- Character Profiles
- World Bible
- Synthesis Notes (how they connect)

**Human Gate Questions:**
- Do characters feel compelling?
- Does the world serve the story?
- Any conflicts between character and world?

---

### Phase 3: Structure (Sequential)

**Why Sequential:** Plot depends on both characters AND world being complete. It's the integration point.

**Agent:** Plot Developer

**Duration:** 1 agent session (longer session)

**Deliverables:**
- Complete Plot Outline
  - Chapter breakdown
  - Scene-level detail
  - Character arc integration
  - World element usage

**Human Gate Questions:**
- Does the plot serve the themes?
- Are character arcs satisfying?
- Is pacing appropriate?
- Any structural concerns?

---

### Phase 4: Writing (Hybrid)

**Why Hybrid:**
- Act 1 must be sequential (establishes everything)
- Act 2 chapters often have parallel potential
- Act 3 benefits from sequential (building to climax)
- But dialogue can be polished in parallel with drafting

**Structure:**

```
ACT 1 (Sequential):
  Scene Writer → Ch.1
  Scene Writer → Ch.2
  Scene Writer → Ch.3
  [GATE: Opening chapters approval]

ACT 2 (Parallel Batches):
  Batch 1: Scene Writer → Ch.4, Ch.5 (parallel if independent)
  Batch 2: Scene Writer → Ch.6, Ch.7 (parallel if independent)
  Dialogue Specialist → Polish key exchanges (parallel with next batch)
  Continuity Keeper → Tracking (ongoing)
  [GATE: Middle chapters approval]

ACT 3 (Sequential):
  Scene Writer → Ch.8 (crisis)
  Scene Writer → Ch.9 (climax)
  Scene Writer → Ch.10 (resolution)
  [GATE: Draft complete approval]
```

**Parallel Opportunities in Writing:**
- Chapters that don't directly follow each other
- Different POV threads
- Parallel timelines in the story
- Dialogue polish while new chapters draft

**Constraints on Parallelism:**
- Each chapter needs the previous chapter's ending
- Character knowledge must be accurate
- Don't parallel chapters that share a scene

**Deliverables:**
- Draft manuscript (chapter by chapter)
- Updated continuity bible
- Polished key dialogue

---

### Phase 5: Polish (Parallel)

**Why Parallel:** Editor and Continuity Keeper have different focuses. They can work the same manuscript simultaneously.

**Agents (Parallel):**
- Editor (structural and line editing)
- Continuity Keeper (final consistency check)

**How to Execute:**

```markdown
Launch both agents in a single message:

Task(
    subagent_type="general-purpose",
    prompt="[Editor prompt with full manuscript]"
)

Task(
    subagent_type="general-purpose",
    prompt="[Continuity Keeper prompt with full manuscript + story bible]"
)
```

**Synthesis Required:**
- Merge editorial suggestions with continuity flags
- Prioritize issues
- Resolve any conflicts (editor's prose change vs. continuity requirement)

**Deliverables:**
- Editorial Report
- Continuity Report
- Prioritized Revision List
- Final Polished Manuscript (after revisions)

**Human Gate Questions:**
- Are you satisfied with the manuscript?
- Any remaining concerns?
- Ready to call it complete?

---

## Time Estimates

| Phase | Sequential Time | Hybrid Time | Savings |
|-------|-----------------|-------------|---------|
| Concept | 30 min | 30 min | 0% |
| Foundation | 60 min | 35 min | ~40% |
| Structure | 45 min | 45 min | 0% |
| Writing | 180 min | 140 min | ~20% |
| Polish | 60 min | 35 min | ~40% |
| **TOTAL** | **375 min** | **285 min** | **~24%** |

*Note: Creative work varies significantly. These are rough estimates.*

## Human Gates Summary

| Gate | After | Key Questions |
|------|-------|---------------|
| Gate 1 | Concept | Is this the story to write? |
| Gate 2 | Foundation | Do characters and world work? |
| Gate 3 | Structure | Is the plot compelling? |
| Gate 4 | Act 1 | Does the opening hook? |
| Gate 5 | Act 2 | Is the middle engaging? |
| Gate 6 | Draft | Is the story complete? |
| Gate 7 | Polish | Is it ready? |

## Adaptation Guidelines

### Make It More Sequential If:
- You're new to multi-agent writing
- The story is highly experimental
- You want maximum control
- Previous phases had significant issues

### Make It More Parallel If:
- You're experienced with the system
- Time is limited
- The story structure is clear and stable
- You trust the synthesis process

### Specific Adaptations:

**Mystery Novella:**
- Keep plot development sequential (careful setup required)
- Parallel: red herrings development + clue placement review

**Character-Driven Novella:**
- More time in Phase 2 (Foundation)
- Consider sequential character development for deep POV

**Action/Adventure:**
- More parallel opportunity in writing phase
- Action sequences can often be drafted in parallel

**Literary Fiction:**
- More sequential overall
- Voice consistency requires careful coordination
- Longer polish phase

## Quick Reference

```
/novella/orchestrator [Use hybrid pattern]

CONCEPT     → Story Architect (alone)
FOUNDATION  → Character Designer + World Builder (parallel)
STRUCTURE   → Plot Developer (alone)
WRITING     → Scene Writers (hybrid: sequential acts, parallel chapters)
POLISH      → Editor + Continuity Keeper (parallel)
```

## Remember

The hybrid pattern isn't about maximizing parallelism—it's about parallelizing where it helps without sacrificing quality. Creative coherence matters more than speed.

Trust the sequential moments. They're where integration happens.
Trust the parallel moments. They're where efficiency lives.
Trust the gates. They're where humans keep creative control.
