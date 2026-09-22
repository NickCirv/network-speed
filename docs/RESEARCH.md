# Source review — network-speed

## Revision and method

Inspected public commit: [`3705ebe111e41c73d746507e00cba68ac8c8dd2e`](https://github.com/NickCirv/network-speed/commit/3705ebe111e41c73d746507e00cba68ac8c8dd2e). Source tree: `bf2ddff494278fd1ff14e0018e9986a3eb4436fe`. Capture scope: all eligible text files; 6 of 6 eligible files.

This review read captured implementation and documentation. It did not install dependencies, execute project commands, call project APIs, check package publication or establish live CI status. Examples are source-derived, not captured execution transcripts.

## Claim ledger

| Claim | Evidence | Status |
| --- | --- | --- |
| Test endpoints, request sizes, TCP timing and output | [index.js](https://github.com/NickCirv/network-speed/blob/3705ebe111e41c73d746507e00cba68ac8c8dd2e/index.js) | Verified in inspected source; execution unverified |

## Findings and verification gaps

Latency is TCP connection timing, not ICMP ping. Default download traffic goes to Cloudflare’s speed endpoint with an httpbin fallback; uploads use httpbin. Results depend on those services and the network path, not just the access link. The upload loop can overrun its requested duration while awaiting a request. ISP lookup uses unencrypted HTTP.

No project tests were executed.

| Dimension | Result |
| --- | --- |
| Purpose and documented commands | Partially verified: static source inspection |
| Clean installation and examples | Unverified |
| Test suite and live CI | Unverified |
| Performance and security guarantees | Unverified |
| Publication | Local documentation only |

## Documentation inventory

- [README.md](https://github.com/NickCirv/network-speed/blob/3705ebe111e41c73d746507e00cba68ac8c8dd2e/README.md) — Rewritten; historic section anchors retained where practical.
- [LICENSE](https://github.com/NickCirv/network-speed/blob/3705ebe111e41c73d746507e00cba68ac8c8dd2e/LICENSE) — protected document preserved unchanged.

## Captured source inventory

- [LICENSE](https://github.com/NickCirv/network-speed/blob/3705ebe111e41c73d746507e00cba68ac8c8dd2e/LICENSE) — Git blob `05b804beeec7d1a6c933d087387ba4adf6463d93`.
- [README.md](https://github.com/NickCirv/network-speed/blob/3705ebe111e41c73d746507e00cba68ac8c8dd2e/README.md) — Git blob `dd8c6bb84272250877f9775154ec57ab9e40b045`.
- [package.json](https://github.com/NickCirv/network-speed/blob/3705ebe111e41c73d746507e00cba68ac8c8dd2e/package.json) — Git blob `9fc6d0a739c80992c0c627e1e5176701d2fa4b89`.
- [.github/workflows/ci.yml](https://github.com/NickCirv/network-speed/blob/3705ebe111e41c73d746507e00cba68ac8c8dd2e/.github/workflows/ci.yml) — Git blob `44515034a394670de44454a7a1bd2c7ef0c9836e`.
- [index.js](https://github.com/NickCirv/network-speed/blob/3705ebe111e41c73d746507e00cba68ac8c8dd2e/index.js) — Git blob `1c268ce58bbcf8d3cba5b7754f91c7571ea14e4c`.
- [test/smoke.test.js](https://github.com/NickCirv/network-speed/blob/3705ebe111e41c73d746507e00cba68ac8c8dd2e/test/smoke.test.js) — Git blob `a2eba067c997f85dfb0e2dbaf147bbde33266e19`.

## Scope boundary

Capture excludes lockfiles, binary artwork, generated output, vendored dependencies and files above the acquisition size limit. The tree records their existence; no verification claim is made for omitted content. Protected documents and historical records are not replaced.

## Reference coverage

Added [command reference](REFERENCE.md) from the argument parser, command handlers and source-defined help at the pinned revision. README examples remain unexecuted.
