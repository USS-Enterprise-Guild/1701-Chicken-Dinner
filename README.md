# GuildMemberSelector 1701

Random guild member picker for WoW 1.12 with a simple roster refresh flow.

## Commands

- `/chd` or `/chickendinner` or `/gpick` - Pick a random guild member (online within 5 days).
- `/chd list` - List all eligible members.
- `/chd refresh` - Force refresh the guild roster.
- `/chd help` - Show command help.

## Eligibility Rules

- Members currently online are always eligible.
- Offline members are eligible if they were online within the last 5 days.
- If the last-online API is unavailable, offline members in the roster are treated as eligible.

## Notes

- The addon temporarily shows offline members to scan eligibility, then restores the user's original "Show Offline Members" setting.
- Guild roster updates are asynchronous; actions run after `GUILD_ROSTER_UPDATE` when needed.

## Files

- `GuildMemberSelector.lua`
- `GuildMemberSelector.toc`
