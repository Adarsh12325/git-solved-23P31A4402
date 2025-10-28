- 24549e3: feat: Add new feature (adarsh, 83 minutes ago)
- 17295e2: merge: Resolve all conflicts between main and dev branches Conflicts resolved in 6 files: - config/app-config.yaml: Combined production and development configurations - config/database-config.json: Created separate profiles for each environment - scripts/deploy.sh: Added multi-environment support with conditional logic - scripts/monitor.js: Implemented environment-based configuration - docs/architecture.md: Merged documentation covering both environments - README.md: Combined feature lists and updated documentation Resolution strategy: Maintained production stability while integrating development features as optional configurations. All features are now accessible through environment variables. (adarsh, 2 hours ago)
- 02011a5: updating dev (Hanu Gupta, 5 days ago)
- 0312c6f: updating main (Hanu Gupta, 5 days ago)
- fadfd24: Revise README for DevOps Simulator project (Hanu Gupta, 5 days ago)
- ae630eb: Initial commit (Hanu Gupta, 5 days ago)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git log feature/new-feature --oneline
- ac10ba5 (origin/feature/new-feature, feature/new-feature) feat: Add new feature
- 7a4f583 (origin/main) merge: Resolve all conflicts between main and conflict-simulator branches
- 17295e2 merge: Resolve all conflicts between main and dev branches Conflicts resolved in 6 files: - config/app-config.yaml: Combined - - production and development configurations - config/database-config.json: Created separate profiles for each environment - scripts/deploy.sh: Added multi-environment support with conditional logic - scripts/monitor.js: Implemented environment-based configuration - docs/architecture.md: Merged documentation covering both environments - README.md: Combined feature lists and updated documentation Resolution strategy: Maintained production stability while integrating development features as optional configurations. All features are now accessible through environment variables.
- d3dd9b2 (instructor/conflict-simulator, conflict-simulator) updating conflict-simulator
- 02011a5 (instructor/dev, dev) updating dev
- 0312c6f (instructor/main, instructor/HEAD) updating main
- fadfd24 Revise README for DevOps Simulator project
- ae630eb Initial commit

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git cherry-pick

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git cherry-pick ac10ba5
error: your local changes would be overwritten by cherry-pick.
hint: commit your changes or stash them to proceed.
fatal: cherry-pick failed

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git cherry-pick 7a4f583
error: your local changes would be overwritten by cherry-pick.
hint: commit your changes or stash them to proceed.
fatal: cherry-pick failed

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git add .

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git stash
Saved working directory and index state WIP on main: 70f04c7 docs: Add FAQ section

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git cherry-pick ac10ba5
[main 23f17d1] feat: Add new feature
 Date: Tue Oct 28 14:50:49 2025 +0530
 1 file changed, 2 insertions(+)
 create mode 100644 scripts/new-feature.js

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git push origin main
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 689 bytes | 172.00 KiB/s, done.
Total 7 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/Adarsh12325/git-solved-23P31A4402.git
   7a4f583..23f17d1  main -> main

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout -b feature/another-feature
Switched to a new branch 'feature/another-feature'

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>echo "test" > test.txt

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git add test.txt

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git commit -m "feat: Add test feature"
[feature/another-feature 5c0c6eb] feat: Add test feature
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>echo "update" >> README.md

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git add README.md

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git commit -m "docs: Update README"
[main e7b2a8a] docs: Update README
 1 file changed, 1 insertion(+)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout feature/another-feature
Switched to branch 'feature/another-feature'

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git rebase main
Successfully rebased and updated refs/heads/feature/another-feature.

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git push origin feature/another-feature --force
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 12 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 534 bytes | 41.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
remote:
remote: Create a pull request for 'feature/another-feature' on GitHub by visiting:
remote:      https://github.com/Adarsh12325/git-solved-23P31A4402/pull/new/feature/another-feature
remote:
To https://github.com/Adarsh12325/git-solved-23P31A4402.git
 * [new branch]      feature/another-feature -> feature/another-feature

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>echo "BUG" >> scripts/deploy.sh

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git add scripts/deploy.sh

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git commit -m "Bad commit"
[feature/another-feature 6804bbf] Bad commit
 1 file changed, 1 insertion(+)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git revert HEAD
