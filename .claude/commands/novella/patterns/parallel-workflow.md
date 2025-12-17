# Parallel Workflow Pattern for Novella Writing

Maximum concurrency for maximum speed. Launch multiple agents simultaneously whenever possible. Best for experienced users who want efficiency.

## Pattern Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                   NOVELLA PARALLEL WORKFLOW                     │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  PHASE 1: CONCEPT (Sequential - Can't parallelize yet)          │
│  ┌─────────────────────┐                                        │
│  │   Story Architect   │ → Story Architecture                   │
│  └─────────────────────┘                                        │
│             │ [Human Gate]                                      │
│             ▼                                                   │
│                                                                 │
│  PHASE 2: FOUNDATION (Full Parallel)                            │
│  ┌─────────────────────┐                                        │
│  │ Character Designer  │──┐                                     │
│  └─────────────────────┘  │                                     │
│  ┌─────────────────────┐  │                                     │
│  │    World Builder    │──┼──→ SYNTHESIZE → Foundation Bundle   │
│  └─────────────────────┘  │                                     │
│  ┌─────────────────────┐  │                                     │
│  │   Plot Outliner*    │──┘  (* rough outline only)             │
│  └─────────────────────┘                                        │
│             │ [Human Gate]                                      │
│             ▼                                                   │
│                                                                 │
│  PHASE 3: STRUCTURE (Sequential - Integration point)            │
│  ┌─────────────────────┐                                        │
│  │   Plot Developer    │ → Detailed Plot Outline                │
│  └─────────────────────┘                                        │
│             │ [Human Gate]                                      │
│             ▼                                                   │
│                                                                 │
│  PHASE 4: WRITING (Maximum Parallel)                            │
│  ┌──────────────────────────────────────────────────────┐       │
│  │  Launch Chapter Writers in Parallel Batches:         │       │
│  │                                                      │       │
│  │  Batch 1: Ch.1 + Ch.4 + Ch.7  (act openers)          │       │
│  │      ↓ [Synthesize & Review]                         │       │
│  │  Batch 2: Ch.2 + Ch.5 + Ch.8  (developments)         │       │
│  │      ↓ [Synthesize & Review]                         │       │
│  │  Batch 3: Ch.3 + Ch.6 + Ch.9  (act closers)          │       │
│  │      ↓ [Synthesize & Review]                         │       │
│  │                                                      │       │
│  │  Parallel Dialogue Polish (during batches)           │       │
│  │  Parallel Continuity Tracking (ongoing)              │       │
│  └──────────────────────────────────────────────────────┘       │
│             │ [Human Gate]                                      │
│             ▼                                                   │
│                                                                 │
│  PHASE 5: POLISH (Full Parallel)                                │
│  ┌─────────────────────┐                                        │
│  │  Editor (Structure) │──┐                                     │
│  └─────────────────────┘  │                                     │
│  ┌─────────────────────┐  │                                     │
│  │  Editor (Line)      │──┼──→ SYNTHESIZE → Revision Plan       │
│  └─────────────────────┘  │                                     │
│  ┌─────────────────────┐  │                                     │
│  │  Continuity Final   │──┘                                     │
│  └─────────────────────┘                                        │
│             │ [Human Gate]                                      │
│             ▼                                                   │
│  ╔═════════════════════════════════════════════════════════╗    │
│  ║               COMPLETED NOVELLA                         ║    │
│  ╚═════════════════════════════════════════════════════════╝    │
└─────────────────────────────────────────────────────────────────┘
```

## Why Choose Parallel?

### Best For:
- **Experienced users** - Understand how agents interact
- **Time-constrained projects** - Speed is priority
- **Clear, stable concepts** - Story vision is locked
- **Independent story threads** - Multiple POVs or parallel plots
- **Large projects** - More opportunities for parallelization

### Trade-offs:
- ✅ 40-60% faster than sequential
- ✅ Multiple perspectives on same elements
- ✅ Efficient use of agent resources
- ❌ Requires more synthesis work
- ❌ Higher risk of inconsistency
- ❌ Harder to course-correct mid-stream
- ❌ Requires experience to manage well

## Critical Rule: Single Message for Parallel Agents

**All parallel agents MUST be launched in a single message for true concurrent execution.**

```markdown
CORRECT (Parallel):
In a single message, invoke all three:
- Task(prompt="Character Designer task...")
- Task(prompt="World Builder task...")
- Task(prompt="Plot Outliner task...")

