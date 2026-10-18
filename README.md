# SwiftForgeUI-Snapshots

Reference images for the snapshot tests of [SwiftForgeUI](https://github.com/HelloSamet/SwiftForgeUI). They live in their own repository so
that apps adding SwiftForgeUI as a Swift package never download them.

You don't clone this repository directly. In a SwiftForgeUI checkout, run:

```bash
scripts/snapshots.sh fetch
```

It clones this repository into `Examples/SwiftForgeShowcase/__Snapshots__` and checks out the exact revision
pinned in `Examples/SwiftForgeShowcase/snapshots.revision`, so every SwiftForgeUI commit is tested against the
references recorded for it.

## Updating references

1. In the SwiftForgeUI checkout, record with `TEST_RUNNER_SWIFTFORGE_RECORD_SNAPSHOTS=1` (see its CONTRIBUTING.md)
   and review every changed image.
2. Here, on a branch: commit the changed images and push them, then open a pull request.
3. In SwiftForgeUI: run `scripts/snapshots.sh pin` and commit the updated `snapshots.revision` with your change.

## License

MIT, like SwiftForgeUI. See [LICENSE](LICENSE).
