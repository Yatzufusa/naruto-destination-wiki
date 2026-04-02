# XP Events Addon

The **NarutoDestinationXPEvents** addon provides an XP multiplier event system. Events can be triggered manually for instant boosts or scheduled automatically on specific days of the week.

---

## Features

- **Manual events** &mdash; Start XP multiplier events instantly with custom duration
- **Automatic scheduling** &mdash; Configure events to run on specific days of the week
- **Threshold system** &mdash; Incremental multiplier steps for progressive events
- **GUI management** &mdash; Visual interface for admins to manage events
- **Live status** &mdash; Players can check current event status at any time

## Command

All functionality is accessed through the single [`/xpevent`](commands.md) command with various subcommands.

| Subcommand | Permission | Description |
|------------|------------|-------------|
| [`status`](commands.md#xpevent-status) | Player | Check current event status |
| [`now`](commands.md#xpevent-now) | OP | Start an event immediately |
| [`automatic`](commands.md#xpevent-automatic) | OP | Configure scheduled events |
| [`stop`](commands.md#xpevent-stop) | OP | Stop the active event |
| [`setmultiplier`](commands.md#xpevent-setmultiplier) | OP | Override the current multiplier |
| [`threshold`](commands.md#xpevent-threshold) | OP | Configure threshold steps |
| [`gui`](commands.md#xpevent-gui) | OP | Open the management GUI |
| [`reload`](commands.md#xpevent-reload) | OP | Reload configuration |