[feature/another-feature 9f33a4c] Revert "Bad commit"
 1 file changed, 1 deletion(-)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git reset --soft HEAD~1

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git reset --mixed HEAD~1

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git reset --hard HEAD~1
HEAD is now at e7b2a8a docs: Update README

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git reflog
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{0}: reset: moving to HEAD~1
de11176 (origin/feature/another-feature) HEAD@{1}: reset: moving to HEAD~1
6804bbf HEAD@{2}: reset: moving to HEAD~1
9f33a4c HEAD@{3}: revert: Revert "Bad commit"
6804bbf HEAD@{4}: commit: Bad commit
de11176 (origin/feature/another-feature) HEAD@{5}: rebase (finish): returning to refs/heads/feature/another-feature
de11176 (origin/feature/another-feature) HEAD@{6}: rebase (pick): feat: Add test feature
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{7}: rebase (start): checkout main
5c0c6eb HEAD@{8}: checkout: moving from main to feature/another-feature
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{9}: commit: docs: Update README
23f17d1 (origin/main) HEAD@{10}: checkout: moving from feature/another-feature to main
5c0c6eb HEAD@{11}: commit: feat: Add test feature
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{0}: reset: moving to HEAD~1
de11176 (origin/feature/another-feature) HEAD@{1}: reset: moving to HEAD~1
6804bbf HEAD@{2}: reset: moving to HEAD~1
9f33a4c HEAD@{3}: revert: Revert "Bad commit"
6804bbf HEAD@{4}: commit: Bad commit
de11176 (origin/feature/another-feature) HEAD@{5}: rebase (finish): returning to refs/heads/feature/another-feature
de11176 (origin/feature/another-feature) HEAD@{6}: rebase (pick): feat: Add test feature
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{7}: rebase (start): checkout main
5c0c6eb HEAD@{8}: checkout: moving from main to feature/another-feature
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{9}: commit: docs: Update README
23f17d1 (origin/main) HEAD@{10}: checkout: moving from feature/another-feature to main
5c0c6eb HEAD@{11}: commit: feat: Add test feature
23f17d1 (origin/main) HEAD@{12}: checkout: moving from main to feature/another-feature
23f17d1 (origin/main) HEAD@{13}: cherry-pick: feat: Add new feature
70f04c7 HEAD@{14}: reset: moving to HEAD
70f04c7 HEAD@{15}: checkout: moving from main to main
70f04c7 HEAD@{16}: checkout: moving from main to main
70f04c7 HEAD@{17}: checkout: moving from feature/new-feature to main
ac10ba5 (origin/feature/new-feature, feature/new-feature) HEAD@{18}: commit: feat: Add new feature
7a4f583 HEAD@{19}: checkout: moving from main to feature/new-feature
70f04c7 HEAD@{20}: commit: docs: Add FAQ section
7a4f583 HEAD@{21}: checkout: moving from feature/new-feature to main
7a4f583 HEAD@{22}: reset: moving to HEAD
7a4f583 HEAD@{23}: checkout: moving from main to feature/new-feature
7a4f583 HEAD@{24}: commit (merge): merge: Resolve all conflicts between main and conflict-simulator branches
17295e2 HEAD@{25}: checkout: moving from main to main
17295e2 HEAD@{26}: commit (merge): merge: Resolve all conflicts between main and dev branches Conflicts resolved in 6 files: - config/app-config.yaml: Combined production and development configurations - config/database-config.json: Created separate profiles for each environment - scripts/deploy.sh: Added multi-environment support with conditional logic - scripts/monitor.js: Implemented environment-based configuration - docs/architecture.md: Merged documentation covering both environments - README.md: Combined feature lists and updated documentation Resolution strategy: Maintained production stability while integrating development features as optional configurations. All features are now accessible through environment variables.
0312c6f (instructor/main, instructor/HEAD) HEAD@{27}: checkout: moving from dev to main
02011a5 (instructor/dev, dev) HEAD@{28}: checkout: moving from main to dev
0312c6f (instructor/main, instructor/HEAD) HEAD@{29}: checkout: moving from main to main
0312c6f (instructor/main, instructor/HEAD) HEAD@{30}: checkout: moving from main to main
0312c6f (instructor/main, instructor/HEAD) HEAD@{31}: checkout: moving from conflict-simulator to main
d3dd9b2 (instructor/conflict-simulator, conflict-simulator) HEAD@{32}: checkout: moving from main to conflict-simulator
0312c6f (instructor/main, instructor/HEAD) HEAD@{33}: clone: from https://github.com/partnrnetwork/git-mastery-challenge-template
(END)

