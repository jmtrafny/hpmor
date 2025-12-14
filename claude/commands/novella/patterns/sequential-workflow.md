# Sequential Workflow Pattern for Novella Writing

The classic, linear approach to creative writing. Each phase completes before the next begins. Simple, clear, and maximally controlled.

## Pattern Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                  NOVELLA SEQUENTIAL WORKFLOW                    │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌─────────────────────┐                                        │
│  │   Story Architect   │ → Story Architecture                   │
│  └──────────┬──────────┘                                        │
│             │ [Human Gate]                                      │
│             ▼                                                   │
│  ┌─────────────────────┐                                        │
│  │ Character Designer  │ → Character Profiles                   │
│  └──────────┬──────────┘                                        │
│             │ [Human Gate]                                      │
│             ▼                                                   │
│  ┌─────────────────────┐                                        │
│  │    World Builder    │ → World Bible                          │
│  └──────────┬──────────┘                                        │
│             │ [Human Gate]                                      │
│             ▼                                                   │
│  ┌─────────────────────┐                                        │
│  │   Plot Developer    │ → Plot Outline                         │
│  └──────────┬──────────┘                                        │
│             │ [Human Gate]                                      │
│             ▼                                                   │
│  ┌─────────────────────┐                                        │
│  │    Scene Writer     │ → Draft Chapters (one at a time)       │
│  └──────────┬──────────┘                                        │
│             │ [Human Gates per Act]                             │
│             ▼                                                   │
│  ┌─────────────────────┐                                        │
│  │      Editor         │ → Editorial Report                     │
│  └──────────┬──────────┘                                        │
│             │ [Human Gate]                                      │
│             ▼                                                   │
│  ┌─────────────────────┐                                        │
│  │  Continuity Keeper  │ → Consistency Verification             │
│  └──────────┬──────────┘                                        │
│             │ [Human Gate]                                      │
│             ▼                                                   │
│  ╔═════════════════════════════════════════════════════════╗    │
│  ║               COMPLETED NOVELLA                         ║    │
│  ╚═════════════════════════════════════════════════════════╝    │
└─────────────────────────────────────────────────────────────────┘
```

## Why Choose Sequential?

### Best For:
- **First-time users** - Learn the system step by step
- **Complex stories** - High interdependence between elements
- **Experimental work** - Unknown territory, need tight control
- **Teaching/Learning** - Understanding each phase clearly
- **Maximum quality control** - Every step reviewed before proceeding

### Trade-offs:
- ✅ Simple to understand and manage
- ✅ Maximum human control at each step
- ✅ Easy to course-correct
- ✅ Clear progress tracking
- ❌ Slower than parallel approaches
- ❌ Each phase waits for previous completion

## Phase-by-Phase Detail

### Phase 1: Story Architecture

**Agent:** Story Architect

**Input:** User's initial concept, genre preferences, constraints

**Process:**
1. Invoke Story Architect with concept
2. Review Story Architecture Document
3. Provide feedback if needed
4. Approve to continue

**Output:**
- Premise and logline
- Theme definitions
- Structural approach
- Scope parameters

**Human Gate Questions:**
- Does this capture the story you want to tell?
- Are the themes meaningful to you?
- Is the scope appropriate?

---

### Phase 2: Character Development

**Agent:** Character Designer

**Input:** Approved Story Architecture

**Process:**
1. Invoke Character Designer with architecture
2. Review all character profiles
3. Request revisions if needed
4. Approve to continue

**Output:**
- Protagonist profile (detailed)
- Supporting character profiles
- Antagonist/opposition profile
- Relationship map
- Voice guides

**Human Gate Questions:**
- Do characters feel alive and distinct?
- Are motivations clear and compelling?
- Do relationships create interesting dynamics?
- Is the cast appropriately sized?

---

### Phase 3: World Building

**Agent:** World Builder

**Input:** Approved Story Architecture + Character Profiles

**Process:**
1. Invoke World Builder with all prior context
2. Review World Bible
3. Request revisions if needed
4. Approve to continue

**Output:**
- Setting descriptions
- Social/cultural context
- Rules and logic
- Atmosphere guide
- Location details

**Human Gate Questions:**
- Does the world serve the story?
- Do settings feel vivid and real?
- Are rules consistent?
- Does atmosphere match intended tone?

---

### Phase 4: Plot Development

**Agent:** Plot Developer

**Input:** All approved foundation documents

**Process:**
1. Invoke Plot Developer with complete foundation
2. Review detailed plot outline
3. Request structural changes if needed
4. Approve to continue

**Output:**
- Chapter breakdown
- Scene-by-scene detail
- Tension map
- Information revelation schedule
- Character arc integration

**Human Gate Questions:**
- Does the plot serve the themes?
- Is pacing appropriate?
- Are character arcs integrated?
- Does the ending feel inevitable yet surprising?

---

### Phase 5: Writing (Chapter by Chapter)

**Agent:** Scene Writer (with Dialogue Specialist as needed)

**Input:** Complete foundation + plot outline

**Process (per chapter):**
1. Invoke Scene Writer for Chapter N
2. Review draft chapter
3. Invoke Dialogue Specialist if dialogue needs work
4. Approve chapter before proceeding to N+1

**Sub-gates:**
- After Act 1 (opening chapters): Full review
- After Midpoint: Full review
- After Act 3: Draft complete review

**Output:**
- Draft manuscript (chapter by chapter)
- Updated continuity notes

**Human Gate Questions (per act):**
- Does the prose match the intended voice?
- Is pacing working?
- Does dialogue sound authentic?
- Any scenes that don't work?

---

### Phase 6: Editorial Review

**Agent:** Editor

**Input:** Complete draft manuscript

**Process:**
1. Invoke Editor for full manuscript review
2. Review Editorial Report
3. Prioritize revisions
4. Execute revisions (may re-invoke Scene Writer)
5. Approve when satisfied

**Output:**
- Structural notes
- Line-level suggestions
- Priority revision list
- Revised manuscript

**Human Gate Questions:**
- Do you agree with editorial assessment?
- Are priority issues addressed?
- Is revision scope appropriate?

---

### Phase 7: Continuity Verification

**Agent:** Continuity Keeper

**Input:** Revised manuscript + all story documents

**Process:**
1. Invoke Continuity Keeper for final check
2. Review Continuity Report
3. Address any remaining issues
4. Final approval

**Output:**
- Continuity verification
- Final issue list (if any)
- Updated story bible

**Human Gate Questions:**
- Are all continuity issues resolved?
- Is the story internally consistent?
- Ready to call it complete?

---

## Execution Template

```markdown
# Novella Project: [Title]
## Sequential Workflow Execution

