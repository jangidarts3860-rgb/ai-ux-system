# Systematic Debugging Principles

Use this file as a reference for investigating bugs, test failures, or unexpected UI behaviors.

## The Iron Law of Debugging
Seek the root cause before attempting fixes. Symptom fixes often create new bugs.

## Recommended Debugging Phases

### Phase 1: Root Cause Investigation
Before proposing a fix, consider:
1. **Read Error Messages Carefully**: Read stack traces completely, noting file paths and error codes.
2. **Reproduce Consistently**: Identify the exact steps to trigger the bug. If it's not reproducible, gather more data.
3. **Check Recent Changes**: Git diffs, new dependencies, and config changes are prime suspects.
4. **Gather Evidence**: Trace the broken flow end-to-end.

### Phase 2: Pattern Analysis
1. Find working examples in the same codebase.
2. Compare the broken code against reference implementations.
3. Identify differences, however small.

### Phase 3: Hypothesis and Testing
1. Form a single, specific hypothesis.
2. Make the smallest possible change to test the hypothesis.
3. Verify if the change worked before continuing.

### Phase 4: Implementation
1. Create a failing test case if possible.
2. Implement a single fix addressing the root cause.
3. Verify the fix against the test case and confirm no side effects.

## Final Rule

Diagnose the root cause before patching.
