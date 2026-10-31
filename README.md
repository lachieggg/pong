# pong

A live ping monitor for the terminal. It shows status, loss, min/avg/max
latency, and a bar graph of the last 40 pings.

## Usage

```
pong [host] [interval]
```

- `host`: ping target. Default `1.1.1.1`.
- `interval`: seconds between pings. Default `1`.

Press ctrl+c to quit.

## Graph

- The y-axis snaps to 50, 100, 200, 500, 1000, 2000, 5000 or 10000 ms. It
  zooms out when a spike arrives and zooms in when the spike leaves the
  40-ping window.
- Bar color runs from green (10 ms or less) to red (1500 ms or more) on a
  log scale.
- A timeout shows as a red `✗`. Each ping waits up to 5 seconds.

## Requirements

`bash`, `ping` (macOS flags), `awk`, `tput`, and a terminal with 24-bit
color.
