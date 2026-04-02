# Kage Vote Addon

The **NarutoDestinationKageVote** addon adds a democratic election system for choosing village Kages. Players can run as candidates, vote for their preferred leader, and admins can manage the entire election process.

---

## Command Overview

All Kage Vote commands are accessible through the master `/kagevote` command or their standalone equivalents.

### Player Commands

| Command | Description |
|---------|-------------|
| [`/kagevote gui`](voting.md#kagevote-gui) | Open the voting GUI |
| [`/kagevote run`](voting.md#kagevote-run) | Run as a candidate in your village's election |
| [`/kagevote vote`](voting.md#kagevote-vote) | Cast your vote for a candidate |
| [`/kagevote candidates`](voting.md#kagevote-candidates) | View current candidates |
| [`/kagevote status`](voting.md#kagevote-status) | View active election status |

### Admin Commands

| Command | Description |
|---------|-------------|
| [`/kagevote start`](admin-commands.md#kagevote-start) | Start a new election |
| [`/kagevote end`](admin-commands.md#kagevote-end) | Conclude an election and declare winner |
| [`/kagevote cancel`](admin-commands.md#kagevote-cancel) | Cancel an active election |
| [`/kagevote add`](admin-commands.md#kagevote-add) | Add a candidate to an election |
| [`/kagevote remove`](admin-commands.md#kagevote-remove) | Remove a candidate |
| [`/kagevote ban`](admin-commands.md#kagevote-ban) | Ban a player from running |
| [`/kagevote unban`](admin-commands.md#kagevote-unban) | Unban a player |
| [`/kagevote reload`](admin-commands.md#kagevote-reload) | Reload configuration |

---

## How Elections Work

1. An admin **starts** an election for a village with a set duration
2. Eligible players **run** as candidates (or admins add them)
3. Village members **vote** for their preferred candidate
4. The election **ends** when the timer expires or an admin concludes it
5. The candidate with the most votes becomes **Kage**

!!! info "Eligibility"
    Both running and voting have configurable requirements:

    - **Affiliation** &mdash; must belong to the village holding the election
    - **Rank** &mdash; configurable minimum rank to run or vote
    - **Level** &mdash; configurable minimum Naruto level
    - **Ban status** &mdash; banned players cannot run as candidates
