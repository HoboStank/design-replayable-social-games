# Worked example: Shared Repair

**Fictional design exercise. No project files, player sessions, or analytics were inspected. All design opportunities below are hypotheses.**

## Brief

A small browser game about fixing odd machines with a friend. Intended for adults on laptops, with mouse and keyboard controls and short, self-contained repair jobs. A two-person team has one week for a prototype change.

**Core promise:** figure out a broken machine, make a useful contribution, and watch it come back to life together.

Assumed current loop: take a tool → click damaged parts → finish the job. Players can act simultaneously, but one player's choices rarely affect the other's. These are invented constraints for the example, not findings about a real game.

## Prioritized opportunities

1. **Make contributions complementary.** Hypothesis: a repair that benefits from two different actions gives players a reason to coordinate. High potential value; low evidence confidence. Medium implementation cost; risk of one player becoming a passive assistant. Depends on shared machine state and reliable input feedback.
2. **Make the result legible.** Hypothesis: a clear before/after animation helps players understand what their actions accomplished. Medium potential value; low confidence. Low-to-medium cost; depends on available art and sound. Avoid obscuring controls or relying on color alone.
3. **Let players choose a repair style.** Hypothesis: choosing a functional part with a visible tradeoff makes a machine feel more personal. Medium potential value; low confidence. Higher cost because it needs balancing and saved state. Defer until the repair itself works.

## Recommended slice: stabilize and tune

Add one machine with two visible interactions:

- One player stabilizes a moving component; the other tunes its alignment
- Either player can take either role and swap without losing progress
- Stabilization involves readable timing choices rather than holding a button indefinitely
- A visible clamp allows solo play: stabilize, lock the clamp, then tune
- If someone leaves, the remaining player can use the clamp and finish

Before: players perform parallel clicks that do not change each other's decisions.

After: one player's timing creates an easier tuning opportunity for the other. Solo players use the same underlying interactions in sequence.

**Excluded:** progression trees, currencies, friend bonuses, public matchmaking, cosmetics, persistent saves, and additional machine types. Do not require players to recruit a friend to test the core loop.

### First-session sequence

1. Arrive at a visibly broken machine with one clear interaction prompt
2. Try stabilization and see the component become easier to align
3. Notice the tuning control and the clamp through labels and motion, not color alone
4. Choose a role with a partner, or engage the clamp when alone
5. Complete the repair; see the machine run and each contribution acknowledged
6. Choose another attempt, swap roles, or leave at a clean stopping point

## Playtest plan

Run a small qualitative pilot with consenting adults who have not seen the prototype. Test both paired and solo play on the target laptop/browser combinations. Record the participant count and every attempt; do not present this pilot as a retention study.

- **Hypothesis:** complementary actions help new players explain their own contribution and their partner's contribution without making either role feel like waiting
- **Comparison:** use the original parallel-click job and the revised job. Alternate their order across pairs where feasible, and note learning effects
- **Observation window:** one job in each version, followed by an optional unprompted repeat. If feasible, offer an optional return session after at least a day; report who was invited and who returned
- **Observe:** first useful action, requests for facilitator help, role changes, inactive waiting, use of the solo fallback, completion, and the choice to repeat or stop
- **Ask after play:** “What did each person do that changed the repair?” and “Was there a point where you wanted to do something but couldn't?”
- **Report:** counts with denominators, short anonymized observations, device issues, and contradictory cases. Ask permission before recording; collect no unnecessary personal information

### Acceptance checklist

These are provisional design checks, not industry benchmarks or statistical proof.

- [ ] New players can identify a useful first action without a verbal walkthrough
- [ ] Each partner can describe how the other affected the repair
- [ ] Both roles contain meaningful choices; neither is mostly waiting
- [ ] Solo completion and recovery after a partner leaves both work
- [ ] Contributions and completion are readable without color-only cues
- [ ] Controls, join behavior, and frame pacing are checked on target devices
- [ ] A player can finish and leave without a loss penalty or pressure to return

### Keep, revise, or stop

- **Keep for further testing** if the contribution is consistently understandable across observed sessions, both roles feel active, and solo/dropout paths work. Seek repeat voluntary play before making replay-value claims
- **Revise** if the idea is understood but one role feels subordinate, coordination is unclear, or controls create avoidable friction
- **Stop or revert** if the mechanic adds frustration without useful cooperation, or a reliable solo/dropout path exceeds the team's available scope

Do not infer causality from a handful of sessions. An optional repeat is a clue, not proof of lasting replay value.

## Open dependencies

Confirm the actual network model, accessibility needs, target devices, art budget, and existing input/state systems before estimating or implementing. The user must authorize implementation separately.
