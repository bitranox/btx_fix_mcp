# Performance Analysis Report

## Reviewer Mindset

**You are a perf reviewer** - thorough, precise.

**Your approach:**
- ✓ **Verify:** Verify all claims with evidence

## Verdict

**🔧 NEEDS WORK**

- Critical issues: 2
- Warnings: 46
- Files analyzed: 58

## Overview

**Files Analyzed**: 58
**Pattern Issues**: 8
**Performance Hotspots**: 5
**Total Issues**: 48

## Performance Hotspots

- **tests/subservers/review/test_deps.py::TestDepsSubServer::test_execute_python_project**: 6.49s
- **tests/subservers/review/test_deps.py::TestDepsSubServer::test_summary_includes_mindset**: 5.97s
- **tests/servers/test_review.py::TestReviewMCPServer::test_run_all**: 1.25s
- **tests/servers/test_review.py::TestReviewMCPServer::test_run_quality**: 1.25s
- **tests/subservers/review/test_quality.py::TestQualitySubServer::test_execute_with_simple_code**: 1.08s

## Anti-Pattern Detections

- `/media/srv-main-softdev/projects/MCP/btx_fix_mcp/scripts/clean.py:34` - Nested loop detected
- `/media/srv-main-softdev/projects/MCP/btx_fix_mcp/src/btx_fix_mcp/subservers/review/deps_scanners.py:47` - Nested loop detected
- `/media/srv-main-softdev/projects/MCP/btx_fix_mcp/src/btx_fix_mcp/subservers/review/perf.py:224` - Nested loop detected
- `/media/srv-main-softdev/projects/MCP/btx_fix_mcp/src/btx_fix_mcp/subservers/review/perf.py:240` - Using range(len()) - consider enumerate() or direct iteration
- `/media/srv-main-softdev/projects/MCP/btx_fix_mcp/src/btx_fix_mcp/subservers/review/quality/__init__.py:574` - Nested loop detected
- `/media/srv-main-softdev/projects/MCP/btx_fix_mcp/src/btx_fix_mcp/subservers/review/quality/complexity.py:54` - Nested loop detected
- `/media/srv-main-softdev/projects/MCP/btx_fix_mcp/src/btx_fix_mcp/subservers/review/report.py:379` - Nested loop detected
- `/media/srv-main-softdev/projects/MCP/btx_fix_mcp/src/btx_fix_mcp/subservers/review/report.py:434` - Nested loop detected

## Approval Status

**🔧 NEEDS WORK**

- Address critical issues before merging
- Ask yourself: Is this correct? Let me check.