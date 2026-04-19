# Skill Pilot Workspace

This folder is a Git submodule of the [Skill Pilot](https://github.com/X-School-Academy/skill-pilot) project, pointing to the sample repository:

> **https://github.com/X-School-Academy/skill-pilot_workspace.git**

It serves as the working area where Skill Pilot saves and organizes your projects, drafts, and outputs.

## Replacing with Your Own Private Repo

This sample workspace is meant to be replaced with your own private GitHub repository. To do so:

1. Create a new **empty** private GitHub repository (e.g., `https://github.com/<you>/my-workspace.git`).

2. Inside the `workspace/` folder, change the remote origin to your new repo and push the existing content:

```bash
cd workspace

# Point to your private repo
git remote set-url origin https://github.com/<you>/my-workspace.git

# Push the sample structure to your private repo
git push -u origin main
```

3. Update the submodule URL in your Skill Pilot fork so it tracks your private repo going forward:

```bash
cd ..  # back to skill-pilot root

# Update .gitmodules to point to your private repo
git config -f .gitmodules submodule.workspace.url https://github.com/<you>/my-workspace.git
git submodule sync
git add .gitmodules
git commit -m "chore: point workspace submodule to personal private repo"
git push
```

## Purpose

- Skill Pilot reads and writes your work under this folder.
- Linking it to your private repo keeps your work version-controlled and private.
- The sample repo (`X-School-Academy/skill-pilot_workspace`) is public and contains only placeholder structure — no real user data.