( Used ALL Git Command )_____________________>>>>>
(1). Used fetch 1 time, pull 1 time.-------------------------------------------------------------------------------------------------------

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git fetch instructor

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git diff main instructor/main
diff --git a/CHANGELOG.md b/CHANGELOG.md
deleted file mode 100644
index 55ee2d0..0000000
--- a/CHANGELOG.md
+++ /dev/null
@@ -1,6 +0,0 @@
-- 24549e3: feat: Add new feature (adarsh, 83 minutes ago)
-- 17295e2: merge: Resolve all conflicts between main and dev branches Conflicts resolved in 6 files: - config/app-config.yaml: Combined production and development configurations - config/database-config.json: Created separate profiles for each environment - scripts/deploy.sh: Added multi-environment support with conditional logic - scripts/monitor.js: Implemented environment-based configuration - docs/architecture.md: Merged documentation covering both environments - README.md: Combined feature lists and updated documentation Resolution strategy: Maintained production stability while integrating development features as optional configurations. All features are now accessible through environment variables. (adarsh, 2 hours ago)
-- 02011a5: updating dev (Hanu Gupta, 5 days ago)
-- 0312c6f: updating main (Hanu Gupta, 5 days ago)
-- fadfd24: Revise README for DevOps Simulator project (Hanu Gupta, 5 days ago)
-- ae630eb: Initial commit (Hanu Gupta, 5 days ago)
\ No newline at end of file
diff --git a/GIT_JOURNEY.md b/GIT_JOURNEY.md
deleted file mode 100644
index 8f373de..0000000
--- a/GIT_JOURNEY.md
+++ /dev/null
@@ -1,179 +0,0 @@
-# My Git Mastery Challenge Journey
-
-## Student Information
-- Name: Adarsh Sah
-- Student ID: 23P31A4402
! If there are updates, pull them
sh: line 1: If: command not found
#done  (press RETURN)
...skipping...
diff --git a/CHANGELOG.md b/CHANGELOG.md
deleted file mode 100644
index 55ee2d0..0000000
--- a/CHANGELOG.md
+++ /dev/null
@@ -1,6 +0,0 @@
-- 24549e3: feat: Add new feature (adarsh, 83 minutes ago)
-- 17295e2: merge: Resolve all conflicts between main and dev branches Conflicts resolved in 6 files: - config/app-config.yaml: Combined production and development configurations - config/database-config.json: Created separate profiles for each environment - scripts/deploy.sh: Added multi-environment support with conditional logic - scripts/monitor.js: Implemented environment-based configuration - docs/architecture.md: Merged documentation covering both environments - README.md: Combined feature lists and updated documentation Resolution strategy: Maintained production stability while integrating development features as optional configurations. All features are now accessible through environment variables. (adarsh, 2 hours ago)
-- 02011a5: updating dev (Hanu Gupta, 5 days ago)
-- 0312c6f: updating main (Hanu Gupta, 5 days ago)
-- fadfd24: Revise README for DevOps Simulator project (Hanu Gupta, 5 days ago)
-- ae630eb: Initial commit (Hanu Gupta, 5 days ago)
\ No newline at end of file
diff --git a/GIT_JOURNEY.md b/GIT_JOURNEY.md
deleted file mode 100644
index 8f373de..0000000
--- a/GIT_JOURNEY.md
+++ /dev/null
@@ -1,179 +0,0 @@
-# My Git Mastery Challenge Journey
-
-## Student Information
-- Name: Adarsh Sah
-- Student ID: 23P31A4402
-- Repository: https://github.com/Adarsh12325/git-solved-23P31A4402
-- Date Started: 28/10/25
-- Date Completed: 28/10/25
-
-## Task Summary
-Cloned instructor's repository with pre-built conflicts and resolved all
-merge conflicts across multiple branches using proper Git workflows.
-
-## Commands Used
-
-| Command | Times Used | Purpose |
-|---------|------------|----------|
-| git clone | 1 | Clone instructor's repository |
-| git checkout | 20+ | Switch between branches |
-| git branch | 10+ | View and manage branches |
-| git merge | 2 | Merge dev and conflict-simulator into main |
-| git add | 30+ | Stage resolved conflicts |
-| git commit | 15+ | Commit resolved changes |
-| git push | 10+ | Push to my repository |
-| git fetch | 2 | Fetch updates from instructor |
-| git pull | 1 | Pull updates |
-| git stash | 2 | Save temporary work |
-| git cherry-pick | 1 | Copy specific commit |
-| git rebase | 1 | Rebase feature branch |
-| git reset | 3 | Undo commits (soft/mixed/hard) |
-| git revert | 1 | Safe undo |
-| git tag | 2 | Create release tags |
-| git status | 50+ | Check repository state |
:
C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git pull instructor main
From https://github.com/partnrnetwork/git-mastery-challenge-template
 * branch            main       -> FETCH_HEAD
