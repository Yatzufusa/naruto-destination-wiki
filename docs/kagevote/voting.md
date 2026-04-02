# Kage Vote - Voting

Player-facing commands for participating in Kage elections.

---

## `/kagevote gui`

Open the **Kage Vote GUI** for a visual overview of active elections.

```
/kagevote gui
```

| | |
|---|---|
| **Permission** | Player |
| **Requires** | Must be a player (not console) |

---

## `/kagevote run`

Register yourself as a **candidate** in your village's active election.

```
/kagevote run
```

| | |
|---|---|
| **Permission** | Player |
| **Source** | `CommandKageVoteRun` |

**Requirements:**

- You must belong to an affiliation that has an active election
- Your rank must meet the minimum requirement (configurable)
- Your Naruto level must meet the minimum requirement (configurable)
- You must not be banned from running

!!! info
    If you don't meet the requirements, the command will tell you why you are ineligible.

---

## `/kagevote vote`

Cast your **vote** for a candidate in your village's election.

```
/kagevote vote <candidate>
```

| Parameter | Description |
|-----------|-------------|
| `candidate` | The player name of the candidate to vote for |

| | |
|---|---|
| **Permission** | Player |
| **Source** | `CommandKageVoteVote` |

**Requirements:**

- You must belong to an affiliation that has an active election
- Your rank must meet the minimum voting requirement (configurable)
- Your Naruto level must meet the minimum voting requirement (configurable)

!!! warning
    You can only vote once per election. Choose carefully!

---

## `/kagevote candidates`

View the **list of candidates** for an election.

```
/kagevote candidates [affiliation]
```

| Parameter | Description |
|-----------|-------------|
| `affiliation` | Village to check (optional, defaults to your own) |

| | |
|---|---|
| **Permission** | Player (level 0) |
| **Source** | `CommandKageVoteCandidates` |

---

## `/kagevote status`

View the **current status** of active elections, including time remaining and vote counts.

```
/kagevote status
```

| | |
|---|---|
| **Permission** | Player (level 0) |
