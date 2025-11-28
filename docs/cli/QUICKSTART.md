# CLI Quickstart

Get started with btx_fix_mcp command-line interface in 5 minutes.

## Installation

```bash
# Quick install
pip install btx_fix_mcp

# Or with uv (faster)
uv pip install btx_fix_mcp
```

## Basic Usage

### Review Uncommitted Git Changes (Default)

```bash
# Go to your project
cd /path/to/your/project

# Review uncommitted changes
python -m btx_fix_mcp review all
```

Output is saved to `LLM-CONTEXT/btx_fix_mcp/review/`.

> **Note**: If your project is not a git repository, `--mode git` automatically falls back to `--mode full` with a warning.

### Review All Files

```bash
python -m btx_fix_mcp review all --mode full
```

### Run Specific Analyses

```bash
# Quality analysis only
python -m btx_fix_mcp review quality

# Security scan only
python -m btx_fix_mcp review security

# Cache optimization analysis
python -m btx_fix_mcp review cache
```

## Output Location

All results are saved to:

```
your-project/
└── LLM-CONTEXT/
    └── btx_fix_mcp/
        └── review/
            ├── scope/          # Files analyzed
            ├── quality/        # Quality metrics
            ├── security/       # Security issues
            ├── deps/           # Dependency analysis
            ├── docs/           # Documentation coverage
            ├── perf/           # Performance analysis
            ├── cache/          # Cache recommendations
            └── report/         # Final summary
```

## Common Workflows

### CI/CD Integration

```bash
# In your CI pipeline
python -m btx_fix_mcp review all --mode full

# Check exit code for failures
if [ $? -ne 0 ]; then
    echo "Code review found issues"
    exit 1
fi
```

### Pre-commit Hook

```bash
# Review only staged changes
python -m btx_fix_mcp review all --mode git
```

### Cache Optimization

```bash
# Profile your tests first
python -m btx_fix_mcp review profile -- pytest tests/

# Then analyze cache opportunities
python -m btx_fix_mcp review cache
```

### Clean Up Old Results

```bash
# Delete all review data
python -m btx_fix_mcp review clean

# Delete specific analysis
python -m btx_fix_mcp review clean -s quality
python -m btx_fix_mcp review clean -s profile

# Preview what would be deleted
python -m btx_fix_mcp review clean --dry-run
```

## Quick Reference

| Command | Options | Defaults |
|---------|---------|----------|
| `review all` | `--mode`, `--complexity`, `--severity` | mode=`git`, complexity=`10`, severity=`low` |
| `review scope` | `--mode` | mode=`git` |
| `review quality` | `--complexity`, `--maintainability` | complexity=`10`, maintainability=`20` |
| `review security` | `--severity`, `--confidence` | severity=`low`, confidence=`low` |
| `review deps` | `--no-vulnerabilities`, `--no-licenses`, `--no-outdated` | all checks enabled |
| `review docs` | `--min-coverage`, `--style` | min-coverage=`80`, style=`google` |
| `review perf` | `--no-profiling`, `--nested-loop-threshold` | profiling enabled, threshold=`2` |
| `review cache` | `--cache-size`, `--hit-rate-threshold`, `--speedup-threshold` | size=`128`, hit-rate=`20.0`, speedup=`5.0` |
| `review profile -- CMD` | (none) | CMD is **required** |
| `review clean` | `-s/--subserver`, `--dry-run` | subserver=`all`, dry-run=`false` |
| `review report` | (none) | - |

> **All options are optional** unless marked as required. See [CLI Reference](REFERENCE.md) for detailed documentation.

## Next Steps

- [CLI Reference](REFERENCE.md) - All commands and options
- [Configuration](../reference/CONFIGURATION.md) - Customize thresholds
- [Cache Profiling](../CACHE_SUBSERVER.md) - LRU cache optimization guide
