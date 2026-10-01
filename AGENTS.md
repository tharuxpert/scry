# Scry

macOS Swift app built with XcodeGen and SwiftLint.

## Fork-only development

This checkout independently maintains `tharuxpert/scry`. Keep all new development,
commits, branches, pushes, issues, and pull requests confined to that fork.

- `origin` must point to `https://github.com/tharuxpert/scry.git`; `main` tracks
  `origin/main`. Start future work from the fork's `main`.
- `upstream` points to `giacomoguidotto/scry` for read-only reference. Keep its push
  URL disabled. Do not push, open or edit pull requests/issues, comment, merge,
  tag, release, or change settings in the original repository unless the user
  explicitly authorizes a specific upstream action.
- Leave upstream PRs #45 and #46 and their source branches (`fix/ocr-completion`
  and `fix/force-click-lookup`) unchanged unless the user specifically requests
  an update. Future fork work must use different branches.
- Specify `--repo tharuxpert/scry` for GitHub CLI operations; do not rely on
  automatic repository selection for a fork. Verify the push destination before
  pushing and push only the requested branch, without automatic tags.
- Keep automatic tagging and release publishing disabled for this fork.
  Creating a release requires an explicit user request.

## Workflow

Run all three checks and fix any failures before considering the task done:

```sh
cd app && xcodegen generate && xcodebuild -scheme Scry -configuration Debug build test && swiftlint
```

The Xcode project is generated from `app/project.yml`. Re-run `xcodegen` from `app/` when you add, remove, or rename source files, or change project settings. Code-only changes do not require regeneration.

## Further reading

- [Versioning & commits](docs/versioning.md)

## Agent skills

### Issue tracker

Issues are tracked in GitHub Issues on this repo. See `docs/agents/issue-tracker.md`.

### Triage labels

Use the default five-label triage vocabulary. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context layout: read `CONTEXT.md` and relevant ADRs before architecture work. See `docs/agents/domain.md`.
