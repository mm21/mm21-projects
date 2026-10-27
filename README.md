# mm21-projects

Maintenance hub for my Python projects. Each project is a sibling git repo in the parent folder (`../<name>`) and is managed by [pyprojkit](https://github.com/mm21/pyprojkit) via its `pyprojconf.py`, `dodo.py` and `noxfile.py`.

## Managed projects

<!-- the manage-projects skill reads this table: keep one row per repo, with the repo folder name in the first column -->

| Project | Description |
| --- | --- |
| [clipsmith](https://github.com/mm21/clipsmith) | Utility to work with video clips, especially suited for creating timelapses from dashcam footage |
| [docfmt](https://github.com/mm21/docfmt) | Reliable docstring formatter: AST-located, surgically spliced, self-verifying |
| [filesentinel](https://github.com/mm21/filesentinel) | Integrity monitoring and repair toolkit for long-term file archives |
| [glyphsynth](https://github.com/mm21/glyphsynth) | Pythonic vector graphics synthesis toolkit |
| [mdforge](https://github.com/mm21/mdforge) | Pythonic multi-flavor Markdown generator |
| [pyprojkit](https://github.com/mm21/pyprojkit) | Development workflow toolkit for Python projects: pyproject.toml sync, doit tasks, nox sessions |
| [sphinx-better-fieldlist](https://github.com/mm21/sphinx-better-fieldlist) | Renders Sphinx field lists as definition lists
| [trilium-alchemy](https://github.com/mm21/trilium-alchemy) | Python SDK and CLI toolkit for Trilium Notes |
| [typecraft](https://github.com/mm21/typecraft) | Annotation-native toolkit for type inspection, validation, and data modeling |

## Maintenance workflow

Open Claude Code in this repo and describe the change, for example:

> bump pyprojkit to 0.9.0 and set `python_version_file=True` in pyprojconf.py

The [`manage-projects`](.claude/skills/manage-projects/SKILL.md) skill then:

1. Makes the change in every managed repo
2. Runs `uv run doit preflight` in each repo and summarizes the results, flagging unexpected changes (e.g. unrelated reformatting)
3. Suggests a one-line conventional commit message and offers to commit, and optionally push to `origin`

To add or remove a project, edit the table above.