Already up to date.


(2). Used stash 1 time.--------------------------------------------------------------------------------------------------------------------

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout -b feature/new-feature
fatal: a branch named 'feature/new-feature' already exists

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>echo "// New feature" >> scripts/new-feature.js

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git add scripts/new-feature.js

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git stash push -m "WIP: New feature development"
Saved working directory and index state On main: WIP: New feature development

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>echo "## FAQ" >> README.md

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git add README.md

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git commit -m "docs: Add FAQ section"
[main ba5b45a] docs: Add FAQ section
 1 file changed, 1 insertion(+)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout feature/new-feature
Switched to branch 'feature/new-feature'

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git stash pop
On branch feature/new-feature
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   scripts/new-feature.js

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        tructor main

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (f8136e7a80bcd7d821ba230e72525ada36b1c8ef)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>echo "// Feature complete" >> scripts/new-feature.js

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git add scripts/new-feature.js

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git commit -m "feat: Add new feature"
[feature/new-feature f81b96d] feat: Add new feature
 1 file changed, 2 insertions(+)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git push origin feature/new-feature
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 350 bytes | 70.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Adarsh12325/git-solved-23P31A4402.git
   ac10ba5..f81b96d  feature/new-feature -> feature/new-feature
   

(3). Used cherry-pick 1 time.--------------------------------------------------------------------------------------------------------------

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout main
Already on 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git log feature/new-feature --oneline
f81b96d (origin/feature/new-feature, feature/new-feature) feat: Add new feature
ac10ba5 feat: Add new feature
7a4f583 merge: Resolve all conflicts between main and conflict-simulator branches
17295e2 merge: Resolve all conflicts between main and dev branches Conflicts resolved in 6 files: - config/app-config.yaml: Combined production and development configurations - config/database-config.json: Created separate profiles for each environment - scripts/deploy.sh: Added multi-environment support with conditional logic - scripts/monitor.js: Implemented environment-based configuration - docs/architecture.md: Merged documentation covering both environments - README.md: Combined feature lists and updated documentation Resolution strategy: Maintained production stability while integrating development features as optional configurations. All features are now accessible through environment variables.
d3dd9b2 (instructor/conflict-simulator, conflict-simulator) updating conflict-simulator
02011a5 (instructor/dev, dev) updating dev
0312c6f (instructor/main, instructor/HEAD) updating main
fadfd24 Revise README for DevOps Simulator project
ae630eb Initial commit

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git cherry-pick f81b96d
[main 4bc3aef] feat: Add new feature
 Date: Tue Oct 28 16:48:08 2025 +0530
 1 file changed, 2 insertions(+)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git push origin main
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 12 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 655 bytes | 81.00 KiB/s, done.
Total 7 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.
To https://github.com/Adarsh12325/git-solved-23P31A4402.git
   0adf177..4bc3aef  main -> main

