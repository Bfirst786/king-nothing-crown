# Open actions: Project / Incubator / HFS gap

Flagged 2026-10-21 for immediate action after the file-share setup. Not yet done.

1. **Amend STD-008 (Fabrication Incubator Operating Model).** It has activity sessions and pilots but no tier for a project, and no promotion path. Proposed ladder: Activity, Build, Test bed, Pilot. Promotion adds layers (HFS linkage, evidence tags, change control) without moving files. Triggers are qualitative: repeatedly contradicts HFS, crosses components, produces reusable output, needs change control. Decide level names, triggers, and whether test beds count against the two-pilot and 5 to 10 hour limits.
2. **Resolve DR-001** (crown in its own repo): confirm the working-folder-plus-extraction rule and ask for the GitHub guide to say so.
3. **Log the decisions.** Add the ladder and the repo decision to the HFS decision log (SYS-CTL-LOG-001). The live log is in the HFS DEVELOPMENT Claude project and could not be written from the KING NOTHING session.
4. **Check names.** "Pilot" and "project" already carry meanings in HFS and in Claude. Record any new level names in the nomenclature changelog (SYS-CTL-LOG-002).
5. **Write-access problem.** Writes to some locations work in one session and fail in another. Observed in the 2026-10-21 session (this is all that was seen; earlier sessions were not available to check):
   - Project library: a write from `/tmp` was refused ("local_path must be inside the working directory"); the same file copied under `/home/claude` was accepted. Two later writes from different folders both worked. The `/tmp` refusal was a path rule, not a permission.
   - GitHub CLI: the `GH_TOKEN` in the session was rejected as invalid, so repo checks and creation failed. Attaching the repo through the session and pushing worked, so a repo can be unwritable through one credential and writable through another.
   - Memory: `/areas/home-fab-system.md` is outside the session's project subtree and cannot be written from the KING NOTHING session.
   - HFS decision log: the live copy sits in the HFS DEVELOPMENT Claude project, and a session is bound to one project, so it cannot be written from here.
   - Google Drive: not tested; only read and search tools were loaded.
   Still to decide: where each master lives, and which project each session should start from for the target it needs to write.
6. **Create the Drive folder** `KING NOTHING` with matching subfolders; parent location still to be chosen.
7. **Confirm the Fusion licence** question (DR-002).
8. **Review the skills** one at a time (`/kn-hfs` first) and commit them.
