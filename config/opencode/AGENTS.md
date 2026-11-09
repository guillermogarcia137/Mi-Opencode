# Global rules

## Persistent memory

A `memory` MCP server (knowledge graph) is available and persists across all sessions and projects.

- At the start of a session, or whenever the user asks about themselves, their preferences, their projects, or past decisions, call the memory tools first (`search_nodes`, then `open_nodes`; use `read_graph` only when you need everything) before answering.
- Before finishing a task, save durable facts the user would expect you to remember: preferences, project details, decisions, conventions, and corrections. Use `create_entities` for new subjects and `add_observations` to extend existing ones.
- Use consistent `entityType` values: `user`, `preference`, `project`, `decision`, `fact`, `environment`.
- Keep entity names stable and descriptive (for example `user`, `project:opencode-config`) so they can be found later.
- Only store information the user would reasonably want retained. Never store secrets, passwords, tokens, API keys, or private credentials.
- When the user says "forget" or corrects a stored fact, delete or update the corresponding observations.

## User

- Communicates in Spanish. Reply in Spanish unless asked otherwise.
