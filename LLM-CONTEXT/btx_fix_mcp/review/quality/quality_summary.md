# Quality Analysis Report

## Reviewer Mindset

**You are a quality reviewer** - thorough, precise.

**Your approach:**
- ✓ **Verify:** Verify all claims with evidence

## Verdict

**❌ REJECTED**

- Critical issues: 6 (14.0%)
- Warnings: 74 (172.1%)
- Total items analyzed: 43

## Overview

**Files Analyzed**: 43 (43 Python, 0 JS/TS)
**Functions Analyzed**: 481
**Total Issues Found**: 107
**Critical Issues**: 6

## Code Metrics

- Total LOC: **11,211**
- Source LOC (SLOC): **6,833**
- Comments: **342**
- Comment Ratio: **5.0%**

## Quality Issues Summary

- Functions >50 lines: **21**
- High cyclomatic complexity (>10): **6**
- High cognitive complexity (>15): **5**
- Functions with nesting >3: **12**
- Code duplication blocks: **28**
- God objects: **5**
- Highly coupled modules: **0**
- Import cycles: **0**
- Dead code items: **0**

## Coverage Metrics

- Type coverage: **0%** (minimum: 80%)
- Docstring coverage: **0.0%** (minimum: 80%)

## Test Suite Analysis

- Total tests: **0**
- Total assertions: **0**
- Assertions per test: **0**
- Unit tests: 0
- Integration tests: 0
- E2E tests: 0
- Test issues: **0**

## Runtime Type Checking (Beartype)

- Status: **❌ Failed**

## Critical Issues (Must Fix)

- 🔴 `src/btx_fix_mcp/subservers/review/deps.py`: Class 'DepsSubServer' is a god object (27 methods, 623 lines)
- 🔴 `src/btx_fix_mcp/subservers/review/docs.py`: Class 'DocsSubServer' is a god object (27 methods, 655 lines)
- 🔴 `src/btx_fix_mcp/subservers/review/perf.py`: Class 'PerfSubServer' is a god object (19 methods, 526 lines)
- 🔴 `src/btx_fix_mcp/subservers/review/quality/architecture.py`: Class 'ArchitectureAnalyzer' is a god object (22 methods, 303 lines)
- 🔴 `src/btx_fix_mcp/subservers/review/security.py`: Class 'SecuritySubServer' is a god object (25 methods, 606 lines)
- 🔴 : Test run timed out

## Refactoring Recommendations

1. **Break Down Long Functions**: 21 functions exceed 50 lines
2. **Reduce Cyclomatic Complexity**: 6 functions exceed threshold
3. **Reduce Cognitive Complexity**: 5 functions are too complex
4. **Extract Duplicated Code**: 28 duplicate blocks found
5. **Refactor God Objects**: 5 classes need decomposition
6. **Add Type Annotations**: Coverage is 0%
7. **Add Docstrings**: Coverage is 0.0%

## Approval Status

**❌ REJECTED**

- Address critical issues before merging
- Ask yourself: Is this correct? Let me check.