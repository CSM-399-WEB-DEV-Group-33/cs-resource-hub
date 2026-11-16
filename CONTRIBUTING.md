# Contributing & Workflow Guide — CS Resource Hub

This guide keeps all 9 members of **CSM 399 Group 33** aligned on Git branching, code quality, and QA documentation so we meet every rubric requirement for **Team Collaboration (15%)**, **Code Quality (20%)**, and **Testing & Review**.

## 1. Branching Strategy

Never commit directly to `main`. Keep `main` clean and demo-ready at all times.

| Branch | Purpose | Who Merges | 
| ----- | ----- | ----- | 
| `main` | Production / demo-ready code only | PM or Front-End Lead via reviewed PR | 
| `dev` | Active integration branch for completed features | Team members via PR | 
| `feat/<short-name>` | New features (e.g., `feat/resource-library`, `feat/bookmarks-context`) | Feature owner | 
| `fix/<short-name>` | Bug fixes and UI polish (e.g., `fix/mobile-navbar`) | Bug owner / QA | 
| `docs/<short-name>` | README, Design Doc assets, QA test logs | Any member | 

### Standard Workflow

```bash
# 1. Sync with dev
git checkout dev
git pull origin dev

# 2. Create your feature branch
git checkout -b feat/your-feature-name

# 3. Work, stage, and commit with clear messages
git add .
git commit -m "feat: add tag filter pills to ResourceLibrary"

# 4. Push and open a Pull Request into dev
git push -u origin feat/your-feature-name
```

## 2. Commit Message Convention

Use short, descriptive prefixes so our commit history is easy for Dr. Banning to grade:

* `feat:` — New feature or page (e.g., `feat: implement BookmarkContext with localStorage`)
* `fix:` — Bug fix or layout issue (e.g., `fix: prevent card overflow on 375px mobile`)
* `style:` — SASS/Bootstrap styling tweaks with no logic change
* `docs:` — Documentation, README, or QA log updates
* `refactor:` — Code cleanup without changing behavior
* `test:` — QA scripts or test cases

## 3. Pull Request Checklist

Before requesting a review on GitHub, verify:

* [ ] Code runs without console errors or React key warnings.
* [ ] Layout works cleanly across **mobile (375px)**, **tablet (768px)**, and **desktop (1280px+)**.
* [ ] All external resource links in `db.json` point to real, publicly accessible URLs (no copyrighted file uploads).
* [ ] Components are modular and well-commented.
* [ ] At least **1 teammate** has reviewed and approved the PR.

## 4. QA Issue & Bug Log Template

The CSM 399 Course Outline requires **documentation of issues found and resolved** during Testing & Review. Use this format when opening GitHub Issues or updating `docs/QA_TEST_LOG.md`:

```markdown
### [BUG-001] Short Title
- **Reported By:** @handle
- **Device / Browser:** e.g., Mobile (375px) / Chrome
- **Steps to Reproduce:**
  1. Go to ...
  2. Click ...
- **Expected Result:** ...
- **Actual Result:** ...
- **Status:** Open | In Progress | Resolved (PR #__)
```
