# Contributing Guidelines

Thanks for helping improve the BitDevs Socratic Seminar archive!

This repository stores the topics, links, and resources discussed in our Socratic Bitcoin seminars.
Each post corresponds to a specific meetup and serves as a public record of what was covered.

This document explains **what** we accept and **how** to contribute so we stay consistent.

## Contents
- [Scope of contributions](#scope-of-contributions)
- [Contribution workflow](#contribution-workflow)
- [Branch naming conventions](#branch-naming-conventions)
- [Commit message conventions](#commit-message-conventions)
- [Pull Request (PR) process](#pull-request-pr-process)
- [Squashing & merge strategy](#squashing--merge-strategy)
- [Citation & link policy](#citation--link-policy)
- [Style guide (Markdown)](#style-guide-markdown)

---

## Scope of contributions

We welcome:

- **Meeting notes** (agendas, link lists, brief summaries)
- **Topic summaries** (background, trade-offs, relevant work)
- **Resource lists** (papers, PRs, BIPs, mailing-list threads)
- **Corrections/improvements** (typos, clarifications, structure)
- **New templates** that improve contributor experience

We avoid:

- Opinionated essays (unless clearly marked as editorial and approved)
- Non-Bitcoin content unrelated to Socratic Seminar topics

---

## Contribution workflow

1. **Open an Issue** (optional but recommended for bigger changes) and describe what you'fll add or fix.
2. **Fork** the repo and create a feature branch:

       git checkout -b docs/2025-10-seminar-notes

3. **Make your changes** and commit them with a meaningful message.
4. **Push your changes** to your forked repository:

       git push origin docs/2025-10-seminar-notes

5. **Open a Pull Request (PR)** to the main repository and link it to the Issue (if applicable).

Try to keep each PR focused on **one meetup** or **one logical change** (e.g. "fix broken links in September 2025 post").

---

## Branch naming conventions

Use short, lowercase names with words separated by hyphens and, when useful, a simple prefix.

Recommended patterns:

- `feat/...` - new content or features
- `fix/...` - bug fixes or corrections
- `docs/...` - documentation-only changes (README, CONTRIBUTING, templates)
- `chore/...` - maintenance, refactors, or build-related changes

Examples:

- `feat/2025-11-socratic-040`
- `docs/add-contributing-guide`
- `fix/typo-2025-09-topics`
- `chore/reorder-readme`

If you create the branch from the GitHub UI, try to avoid generic names like `patch-1` and prefer something descriptive.

---

## Commit message conventions

We follow a lightweight style similar to what is already used in `saopaulobitdevs.org`, for example:

- `feat: november meetup`
- `feat(header): add X (@saopaulobitdevs) link to navigation`
- `feat(_posts): arkade announcement`
- `fix(_posts): use xcancel. fuck X`
- `fix broken link and remove two topics`
- `2025-09 (#68)`

General rules:

- Write commit messages in **English**.
- Start with a **type**, optional **scope**, then a **short description**:

      <type>(optional-scope): short description

- Keep the subject line concise (ideally ≤ 72 characters).
- Use the body (optional) to explain **why** you're changing something, not just **what** changed.

Common types:

- `feat` - new posts, new sections, or new functionality
- `fix` - bug fixes, broken links, formatting issues
- `docs` - README, CONTRIBUTING, or other documentation-only updates
- `chore` - maintenance (moving files, renaming, non-user-visible cleanups)
- `refactor` - internal restructuring without changing behavior
- `style` - whitespace, formatting, no content changes
- `test` - adding or adjusting tests (if the repo grows tests later)

Examples for this repository:

- `feat(topics): add socratic seminar 040`
- `feat(posts): add november 2025 meetup`
- `fix(links): update delvingbitcoin URLs for september`
- `docs: add contribution guidelines`
- `chore(posts): reorder sections by topic`

If you are working on a seminar topic file and that's the only change in the PR, a short and focused subject like below is fine:

- `2025-09: add socratic seminar topics`

---

## Pull Request (PR) process

When opening a PR, please:

1. **Keep it focused.**  
   Ideally, one PR = one meetup post or one small set of related fixes.

2. **Sync with `main`** before opening:

       git fetch upstream
       git checkout main
       git pull upstream main
       git checkout your-branch
       git rebase main

3. **Run checks locally** if the repository provides them (e.g. linters, test scripts, or static site build).  
   Example: `make` / `make test` / `jekyll serve`, as documented in the README.

4. **Write a clear PR description.**  
   A simple template you can follow:

       Summary
       -------
       - Add topics for the November 2025 Socratic seminar.
       - Include links to BIPs, PRs, and Delving Bitcoin threads.

       Details
       -------
       - Meetup date: 2025-11-05
       - Sections: Announcements, Bitcoin, Lightning, Misc

       Checklist
       ---------
       - [ ] Links render correctly in Markdown preview
       - [ ] No private or non-public resources referenced

5. **Address review comments.**  
   - Push follow-up commits in the same branch.
   - Prefer adding new commits rather than force-pushing while the review is active (maintainers can squash at merge time).

A maintainer will review your changes and either approve, request small fixes, or start a discussion if something is unclear.

---

## Squashing & merge strategy

To keep the history readable, we generally:

- Use **"Squash and merge"** for most PRs so that each PR becomes a **single logical commit** on `main` (often one commit per meetup or per change-set).
- Occasionally keep multiple commits (regular merge) when the history inside the PR is meaningful on its own.

What this means for contributors:

- You **don't need** perfectly clean commits while you are iterating on your branch.
- It's nice (but not mandatory) to clean up obvious "WIP" commits before asking for review.
- Maintainers will pick an appropriate merge strategy. If we squash, we'll make sure the final commit message follows the conventions above.

Please:

- Never push directly to `main`.
- Avoid force-pushing to branches that are already under active review unless you're explicitly asked to rebase/cleanup.

---

## Citation & link policy

This archive is meant to point to **public resources** and capture **what was discussed**, not who said what in the room.

When adding topics:

- Prefer **canonical, stable URLs**:
  - Bitcoin Core / other repos on GitHub
  - BIPs from the official BIPs repository
  - bitcoin-dev / delvingbitcoin threads
  - arXiv papers, project documentation, blog posts
- Avoid:
  - URL shorteners whenever possible.
  - Tracking parameters (`utm_*`, etc.) when it doesn't break the link.
- X/Twitter links are acceptable if they are the main source, but:
  - Prefer pairing them with a more durable reference when available (mailing list, blog, BIP PR, etc.).
- Respect privacy:
  - Don't link to **private chat logs**, closed groups, or personal DMs.
  - Don't include personal data about attendees (emails, phone numbers, doxxing, etc.).
  - When summarizing ideas from participants, it's fine to keep it anonymous unless they already publish under that identity.

---

## Style guide (Markdown)

To keep the archive consistent and easy to read:

- **Headings**
  - Start sections at `##` and use `###` for subsections.
  - Use a small, predictable set of sections, for example:
    - `## Avisos` / `## Announcements`
    - `### Bitcoin`, `### Lightning`, `### Mining`, `### Maneiro` / `### Misc`.

- **Lists**
  - Use bullet lists for topics, with descriptive link text:

        * [BIP-444: Reduced Data Temporary Softfork](https://github.com/bitcoin/bips/pull/2017) - softfork proposal to reduce block data.
        * [LND 0.20.0-rc2](https://github.com/lightningnetwork/lnd/releases/tag/v0.20.0-beta.rc2)

  - Prefer **descriptive link text** instead of bare URLs.

- **Language**
  - File content can follow the meetup's usual language (e.g. Portuguese or English).
  - **Commit messages and PR descriptions should always be in English.**

- **Formatting details**
  - Try to wrap lines around ~100 characters to keep diffs readable.
  - Avoid trailing whitespace and unnecessary blank lines.
  - Keep YAML front-matter and indentation consistent with existing files.
  - When adding new files, copy from a recent existing post/template to match structure.

- **Code & configuration**
  - If you touch any scripts or configuration files:
    - Follow the existing style in that language (indentation, quoting, etc.).
    - Prefer small, focused changes that are easy to review.

Thanks again for contributing and helping to keep our Socratic archive useful and consistent!
