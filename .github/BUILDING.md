# GitHub validation

All project build and validation work runs on GitHub-hosted GitHub Actions
runners. Open **Actions → Hosted bookmarklet validation → Run workflow** to
validate manually. Pushes and pull requests run the same workflow.

This repository contains a standalone browser bookmarklet with no dependency
manifest or compiler. CI checks `original-source.js` and the README's encoded
bookmarklet for JavaScript syntax errors, then uploads those existing files as
the `bookmarklet` artifact. CI does not execute the bookmarklet or log into any
banking service. There is no application package build to run.

Inspect the completed workflow and artifact before reporting validation
success. Any future minification, packaging, security checks, lint, type checks,
or tests must also run on hosted Actions runners. Report Actions blockers
instead of running builds on this computer.
