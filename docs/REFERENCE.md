# Command reference

Use `node index.js` from the pinned source checkout described in the [README](../README.md). The entries below describe the inspected implementation.

| Command or argument | Behavior |
| --- | --- |
| `--ping` | Run TCP latency probes. |
| `--download` | Run download transfer measurements. |
| `--upload` | Run upload transfer measurements; no mode flags selects all three tests. |
| `--server URL` | Override the test server base URL. |
| `--size MB` | Set download size, default 10 MB. |
| `--duration SECONDS` | Set the upload measurement window, default 10 seconds; requests may outlast it. |
| `--isp` | Request ISP information from ip-api.com over HTTP. |
| `--json` | Print structured results. |
| `--simple` | Print a one-line summary. |

For prerequisites, file writes, external services and known limitations, see [Behavior and limits](../README.md#behavior-and-limits).

Implementation: [index.js](https://github.com/NickCirv/network-speed/blob/3705ebe111e41c73d746507e00cba68ac8c8dd2e/index.js); [review evidence](RESEARCH.md).
