# Upstream engineering case studies

[Back to profile](../README.md)

These are changes accepted into independent upstream repositories. Links include the original implementation, regression tests, discussion and merge record. Local test counts below describe the submitted regression suites, not a claim that every local full-suite attempt passed.

## Repowise: distinguish dispatch from nesting in seven languages

**Merged 2026-10-27** · [PR #4709](https://github.com/repowise-dev/repowise/pull/4709) · [Issue #3285](https://github.com/repowise-dev/repowise/issues/3285)

A dispatch such as `a ? 1 : (b ? 2 : (c ? 3 : 4))` was counted as nesting depth 3 and cognitive complexity 6. The correction treats its else-arm chain as flat: depth 1, cognitive complexity 3, with cyclomatic complexity still 4. Decisions inside the condition or consequence remain genuinely nested.

The patch extends the existing rule to Java, C, C++, C#, Dart, Objective-C and PHP, then increments the analyzer version so cached results are recomputed. Sixty new cases cover parentheses, lambdas, enclosing conditions and the user-visible health finding: **40 fail / 20 pass before**, **60 pass after**. The project member's approval explicitly highlights those parametrized distinctions as the safety argument for the seven-language change.

**What this demonstrates:** language-aware analysis, compatibility across syntax families, cache invalidation, and regression tests that protect both changed and unchanged behavior.

## Repowise: handle CSD input with no definitions

**Merged 2026-10-24** · [PR #4492](https://github.com/repowise-dev/repowise/pull/4492) · [Issue #4480](https://github.com/repowise-dev/repowise/issues/4480)

The parser paired discovered resources with their following boundaries using strict `zip`. It appended an end-of-file boundary even when there were no resources, so empty or comment-only files raised a length mismatch instead of producing an empty parse result.

The fix appends that boundary only when definitions exist. It preserves strict pairing and the line ranges for real resources. Seven regression cases cover empty, whitespace-only, comment-only, ALTER-only and skipped-resource inputs, plus single/multiple-definition controls: **5 fail / 2 pass before**, **7 pass after**.

**What this demonstrates:** a small root-cause correction with explicit controls, rather than suppressing an exception or weakening a parser invariant.

## nanobot: honor timeouts during model recovery and finalization

**Merged 2026-08-24 UTC** · [PR #5496](https://github.com/HKUDS/nanobot/pull/5496)

The normal model-request path honored the configured wall-clock timeout, but no-tools requests during recovery and finalization called the provider directly. A hung provider could keep the session lock occupied and block later messages.

The change shares timeout resolution across request paths and applies it to no-tools requests while preserving the structured error response. A regression simulates hung max-iteration finalization; the focused runner suite passed 223 tests. The upstream collaborator approved and merged the fix.

**What this demonstrates:** async lifecycle reasoning, bounded waiting and a regression that exercises the actual stalled-provider path.

## Verification and attribution

The PR pages are the source of truth for accepted code, review and merge state. Pending PRs are linked separately on the profile and are not presented as accepted work. AI assistance in implementation, tests and review is disclosed in the recent Repowise PR descriptions.