(4). Used rebase 1 time.-------------------------------------------------------------------------------------------------------------------

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout -b feature/another-feature
fatal: a branch named 'feature/another-feature' already exists

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>echo "test" > test.txt

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git add test.txt

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git commit -m "feat: Add test feature"
[main d46d800] feat: Add test feature
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>
C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template># Main has moved forward
'#' is not recognized as an internal or external command,
operable program or batch file.

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout main
Already on 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>echo "update" >> README.md

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git add README.md

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git commit -m "docs: Update README"
[main bc9c11b] docs: Update README
 1 file changed, 1 insertion(+)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>
C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template> # Rebase feature onto main
'#' is not recognized as an internal or external command,
operable program or batch file.

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout feature/another-feature
Switched to branch 'feature/another-feature'

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git rebase main
warning: skipped previously applied commit 23f17d1
hint: use --reapply-cherry-picks to include skipped commits
hint: Disable this message with "git config set advice.skippedCherryPicks false"
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Auto-merging config/app-config.yaml
CONFLICT (add/add): Merge conflict in config/app-config.yaml
Auto-merging config/database-config.json
CONFLICT (add/add): Merge conflict in config/database-config.json
Auto-merging docs/architecture.md
CONFLICT (add/add): Merge conflict in docs/architecture.md
Auto-merging scripts/deploy.sh
CONFLICT (add/add): Merge conflict in scripts/deploy.sh
Auto-merging scripts/monitor.js
CONFLICT (add/add): Merge conflict in scripts/monitor.js
error: could not apply d3dd9b2... updating conflict-simulator
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
hint: Disable this message with "git config set advice.mergeConflict false"
Could not apply d3dd9b2... # updating conflict-simulator

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>
C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template># Push (may need --force)
'#' is not recognized as an internal or external command,
operable program or batch file.

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git push origin feature/another-feature --force
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Adarsh12325/git-solved-23P31A4402.git
 + de11176...e7b2a8a feature/another-feature -> feature/another-feature (forced update)


(5). Git Reset & revert--------------------------------------------------------------------------------------------------------------------

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>echo "BUG" >> scripts/deploy.sh

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git add scripts/deploy.sh

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git commit -m "Bad commit"
[feature/another-feature 6804bbf] Bad commit
 1 file changed, 1 insertion(+)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git revert HEAD
