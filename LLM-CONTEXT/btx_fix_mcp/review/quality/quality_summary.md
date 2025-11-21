# Quality Analysis Report

## Reviewer Mindset

**You are a quality reviewer** - thorough, precise.

**Your approach:**
- ✓ **Verify:** Verify all claims with evidence

## Verdict

**❌ REJECTED**

- Critical issues: 11 (19.0%)
- Warnings: 183 (315.5%)
- Total items analyzed: 58

## Overview

**Files Analyzed**: 58 (58 Python, 0 JS/TS)
**Functions Analyzed**: 496
**Total Issues Found**: 238
**Critical Issues**: 11

## Code Metrics

- Total LOC: **11,976**
- Source LOC (SLOC): **7,702**
- Comments: **443**
- Comment Ratio: **5.8%**

## Quality Issues Summary

- Functions >50 lines: **34**
- High cyclomatic complexity (>10): **30**
- High cognitive complexity (>15): **25**
- Functions with nesting >3: **36**
- Code duplication blocks: **62**
- God objects: **2**
- Highly coupled modules: **1**
- Import cycles: **0**
- Dead code items: **1**

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

- Status: **✅ Passed**

## Critical Issues (Must Fix)

- 🔴 `src/btx_fix_mcp/subservers/review/deps.py`: Function '_generate_summary' has complexity 21 (threshold: 10)
- 🔴 `src/btx_fix_mcp/subservers/review/quality/__init__.py`: Function 'execute' has complexity 34 (threshold: 10)
- 🔴 `src/btx_fix_mcp/subservers/review/quality/__init__.py`: Function '_run_analyzers_parallel' has complexity 21 (threshold: 10)
- 🔴 `src/btx_fix_mcp/subservers/review/quality/metrics.py`: Function '_analyze_code_churn' has complexity 21 (threshold: 10)
- 🔴 `src/btx_fix_mcp/subservers/review/quality/__init__.py`: Function '_run_analyzers_parallel' is 112 lines (max: 50)
- 🔴 `src/btx_fix_mcp/subservers/review/quality/__init__.py`: Function 'execute' is 139 lines (max: 50)
- 🔴 `src/btx_fix_mcp/subservers/review/quality/metrics.py`: Function '_analyze_code_churn' is 122 lines (max: 50)
- 🔴 `src/btx_fix_mcp/subservers/review/report.py`: Function '_generate_report' is 109 lines (max: 50)
- 🔴 `src/btx_fix_mcp/subservers/review/security.py`: Function '_generate_summary' is 116 lines (max: 50)
- 🔴 `src/btx_fix_mcp/subservers/review/deps.py`: Class 'DepsSubServer' is a god object (13 methods, 503 lines)
- 🔴 `src/btx_fix_mcp/subservers/review/quality/__init__.py`: Class 'QualitySubServer' is a god object (41 methods, 717 lines)

## Refactoring Recommendations

1. **Break Down Long Functions**: 34 functions exceed 50 lines
2. **Reduce Cyclomatic Complexity**: 30 functions exceed threshold
3. **Reduce Cognitive Complexity**: 25 functions are too complex
4. **Extract Duplicated Code**: 62 duplicate blocks found
5. **Refactor God Objects**: 2 classes need decomposition
6. **Add Type Annotations**: Coverage is 0%
7. **Add Docstrings**: Coverage is 0.0%
8. **Remove Dead Code**: 1 unused items found

## Approval Status

**❌ REJECTED**

- Address critical issues before merging
- Ask yourself: Is this correct? Let me check.