# Changelog

All notable changes to this project will be documented in this file following
the [Keep a Changelog](https://keepachangelog.com/) format.

## [Unreleased]

## [1.0.0] - 2025-11-27

### Added
- Centralized configuration in `pyproject.toml`:
  - `[tool.clean]` section for clean patterns
  - `[tool.git]` section for default git remote
  - `[tool.scripts.test]` section for test runner settings (pytest-verbosity, coverage-report-file, src-path)
- Windows compatibility: All Unicode symbols replaced with ASCII equivalents
- Regex-based vulture output parsing to handle Windows paths with drive letters

### Changed
- **BREAKING**: Minimum Python version is now 3.13 (previously 3.9)
- Updated all dependencies to latest stable versions
- Modernized type hints to use Python 3.13+ syntax (`X | None` instead of `Optional[X]`)
- CI/CD now tests on Python 3.13, 3.14, and latest (3.x)
- Refactored `scripts/*.py` to reduce cyclomatic complexity (all functions now A/B grade)
- Moved `profile_application.py` to `src/btx_fix_mcp/scripts/` for proper packaging
- README badges now point to correct repository (btx_fix_mcp)

### Removed
- Dropped support for Python 3.9, 3.10, 3.11, and 3.12
- Removed `tomli` fallback (tomllib is built-in for Python 3.11+)
- Removed `typing.Optional` imports throughout codebase
- Removed all Unicode symbols (emojis, checkmarks, arrows) for Windows compatibility

### Fixed
- Windows encoding errors (`charmap` codec failures) by replacing Unicode with ASCII
- Windows path parsing in vulture dead code detection
- Windows `Path.home()` test failure when environment variables are cleared

## [0.1.0] - 2025-11-04
- Bootstrap `btx_fix_mcp`
