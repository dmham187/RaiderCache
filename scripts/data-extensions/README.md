# Data extensions

Manual additions that the upstream data (RaidTheory) does not contain yet.
`fetch-data.ts` merges them in after every sync:

- `items.json`: items are added only if their id is missing upstream.
- `hideout.json`: for an existing module only levels above the upstream maximum are appended; unknown modules are added.
- `quests.json`: quests are added only if their id is missing upstream.
- `projects.json`: projects are added only if their id is missing upstream.

Once upstream catches up, the extension entries are ignored automatically. Delete them whenever convenient.
Format is the raw RaidTheory format (snake_case ids, `name.en`).
