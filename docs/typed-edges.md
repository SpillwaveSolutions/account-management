# Typed edges — Account Management

Direction matters. Packs follow outbound edges by default.

| `rel` | Meaning |
|-------|---------|
| `belongs_to` | Contact or deliverable belongs to client |
| `owned_by` | Account manager identity |
| `has` | Client has plan / SOW / risk |
| `reports_to` | Contact reporting line |
| `committed_to` | Commitment toward deliverable |
| `due_on` | Milestone or renewal date |
| `originates_from` | Came from meeting or thread |
| `related_to` | Soft association |
| `blocks` | Issue blocks deliverable |

Unknown `rel` values are treated as `info` by validation. Do not invent new names in this plugin.
