# retide-hq

Opinionated log housekeeping tool with dry-run support

Started as a weekend hack, grew on me.

## Highlights

- Archive matched logs into a timestamped .tar.gz
- Filter by age (--older-than) or size (--larger-than)
- Scan directories for log files by glob pattern
- Exit codes friendly for cron and CI
- Dry-run mode shows what would happen, touches nothing

## Examples

```bash
# show what would be cleaned, change nothing
logwash ./logs --older-than 30 --dry-run

# archive logs older than 30 days
logwash ./logs --older-than 30 --archive ./backup
```

## Installation

```bash
pip install -r requirements.txt
python -m logwash --help
```

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── configuration.md
│   ├── faq.md
│   ├── roadmap.md
│   └── usage.md
├── logwash/
│   ├── __init__.py
│   ├── __main__.py
│   ├── cli.py
│   ├── errors.py
│   └── utils.py
├── tests/
│   └── test_cli.py
├── .editorconfig
├── .gitignore
├── CODE_OF_CONDUCT.md
├── LICENSE
├── SECURITY.md
├── pyproject.toml
└── requirements.txt
```

## 说明

个人练习项目, 谨慎用于生产环境。

## License

MIT - see [LICENSE](LICENSE).