### Current Status
- **Phase:** [1-7]
- **Agent:** [Current agent]
- **Status:** [In progress / Awaiting approval / Complete]

### Completed Phases
- [x] Phase 1: Story Architecture ✓
  - Approved: [Date]
  - Documents: story-architecture.md
- [ ] Phase 2: Character Development
- [ ] Phase 3: World Building
- [ ] Phase 4: Plot Development
- [ ] Phase 5: Writing
- [ ] Phase 6: Editorial Review
- [ ] Phase 7: Continuity Check

### Current Phase Details
[Details of current work]

### Next Steps
[What happens after current phase completes]
```

## Time Estimates

| Phase | Estimated Time | Cumulative |
|-------|----------------|------------|
| Story Architecture | 30 min | 30 min |
| Character Design | 45 min | 1h 15m |
| World Building | 45 min | 2h |
| Plot Development | 60 min | 3h |
| Writing (10 chapters) | 200 min | 6h 20m |
| Editorial Review | 45 min | 7h 5m |
| Continuity Check | 30 min | 7h 35m |
| **TOTAL** | **~7.5 hours** | |

*Note: These are active agent time estimates. Calendar time will be longer due to human review gates.*

## Handling Issues

### If a Phase Needs Major Revision

1. Accept that earlier work may need updating
2. Complete revision in current phase
3. Assess impact on completed phases
4. Re-run affected phases if necessary
5. Document changes

### If You Want to Go Back

The sequential pattern allows easy backtracking:

1. Identify the phase that needs change
2. Make the change
3. Re-run all subsequent phases with updated input
4. This ensures consistency cascades forward

### If Time Is Limited

Consider switching to Hybrid pattern, or:
1. Complete through Plot Development fully
2. Write Act 1 only
3. Pause project with clear documentation
4. Resume later with all context preserved

## Quick Reference

```
/novella/orchestrator [Use sequential pattern]

1. STORY ARCHITECT    → Architecture Doc  → [Gate]
2. CHARACTER DESIGNER → Character Profiles → [Gate]
3. WORLD BUILDER      → World Bible        → [Gate]
4. PLOT DEVELOPER     → Plot Outline       → [Gate]
5. SCENE WRITER       → Draft Chapters     → [Gates per Act]
6. EDITOR             → Editorial Report   → [Gate]
7. CONTINUITY KEEPER  → Verification       → [Gate]
                                              ↓
                                    COMPLETED NOVELLA
```

## When to Switch Patterns

Consider switching to **Hybrid** if:
- Project is going smoothly
- You want to speed up
- Foundation phases are solid

Consider switching to **Iterative** if:
- You're a discovery writer
- Major inspiration strikes mid-project
- You want to write before fully planning

## Remember

Sequential is the safest, most controlled approach. Every step builds on approved work. Nothing proceeds without human sign-off.

It's slower, but it's thorough. For learning the system or for complex projects where you need maximum control, sequential is the right choice.

Trust the process. One step at a time.
