# Privacy Policy — SE2 Team Sync

_Last updated: 2026-07-02_

## What this app is

**SE2 Team Sync** is an internal tool used by Salesforce Solution Engineers to
synchronize display names, avatar photos, and department metadata between a
Salesforce demo org and a Slack Enterprise Grid workspace. It is not sold,
distributed to end users, or offered as a commercial service.

## What data the app accesses

When installed by a Slack Enterprise Grid Org Owner, the app can read and write
the following user profile fields via the Slack Web API and SCIM endpoints:

- `displayName`, `givenName`, `familyName`
- `photos[0].value` (avatar image URL)
- `title`, `department` (read-only in practice; SCIM does not persist `title`)

The app does **not** access:

- Direct messages, channel messages, or file contents
- Message reactions, threads, or search history
- Any billing or payment information

## Where data is stored

- **Slack side**: All modifications are made directly to Slack's user records.
  No data is exported to third-party systems.
- **Local operator machine**: A CSV file (`team-members.csv`) containing
  `slack_user_id`, `jp_first`, `jp_last`, and matching hints for a target
  Salesforce demo org may be stored locally by the operator. This file is
  `.gitignore`d and never committed to the source repository.
- **Photos**: Fictional demo avatars generated from AI image tools are hosted
  publicly at <https://github.com/manabutech-kyushu/t10-photos>. Real employee
  photos are never uploaded to this repository.

## Retention

The app itself does not maintain a server or database. Any operational data
lives on the operator's local machine and is retained at the operator's
discretion.

## Who can use it

Only Enterprise Grid Org Owners of workspaces owned by the Salesforce
Solution Engineering team. External distribution requires explicit approval.

## Contact

For questions or removal requests, please open an issue at
<https://github.com/manabutech-kyushu/t10-photos/issues>.
