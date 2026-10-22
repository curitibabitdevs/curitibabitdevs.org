# Contributing Guidelines

Thanks for helping improve the BitDevs Socratic Seminar archive!

This document defines the scope, rules, and workflow for contributing to the repository.
Instructions for creating or updating meetup posts live in the README.

This document explains **what** we accept and **how** to contribute so we stay consistent.

## Contents

- [Scope of contributions](#scope-of-contributions)
- [Citation & link policy](#citation--link-policy)
- [Style guide (Markdown)](#style-guide-markdown)
- [Contribution workflow](#contribution-workflow)
- [Branch naming conventions](#branch-naming-conventions)
- [Commit message conventions](#commit-message-conventions)
- [Merge strategy](#merge-strategy)

---

## Scope of contributions

This repository accepts two main types of contributions:

- **Meetup-related content**: topics, links, summaries, and corrections for specific Socratic seminars.
- **General repository maintenance**: documentation, layouts, scripts, CI configuration, and other housekeeping.

This guide focuses on defining what is in scope and how contributions should be made.
Workflow and naming rules apply to all contribution types.

### Accepted contributions

#### General repository maintenance

- Documentation improvements
- Layout and styling changes
- Scripts, tooling, and CI configuration
- Refactors that improve consistency or maintainability

#### Meetup-related contributions

- Topic summaries and background material
- Curated resource lists (papers, PRs, BIPs, mailing-list threads)
- Corrections and structural improvements
- New templates that improve the contributor experience

### Out of scope

- Opinionated or editorial content unless explicitly approved
- Content unrelated to Bitcoin or Socratic Seminar discussions
- Promotional or low-signal material

---

If you only want to **propose topics** (without editing files yourself), you can open an Issue like:

> `Topics for Socratic #NNN`

and list the suggested links. In that case, the sections **Citation & link policy**, and **Style guide (Markdown)** are the most relevant.

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
  - URL shorteners whenever possible
  - Tracking parameters (`utm_*`, etc.) when it doesn't break the link
- X/Twitter links are acceptable if they are the main source
- Respect privacy:
  - Don't link to **private chat logs**, closed groups, or personal DMs
  - Don't include personal data about attendees (emails, phone numbers, doxxing, etc.)
  - When summarizing ideas from participants, it's fine to keep it anonymous unless they already publish under that identity

---

## Style guide (Markdown)

To keep the archive consistent and easy to read:

- **Headings**
  - Start sections at `##` and use `###` for subsections.
  - Use a small, predictable set of sections, for example:
    - `## Avisos` / `## Announcements`
    - `### Bitcoin`, `### Lightning`, `### Mining`, `### Misc`.

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

---

## Contribution workflow

1. **Open an Issue** (optional but recommended for bigger changes) and describe what you'll add or fix.
2. **Fork** the repo and create a feature branch:

```shell
  git checkout -b docs/2025-10-seminar-notes
```

3. **Make your changes** and commit them with a meaningful message.
4. **Push your changes** to your forked repository:

```shell
  git push origin docs/2025-10-seminar-notes
```

5. **Make sure your branch is up to date with the `master` branch** before opening the PR.
6. **Run checks locally** if the repository provides them (e.g. linters, test scripts, or static site build).
   Example: `make` / `make test` / `jekyll serve`, as documented in the README.
7. **Open a Pull Request (PR)** to the main repository and link it to the Issue (if applicable).

Try to keep each PR focused on **one meetup** or **one logical change** (e.g. "fix broken links in September 2026 post").

### PR description

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

### Addressing review comments

- Push follow-up commits to the same branch.
- **Clean history approach**: Feel free to amend commits and force-push with `--force-with-lease` to keep history clean—just leave a comment in the PR describing your changes.
- Alternatively, you can add new commits for each review round; maintainers will squash at merge time if needed.

---

## Merge strategy

We currently default to **"Squash and merge"**, because commit histories are often fragmented or
poorly structured. Squashing makes the final commit reflect the PR title, which a maintainer can
adjust before merging.

That said, we prefer a clean and well-structured commit history: when the commits in a PR are
meaningful on their own, we can use **"Rebase and merge"** instead, preserving a clearer history
on `master`.

What this means for contributors:

- You **don't need** perfectly clean commits while you are iterating on your branch, and
  force-pushing to your own feature branch is fine before review.
- Cleaning up "WIP" commits before asking for review is welcome — it's what makes rebase and merge
  possible.
- Maintainers pick the merge strategy. If we squash, we'll make sure the final commit message
  follows the conventions above.
- Never push directly to `master`.