INCORRECT (Sequential despite intention):
Message 1: Task(prompt="Character Designer task...")
Message 2: Task(prompt="World Builder task...")
Message 3: Task(prompt="Plot Outliner task...")
```

## Phase-by-Phase Detail

### Phase 1: Concept (Sequential)

**Why Sequential:** There's nothing to parallelize—story must be defined first.

**Agent:** Story Architect

**Output:** Story Architecture Document

---

### Phase 2: Foundation (Full Parallel)

**Agents (all launched together):**

1. **Character Designer**
   - Focus: Full character profiles
   - Input: Story Architecture
   - Output: Character Profiles

2. **World Builder**
   - Focus: Full world bible
   - Input: Story Architecture
   - Output: World Bible

3. **Plot Developer (Outline Mode)**
   - Focus: Rough structural outline only
   - Input: Story Architecture
   - Output: High-level beat sheet

**Execution:**

```markdown
Launch in single message:

Task(
    subagent_type="general-purpose",
    description="Design characters",
    prompt="You are the Character Designer. Using this Story Architecture: [doc], create complete character profiles..."
)

Task(
    subagent_type="general-purpose",
    description="Build world",
    prompt="You are the World Builder. Using this Story Architecture: [doc], create the world bible..."
)

Task(
    subagent_type="general-purpose",
    description="Outline plot",
    prompt="You are the Plot Developer in OUTLINE MODE. Using this Story Architecture: [doc], create a high-level beat sheet (NOT full scene breakdown yet)..."
)
```

**Synthesis Required:**
- Ensure characters fit the world
- Align character arcs with plot beats
- Resolve any contradictions
- Create unified foundation document

---

### Phase 3: Structure (Sequential)

**Why Sequential:** Integration point—detailed plot must incorporate characters AND world.

**Agent:** Plot Developer (Full Mode)

**Input:** Synthesized foundation (characters + world + outline)

**Output:** Complete, detailed plot outline with scene-level breakdown

---

### Phase 4: Writing (Maximum Parallel)

**Strategy: Batch by Position, Not Sequence**

Instead of writing Ch.1 → Ch.2 → Ch.3, write chapters that won't directly interfere:

**Batch 1: Act Openers**
- Chapter 1 (Act 1 opening)
- Chapter 4 (Act 2 opening)
- Chapter 7 (Act 3 opening)

*These chapters start fresh contexts and are less dependent on exact previous endings.*

**Batch 2: Act Developments**
- Chapter 2
- Chapter 5
- Chapter 8

**Batch 3: Act Closers**
- Chapter 3 (Act 1 climax)
- Chapter 6 (Midpoint)
- Chapter 9 (Climax/Resolution)

**Execution per Batch:**

```markdown
Launch in single message:

Task(
    subagent_type="general-purpose",
    description="Write Chapter 1",
    prompt="You are the Scene Writer. Write Chapter 1 using: [full context including plot outline, characters, world]. This is the story opening. Target: 3,000 words..."
)

Task(
    subagent_type="general-purpose",
    description="Write Chapter 4",
    prompt="You are the Scene Writer. Write Chapter 4 using: [full context]. This is Act 2 opening. The reader has experienced [Act 1 summary]. Target: 3,500 words..."
)

Task(
    subagent_type="general-purpose",
    description="Write Chapter 7",
    prompt="You are the Scene Writer. Write Chapter 7 using: [full context]. This is Act 3 opening. The reader has experienced [Acts 1-2 summary]. Target: 3,500 words..."
)
```

**Between Batches:**
1. Collect all chapters from batch
2. Synthesize: ensure consistency, adjust transitions
3. Update continuity bible
4. Provide updated context to next batch

**Parallel Support Streams:**
- Dialogue Specialist: Polish key exchanges as chapters complete
- Continuity Keeper: Track facts in real-time

---

### Phase 5: Polish (Full Parallel)

**Agents (all launched together):**

1. **Editor (Structural Focus)**
   - Assess overall structure, pacing, arc
   - Output: Structural notes

2. **Editor (Line Focus)**
   - Review prose quality, word-level issues
   - Output: Line editing notes

3. **Continuity Keeper**
   - Final consistency verification
   - Output: Continuity report

**Execution:**

```markdown
Launch in single message:

