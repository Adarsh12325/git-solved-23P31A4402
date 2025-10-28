# My Git Mastery Challenge Journey

## Student Information
- Name: Adarsh Sah
- Student ID: 23P31A4402
- Repository: https://github.com/Adarsh12325/git-solved-23P31A4402
- Date Started: 28/10/25
- Date Completed: 28/10/25

## Task Summary
Cloned instructor's repository with pre-built conflicts and resolved all 
merge conflicts across multiple branches using proper Git workflows.

## Commands Used

| Command | Times Used | Purpose |
|---------|------------|----------|
| git clone | 1 | Clone instructor's repository |
| git checkout | 20+ | Switch between branches |
| git branch | 10+ | View and manage branches |
| git merge | 2 | Merge dev and conflict-simulator into main |
| git add | 30+ | Stage resolved conflicts |
| git commit | 15+ | Commit resolved changes |
| git push | 10+ | Push to my repository |
| git fetch | 2 | Fetch updates from instructor |
| git pull | 1 | Pull updates |
| git stash | 2 | Save temporary work |
| git cherry-pick | 1 | Copy specific commit |
| git rebase | 1 | Rebase feature branch |
| git reset | 3 | Undo commits (soft/mixed/hard) |
| git revert | 1 | Safe undo |
| git tag | 2 | Create release tags |
| git status | 50+ | Check repository state |
| git log | 30+ | View history |
| git diff | 20+ | Compare changes |

## Conflicts Resolved

### Merge 1: main + dev (6 files)

#### Conflict 1: config/app-config.yaml
- **Issue**: Production used port 8080, development used 3000
- **Resolution**: Created unified config with environment-based settings
- **Strategy**: Keep production as default, add dev as optional
- **Difficulty**: Medium
- **Time**: 15 minutes

#### Conflict 2: config/database-config.json
- **Issue**: Different database hosts and SSL modes
- **Resolution**: Created separate profiles for production and development
- **Strategy**: Restructured JSON to support both environments
- **Difficulty**: Medium
- **Time**: 10 minutes

#### Conflict 3: scripts/deploy.sh
- **Issue**: Different deployment strategies (production vs docker-compose)
- **Resolution**: Added conditional logic based on DEPLOY_ENV variable
- **Strategy**: Made script handle both environments dynamically
- **Difficulty**: Hard
- **Time**: 20 minutes

#### Conflict 4: scripts/monitor.js
- **Issue**: Different monitoring intervals and log formats
- **Resolution**: Environment-based configuration object
- **Strategy**: Used process.env.NODE_ENV to determine behavior
- **Difficulty**: Medium
- **Time**: 15 minutes

#### Conflict 5: docs/architecture.md
- **Issue**: Different architectural descriptions
- **Resolution**: Merged both descriptions into comprehensive document
- **Strategy**: Created sections for each environment
- **Difficulty**: Easy
- **Time**: 10 minutes

#### Conflict 6: README.md
- **Issue**: Different feature lists and version numbers
- **Resolution**: Combined all features with clear environment labels
- **Strategy**: Organized features by category
- **Difficulty**: Easy
- **Time**: 10 minutes

### Merge 2: main + conflict-simulator (6 files)
Merge Conflict Summary — Production + Experimental Integration

#### Conflict 1: config/app-config.yaml
- **Issue**: Production used static ports (8080, 3000), Experimental introduced AI and metrics ports (9000–9002)
- **Resolution**: Unified configuration supporting multi-port environments
- **Strategy**: Default to production ports; include AI ports under experimental profile
- **Difficulty**: Medium
- **Time**: 20 minutes

#### Conflict 2: config/database-config.json
- **Issue**: Production had traditional single-host DB; Experimental introduced distributed and replicated setup
- **Resolution**: Integrated both into a structured multi-environment JSON
- **Strategy**: Keep production and development under standard section; add distributed cluster under experimental
- **Difficulty**: Medium
- **Time**: 15 minutes

#### Conflict 3: scripts/deploy.sh
- **Issue**: Production used rolling updates; Experimental had AI-based predictive scaling
- **Resolution**: Merged both into one adaptive deployment script
- **Strategy**: Added conditional flags (--experimental, DEPLOY_ENV) to handle different strategies dynamically
- **Difficulty**: Hard
- **Time**: 25 minutes

#### Conflict 4: scripts/monitor.js
- **Issue**: Production had simple monitoring; Experimental used AI prediction and ML-based metrics
- **Resolution**: Combined both modes with environment toggle
- **Strategy**: Retained production stability, added AI-enhanced monitoring under experimental mode
- **Difficulty**: Hard
- **Time**: 25 minutes

#### Conflict 5: docs/architecture.md
- **Issue**: Production described microservices setup; Experimental added event-driven AI/ML and multi-cloud details
- **Resolution**: Created a comprehensive architecture covering all environments
- **Strategy**: Organized into “Stable” and “Experimental” sections for clarity
- **Difficulty**: Medium
- **Time**: 15 minutes
 
#### Conflict 6: README.md
- **Issue**: Production focused on CI/CD basics; Experimental added AI, ML, and chaos engineering features
- **Resolution**: Merged all content, distinguishing Stable and Experimental builds
- **Strategy**: Unified documentation while keeping version history intact
- **Difficulty**: Easy
- **Time**: 10 minutes-

#### Overall Summary
All conflicts were resolved by merging production stability with experimental AI capabilities.
Final codebase now supports:
- Environment-aware configurations
- AI-enhanced monitoring and deployment
- Unified documentation and maintainability


## Used ALL Git Commands

1. Used fetch 1 time, pull 1 time.
2. Used stash 1 time.
3. Used cherry-pick 1 time.
4. Used rebase 1 time.
5. Used reset 3 times, revert 1 times.
6. Created 2+ tags.


## Most Challenging Parts

1. **Understanding Conflict Markers**: Initially confused by `<<<<<<<`, `=======`, `>>>>>>>` symbols. Learned that HEAD is current branch and the other side is incoming changes.

2. **Deciding What to Keep**: Hardest part was choosing between conflicting code. Learned to read both versions completely before deciding.

3. **Complex Logic Conflicts**: deploy.sh had completely different logic. Had to understand both approaches before combining.

4. **Testing After Resolution**: Making sure resolved code actually worked was crucial.

## Key Learnings

### Technical Skills
- Mastered conflict resolution process
- Understood merge conflict markers
- Learned to use git diff effectively
- Practiced all major Git commands

### Best Practices
- Always read both sides of conflict before resolving
- Test resolved code before committing
- Write detailed merge commit messages
- Use git status frequently
- Commit atomically

### Git Workflow Insights
- Conflicts are normal, not errors
- Take time to understand both changes
- When in doubt, ask for clarification
- Document your resolution strategy
- Keep calm and read carefully

## Reflection
This challenge taught me that merge conflicts aren't scary - they're 
just Git asking "which version do you want?". The key is understanding 
what each side is trying to do before combining them. I now feel 
confident handling conflicts in real projects.

The hands-on practice with all Git commands (especially rebase and 
cherry-pick) was invaluable. I understand the difference between merge 
and rebase, and when to use each. Most importantly, I learned that 
git reflog is a lifesaver!
