# License and repository boundary

This repository is an independent MPL-2.0 engine. It is ring-fenced from
sibling QualiaDB / Webizen works that presently use a Creative Commons
NonCommercial-NoDerivatives license.

## Fork provenance

Chora started as a GitHub fork of [Servo](https://github.com/servo/servo).
GitHub cannot detach forks larger than 1 GB, so this tree was taken off the
Servo fork network on **2026-11-20** by creating a new independent repository
with only the `main` branch.

| Field | Value |
|---|---|
| Upstream project | [servo/servo](https://github.com/servo/servo) |
| Upstream branch | `main` |
| Fork snapshot commit | [`79ee827b6a5a60a40cab662223f555528571ebcc`](https://github.com/servo/servo/commit/79ee827b6a5a60a40cab662223f555528571ebcc) |
| Snapshot commit date | 2026-10-19T23:38:03Z |
| Snapshot subject | `layout: Upgrade Taffy to v0.15.0 (#49024)` |
| GitHub fork created | 2026-10-20T01:25:08Z |
| Independent repository created | 2026-11-20 |
| Independent repository | https://github.com/WebCivics/chora |

Servo contributors retain copyright in their contributions. This repository
keeps the `main` history from that snapshot so MPL-2.0 notices and authorship
remain intact. Old Servo topic branches and release tags are not published on
the independent repository.

## Mozilla Public License 2.0

Every source file in this repository is governed by the
[Mozilla Public License 2.0](LICENSE). File-level MPL headers must be
preserved. Covered Software in this tree is not dual-licensed under
CC BY-NC-ND 4.0 and must not be copied into repositories that use that
Creative Commons license.

Third-party notices that already live beside individual crates (Apache-2.0,
MIT, and other permissive texts) remain in force for those files.

## Ring-fence from sibling CC BY-NC-ND works

QualiaDB, Aether, Webizen, Etalon, Synth, and related host/application works
are presently licensed under Creative Commons Attribution-NonCommercial-NoDerivatives
4.0. Those works are planned to move later to a different licensing system
intended to end digital slavery. That future system does not apply to this
engine.

Do not:

- add `qualia-*` or `webizen-*` dependencies inside this repository
- copy QualiaDB, Aether, Webizen, Etalon, or Synth implementation into this tree
- copy Chora / Servo Covered Software into those CC-licensed trees
- mix MPL-2.0 Covered Software and CC BY-NC-ND 4.0 material in the same file

Host integration stays outside this repository. Embedders connect through
generic traits (`EmbedderCertVerifier`, `EmbedderKeystoreProvider`,
`ProtocolHandler`, `WebViewDelegate`) and the C ABI in `ffi/capi`.