Task(
    subagent_type="general-purpose",
    description="Structural edit",
    prompt="You are the Editor focusing on STRUCTURE. Review this manuscript for: pacing, story arc, scene effectiveness, chapter transitions..."
)

Task(
    subagent_type="general-purpose",
    description="Line edit",
    prompt="You are the Editor focusing on LINE EDITING. Review this manuscript for: prose quality, word choice, dialogue, description..."
)

Task(
    subagent_type="general-purpose",
    description="Continuity check",
    prompt="You are the Continuity Keeper. Perform final verification of: timeline, character consistency, world facts, logic..."
)
```

**Synthesis:**
- Merge all feedback into prioritized revision plan
- Resolve any conflicting suggestions
- Execute revisions

---

## Time Comparison

| Phase | Sequential | Parallel | Savings |
|-------|------------|----------|---------|
| Concept | 30 min | 30 min | 0% |
| Foundation | 90 min | 35 min | ~60% |
| Structure | 45 min | 45 min | 0% |
| Writing (9 ch) | 180 min | 100 min | ~45% |
| Polish | 75 min | 30 min | ~60% |
| **TOTAL** | **420 min** | **240 min** | **~43%** |

*Includes synthesis time in parallel estimates.*

## Synthesis Strategies

### For Foundation Phase
- **Character-World Alignment:** Check that characters fit the world's rules and culture
- **Plot-Character Alignment:** Ensure plot outline uses character motivations
- **Terminology Unification:** Same names for same things across all docs

### For Writing Phase
- **Transition Smoothing:** Adjust chapter endings/beginnings to flow
- **Voice Consistency:** Ensure same narrative voice across parallel-written chapters
- **Continuity Integration:** Incorporate Continuity Keeper's flags

### For Polish Phase
- **Priority Matrix:** Rank issues by impact
- **Conflict Resolution:** If structural edit conflicts with line edit, structural wins
- **Triage:** Some issues can wait for final pass

## Risk Mitigation

### Risk: Inconsistency Between Parallel Outputs

**Mitigation:**
- Detailed Story Architecture reduces divergence
- Explicit synthesis step after each parallel phase
- Continuity Keeper running in parallel during writing

### Risk: Wasted Work from Early Divergence

**Mitigation:**
- Gate after Phase 1 ensures concept is locked
- Gate after Phase 2 catches foundation issues before writing
- Batch writing allows mid-course corrections

### Risk: Synthesis Takes Too Long

**Mitigation:**
- Use synthesis checklists (see templates)
- Focus on conflicts, not reviewing everything
- Accept minor inconsistencies for later polish

## When to Fall Back to Sequential

Switch mid-project if:
- Synthesis is finding major conflicts repeatedly
- Story vision is shifting significantly
- Quality is suffering for speed
- You're spending more time synthesizing than you're saving

## Quick Reference

```
/novella/orchestrator [Use parallel pattern]

CONCEPT (Sequential):
  Story Architect → Architecture Doc → [Gate]

FOUNDATION (Parallel Launch):
  Character Designer ─┐
  World Builder      ─┼─→ Synthesize → Foundation → [Gate]
  Plot Outliner      ─┘

STRUCTURE (Sequential):
  Plot Developer (full) → Detailed Outline → [Gate]

WRITING (Batch Parallel):
  Batch 1: Ch.1 + Ch.4 + Ch.7 → Synthesize
  Batch 2: Ch.2 + Ch.5 + Ch.8 → Synthesize
  Batch 3: Ch.3 + Ch.6 + Ch.9 → Synthesize
  [Gate: Draft Complete]

POLISH (Parallel Launch):
  Editor (Structure) ─┐
  Editor (Line)      ─┼─→ Synthesize → Revise → [Gate]
  Continuity Final   ─┘

→ COMPLETED NOVELLA
```

## Remember

Parallel is powerful but demanding. You're trading control for speed. The synthesis work is real work—factor it in.

The goal is a great story, not just a fast one. If parallel is creating problems, slow down. A finished novella written sequentially beats an inconsistent novella written in parallel.

Use this pattern when you know what you're doing and the story is clear in your mind. Speed follows clarity.
