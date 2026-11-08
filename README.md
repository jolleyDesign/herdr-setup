# Herdr setup

My Herdr app config: the Herdr Sim layout and the mods it uses. Only my own files are
tracked (see `.gitignore`); Herdr writes everything else here.

## New computer

1. Install Herdr and start it once (it creates `~/.config/herdr-app`).
2. In that folder:

   ```sh
   git init -b main
   git remote add origin <repo url>
   git fetch origin
   git checkout -f main
   ```

   Herdr picks the files up live. Switch to the layout with `ctrl-shift-l` if it isn't shown.
3. Optional: space folders are saved outside this folder, in `~/.config/herdr-space-folders.json`.
   To carry them over, copy that file into `extras/` here and commit it, then copy it back on the
   new machine (they reference this machine's space ids, so they may not all match).

## Needs

- Simulator panel: Xcode with a simulator and Node; Android SDK and an emulator for Android.
- Forge (`ctrl-shift-f`): `gh` signed in (or `glab` for GitLab), `python3`.
- Git graph and filetree: `git`.

## Layout: `herdr-sim`

A clone of Herdr 0.1.14's `main`:

- Sidebar: `space-folders` (spaces with folders), `agents-herdr-sim` (double-click an agent to rename its tab).
- Top bar (`tabs-herdr-sim`): Changes, Git (`cmd-g`), Tree, Simulator (`cmd-shift-s`).
- `main-folders`: Herdr's `main` with folders in the sidebar.

Cloned mods (`tabs-herdr-sim`, `agents-herdr-sim`, `space-folders`) and the layouts are frozen
copies; after a Herdr update that changes the originals, re-clone and re-apply the changes.

## Sources

- herdr-sim, herdr-sim-screen, tabs-herdr-sim: github.com/wobsoriano/herdr-sim
- git-graph: github.com/rabeeh-ta/herdr-git-graph
- forge-*: github.com/greenflagged/herdr-forge
- over9k-switcher: github.com/herunan/herdr-over9k (no key bound)
- filetree, file-icons: github.com/cybertron288/herdr-mods
