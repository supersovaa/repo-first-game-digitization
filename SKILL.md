# repo-first-game-digitization

Digitize an analog game from official rules while keeping repository-local rule and design canons as the working sources of truth.

Apply this skill when an analog game's official rules are available on an official website and the project will maintain its own rule canon and design canon.

## Core model

Treat the official website as the source material, the rule canon as the project's complete game-rule reference, and the design canon as the record of how those rules become digital behavior.

Use the repository canons as the default sources during design and implementation.

Access official sources again for implementation-source capture as described below or when the user requests it. Apply official updates after the user instructs the project to update its canon.

## Build the rule canon

Rewrite and reorganize the adopted official rules into a readable, complete rule canon.

Make the adopted game understandable from the rule canon itself. Consolidate related rules, normalize terminology, and make conditions, exceptions, precedence, and interactions explicit where the source material establishes them.

Record links to the official materials used as sources.

Integrate adopted gameplay information from official FAQs into the rule canon according to its meaning, including rules, conditions, exceptions, interactions, and examples that appear only in the FAQ.

For FAQ-derived rulings, record the FAQ number. Add a direct link to the individual FAQ when one is available; otherwise link to the official FAQ source.

Treat the current official rules as incorporating published errata. Use errata history only when the user requests historical investigation.

## Preserve implementation source text

Before implementing a unit, item, or other game element whose behavior depends on official effect text, store the effect text needed for that implementation in the repository.

Store source text only for elements that enter the implementation scope. Record the official URL for each stored source.

Keep the stored official text distinct in meaning from implementation data. Let the repository choose the file format, placement, and whether both live in the same file.

Make each implementation data entry traceable to the stored official text that supports it.

Keep the stored source as tracked repository content after implementation completes.

During normal implementation work, use the repository-stored official text. When the user instructs the project to update its canon, refresh the stored official text for affected implemented elements from the current official source. Replace the repository's current copy when the official text changed and use Git history for earlier copies.

## Define digitization scope

Record the digital treatment of rules that fall outside the implementation scope, together with the reason.

Common scope exclusions include physical constraints that carry no game meaning, rules for expansions outside the project's adopted scope, and etiquette or table-management guidance.

Preserve any game meaning carried by a physical procedure. State, legal actions, victory conditions, ordering, randomness, hidden information, and other gameplay semantics remain part of the digital rules when the physical wording expresses them.

## Handle conflicts and gaps

When official sources conflict, prefer a digitization path that makes the conflicting choice irrelevant while preserving the adopted gameplay.

When a conflict still requires a choice, present the conflicting rulings and their sources to the user and use the user's decision.

When the official rules leave a required behavior unspecified, ask the user for the ruling and record the resulting decision in the appropriate canon.

Assume the user is familiar with the game and is the authority for these project-specific rulings.

## Build the design canon

Record the design decisions that make the adopted rules work as a digital game.

Relevant subjects can include game state, state transitions, legal operations, information visibility, randomness, automation, replacement of physical procedures, and digital realization of ambiguous or simultaneous behavior.

Keep implementation technology and presentation details in the design canon when they affect game meaning. Let the project choose the design granularity, document structure, and technical level appropriate to its conventions.

## Keep each meaning canonical

Give each rule, ruling, and design decision one canonical location.

Use references from other locations when that meaning is needed elsewhere. Structure the canons so a semantic change completes by editing its canonical location once.

Use examples to demonstrate application of a rule or design decision rather than to redefine it.

## Write binding examples

Let straightforward major rules stand on clear canonical prose.

Add binding examples where complex conditions, interacting rules, edge cases, or adjudication benefit from concrete outcomes.

Use only elements that actually exist in the game when constructing examples.

When multiple rules or conditions can apply together, include at least one example that establishes an adjudication for that combination.

Place rule-derived examples with the rule canon and design-derived examples with the design canon.

Treat canonical prose as authoritative when an example appears inconsistent. Let the user determine whether the apparent inconsistency is an actual contradiction, a separate condition, or an exception.

Update affected examples when a rule or design change changes their expected outcome.

## Do not require unrealizable examples

Do not require a binding example or executable test merely because a rule or design admits a theoretical branch.

When no concrete scenario can be constructed from the real game elements currently in implementation scope, do not require that case as current test evidence and do not introduce fictional elements, test-only effects, or otherwise unnecessary generic machinery solely to make the case testable.

Distinguish directly constructing an otherwise unreachable initial test state from inventing an interaction that the in-scope real game elements cannot produce.

When a plan intentionally omits a test for this reason, record that the current implementation scope has no realizable example. During review, independently inspect the in-scope real elements and confirm that no such example can actually be constructed. If one can be constructed, treat the omission as a test-plan gap.

When required behavior remains part of the implementation but no real in-scope elements can make that behavior observable, record the uncovered behavior as deferred formal coverage rather than treating the test omission as permanently satisfied. Record what behavior remains uncovered, why no realizable example exists, and the condition under which a real element would make it observable.

The originating implementation may complete with deferred formal coverage while that realization condition remains absent, provided all currently observable required behavior has the required test evidence.

Allow deferred formal coverage to remain unresolved for as long as the realization condition is absent. Do not introduce future elements, fictional elements, test-only effects, or otherwise unnecessary generic machinery solely to discharge it.

When a later in-scope real element makes the deferred case realizable, make that deferred coverage available to the planning and testing workflow so the case receives formal coverage at that point.

## Expose binding examples to testing

Treat binding examples from both canons as settled expected outcomes for the workflow responsible for testing.

Make each binding example clear enough that the applicable behavior can be checked without inventing additional rule or design decisions.

When implementation proceeds, make applicable binding examples available to the project's testing workflow.

Leave derivation of executable tests, test-level selection, test implementation, and test execution to the workflow responsible for testing.

Keep implementation behavior aligned with the rule canon, the design canon, and their binding examples.
