Use `AGENTS.md` in the repository root as the primary source of guidance for this codebase.

Key points:
- Prefer concise, targeted edits and link to existing docs instead of copying large sections.
- Use `scripts/run_tests.sh` for validation; avoid running `pytest` directly unless explicitly requested.
- Preserve profile safety by using `get_hermes_home()` for internal state paths and `display_hermes_home()` for user-facing paths.
- Tool implementations belong in `tools/*.py`; CLI command definitions live in `hermes_cli/commands.py` and dispatch in `cli.py`.
- For UI work, extend `ui-tui`/Ink rather than rewriting the main terminal chat flow in React.
