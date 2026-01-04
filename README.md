# Winner Winner Chicken Dinner 🍗

A random guild member picker addon for World of Warcraft 1.12 (Vanilla).

Part of the **1701 Addons** suite for the USS Enterprise Guild.

## Installation

1. Copy the `1701-Chicken-Dinner` folder to your `Interface/AddOns` directory
2. Rename the folder to `GuildMemberSelector` (must match the .toc filename)
3. Restart WoW or `/reload`

## Commands

| Command | Description |
|---------|-------------|
| `/chd` | Pick a random eligible guild member |
| `/chickendinner` | Same as `/chd` |
| `/gpick` | Same as `/chd` |
| `/chd list` | List all eligible members |
| `/chd refresh` | Force refresh the guild roster |
| `/chd help` | Show command help |

## Eligibility Rules

- **Online members** are always eligible
- **Offline members** are eligible if last online within **5 days**
- If the last-online API is unavailable, all roster members are treated as eligible

## Features

- Preserves your "Show Offline Members" roster setting during scans
- Caches roster data for 60 seconds to avoid excessive refreshes
- Displays member info: name, level, class, and online status
- Sorted list view (online first, then alphabetically)

## API

The addon exposes functions for external use:

```lua
WinnerWinnerChickenDinner1701.PickRandomMember()   -- Returns random eligible member
WinnerWinnerChickenDinner1701.GetEligibleMembers() -- Returns table of eligible members
WinnerWinnerChickenDinner1701.ListEligibleMembers() -- Prints list to chat
WinnerWinnerChickenDinner1701.DoRandomPick()       -- Picks and announces winner
```

## Files

- `GuildMemberSelector.lua` - Main addon code
- `GuildMemberSelector.toc` - Addon metadata (Interface: 11200, Version: 1.0.1)