[feature/another-feature 9f33a4c] Revert "Bad commit"
 1 file changed, 1 deletion(-)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git reset --soft HEAD~1

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git reset --mixed HEAD~1

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git reset --hard HEAD~1
HEAD is now at e7b2a8a docs: Update README

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git reflog
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{0}: reset: moving to HEAD~1
de11176 (origin/feature/another-feature) HEAD@{1}: reset: moving to HEAD~1
6804bbf HEAD@{2}: reset: moving to HEAD~1
9f33a4c HEAD@{3}: revert: Revert "Bad commit"
6804bbf HEAD@{4}: commit: Bad commit
de11176 (origin/feature/another-feature) HEAD@{5}: rebase (finish): returning to refs/heads/feature/another-feature
de11176 (origin/feature/another-feature) HEAD@{6}: rebase (pick): feat: Add test feature
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{7}: rebase (start): checkout main
5c0c6eb HEAD@{8}: checkout: moving from main to feature/another-feature
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{9}: commit: docs: Update README
23f17d1 (origin/main) HEAD@{10}: checkout: moving from feature/another-feature to main
5c0c6eb HEAD@{11}: commit: feat: Add test feature
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{0}: reset: moving to HEAD~1
de11176 (origin/feature/another-feature) HEAD@{1}: reset: moving to HEAD~1
6804bbf HEAD@{2}: reset: moving to HEAD~1
9f33a4c HEAD@{3}: revert: Revert "Bad commit"
6804bbf HEAD@{4}: commit: Bad commit
de11176 (origin/feature/another-feature) HEAD@{5}: rebase (finish): returning to refs/heads/feature/another-feature
de11176 (origin/feature/another-feature) HEAD@{6}: rebase (pick): feat: Add test feature
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{7}: rebase (start): checkout main
5c0c6eb HEAD@{8}: checkout: moving from main to feature/another-feature
e7b2a8a (HEAD -> feature/another-feature, main) HEAD@{9}: commit: docs: Update README
23f17d1 (origin/main) HEAD@{10}: checkout: moving from feature/another-feature to main
5c0c6eb HEAD@{11}: commit: feat: Add test feature
23f17d1 (origin/main) HEAD@{12}: checkout: moving from main to feature/another-feature
23f17d1 (origin/main) HEAD@{13}: cherry-pick: feat: Add new feature
70f04c7 HEAD@{14}: reset: moving to HEAD
70f04c7 HEAD@{15}: checkout: moving from main to main
70f04c7 HEAD@{16}: checkout: moving from main to main
70f04c7 HEAD@{17}: checkout: moving from feature/new-feature to main
ac10ba5 (origin/feature/new-feature, feature/new-feature) HEAD@{18}: commit: feat: Add new feature
7a4f583 HEAD@{19}: checkout: moving from main to feature/new-feature
70f04c7 HEAD@{20}: commit: docs: Add FAQ section
7a4f583 HEAD@{21}: checkout: moving from feature/new-feature to main
7a4f583 HEAD@{22}: reset: moving to HEAD
7a4f583 HEAD@{23}: checkout: moving from main to feature/new-feature
7a4f583 HEAD@{24}: commit (merge): merge: Resolve all conflicts between main and conflict-simulator branches
17295e2 HEAD@{25}: checkout: moving from main to main
17295e2 HEAD@{26}: commit (merge): merge: Resolve all conflicts between main and dev branches Conflicts resolved in 6 files: - config/app-config.yaml: Combined production and development configurations - config/database-config.json: Created separate profiles for each environment - scripts/deploy.sh: Added multi-environment support with conditional logic - scripts/monitor.js: Implemented environment-based configuration - docs/architecture.md: Merged documentation covering both environments - README.md: Combined feature lists and updated documentation Resolution strategy: Maintained production stability while integrating development features as optional configurations. All features are now accessible through environment variables.
0312c6f (instructor/main, instructor/HEAD) HEAD@{27}: checkout: moving from dev to main
02011a5 (instructor/dev, dev) HEAD@{28}: checkout: moving from main to dev
0312c6f (instructor/main, instructor/HEAD) HEAD@{29}: checkout: moving from main to main
0312c6f (instructor/main, instructor/HEAD) HEAD@{30}: checkout: moving from main to main
0312c6f (instructor/main, instructor/HEAD) HEAD@{31}: checkout: moving from conflict-simulator to main
d3dd9b2 (instructor/conflict-simulator, conflict-simulator) HEAD@{32}: checkout: moving from main to conflict-simulator
0312c6f (instructor/main, instructor/HEAD) HEAD@{33}: clone: from https://github.com/partnrnetwork/git-mastery-challenge-template
(END)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git reset --hard 17295e2
HEAD is now at 17295e2 merge: Resolve all conflicts between main and dev branches Conflicts resolved in 6 files: - config/app-config.yaml: Combined production and development configurations - config/database-config.json: Created separate profiles for each environment - scripts/deploy.sh: Added multi-environment support with conditional logic - scripts/monitor.js: Implemented environment-based configuration - docs/architecture.md: Merged documentation covering both environments - README.md: Combined feature lists and updated documentation Resolution strategy: Maintained production stability while integrating development features as optional configurations. All features are now accessible through environment variables.

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git cherry-pick ac10ba5
[main 24549e3] feat: Add new feature
 Date: Tue Oct 28 14:50:49 2025 +0530
 1 file changed, 2 insertions(+)
 create mode 100644 scripts/new-feature.js

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git push origin main --force
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 413 bytes | 206.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Adarsh12325/git-solved-23P31A4402.git
 + 23f17d1...24549e3 main -> main (forced update) 


(6). Created 2+ tags.----------------------------------------------------------------------------------------------------------------------

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git tag -a v1.0.0 -m "Release 1.0.0: Resolved all conflicts"

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git tag -a v1.1.0 -m "Release 1.1.0: Added all features"

C:\GPP_TASKS\Git_Mastery\git-mastery-challenge-template>git push origin --tags
Enumerating objects: 2, done.
Counting objects: 100% (2/2), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 246 bytes | 61.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Adarsh12325/git-solved-23P31A4402.git
 * [new tag]         v1.0.0 -> v1.0.0
 * [new tag]         v1.1.0 -> v1.1.0


