# User Preferences

- Record durable user corrections and workflow preferences here as short actionable bullets.
- For skill authoring, write frontmatter descriptions for LLM pickup: focus on capability, outputs, triggers, and task context, not implementation details.
- For skill authoring, keep `SKILL.md` minimal and move tool usage details into `references/` files; document tool usage, not tool internals.
- For skill updates that rename the skill, rename the skill folder too, and split mode-specific instructions into dedicated reference files.
- For scene/video tests, do not mock `capture_image`, `record_screen`, or similar HTML/CSS rendering paths when the goal is to verify the real rendered output.
- For Explore worktree creation, stash local changes before `git worktree add`, apply the stash in both the new worktree and the original repo, drop the stash afterward, and create a `config/.env` symlink in the new worktree that points to the original repo env file.
- Always use the `git-github` agent skill when committing - never use a raw `git commit` bash command directly.
- For frozen feature files under `core/features/`, use natural English feature-phrase filenames developers would use during the lifecycle; keep extra keywords and synonyms inside the file content instead of stuffing them into the filename.
- For Explore showcase prompts, when details are already defined in a referenced requirements/update/issues file, keep the `prompt` concise and do not repeat those details.
- For Explore showcase requirement briefs, do not include generic agent-safety reminders such as prompt-injection warnings; those belong in the relevant agent skill behavior, not in user-authored requirements.
- For Explore showcase runtime deliverables such as `output.md` or user manuals, name the required file in the requirements/prompt but do not provide a prefilled template unless explicitly requested.
- For serial Explore showcases, do not write "previous task" as the dependency reference; state what has already been set up and give the exact copied destination file path, because the runtime AI may not have prior task memory.
