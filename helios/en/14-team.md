---
title: "Team Management"
---

## Objective

Manage tenant users, roles, and invitations.

## Access

Sidebar -> Team
Path: /app/{tenant}/team

## Roles

- owner, admin (full management)
- agent, viewer (read only)

## Invite a member

1. Press Invite Team Member.
2. Complete Email and Role.
3. Press Send Invitation.

Fields:

| Field | Mandatory | Format | Example | Note |
| --- | --- | --- | --- | --- |
| Email Address | Yes | valid email | user@acme.com | - |
| Role | Yes | admin/agent/viewer | agent | Permission control |

## Change a user's role

1. In the table, open Actions (menu).
2. Select the new role.
3. Confirm.

## Activate/deactivate user

1. In the table, open Actions.
2. Press Deactivate User or Activate User.
3. Confirm.

Notes:

- You cannot modify your own username.
- The owner role is fixed.

## Pending invitations

- They are listed in Pending Invitations.
- Shows email, role, guest by, expiration.

## Good practices

- Use viewer for read-only access.
- Deactivate users who do not require access.

## Suggested illustrations

### Team Members
![Team Members](../../images/helios/en/team/team-members-list.png)