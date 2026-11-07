# Phase 1: Planning – North&Bridge Ltd

## 1. Company profile

North&Bridge Ltd is a fictional professional services firm with about 50
staff in one office, plus some remote and hybrid workers (this is why VPN
support is needed). The IT team is simulated: one Tier 1 helpdesk agent and
one Tier 2 sysadmin.

| Department | Staff |
|---|---|
| Finance | 10 |
| HR | 5 |
| Sales | 12 |
| Operations | 13 |
| IT | 3 |
| Management | 7 |
| **Total** | **50** |

Note: only about 10 user accounts will be created in Active Directory for
the lab. The rest of the headcount is described, not built.

## 2. Priority matrix

| Priority | Definition | Example |
|---|---|---|
| P1 – Critical | Many users or a critical service down | VPN down for all remote staff |
| P2 – High | One user fully blocked, or a department impacted | Finance user locked out at month end |
| P3 – Medium | One user partially affected, workaround exists | Software won't install, web version available |
| P4 – Low | Request or minor issue | Printer preference, how-to question |

## 3. SLA targets (simulated)

These values are my own simulation choices. They are not taken from ITIL
or any official standard.

| Priority | First response | Resolution target |
|---|---|---|
| P1 | 15 minutes | 4 hours |
| P2 | 30 minutes | 8 hours |
| P3 | 4 hours | 3 business days |
| P4 | 1 business day | 5 business days |

- **First response:** time until someone acknowledges the ticket and starts work.
- **Resolution target:** time within which the ticket should be fixed and closed.

## 4. Support tiers and escalation

**Tier 1 (helpdesk):** logs and triages tickets, handles password resets,
account unlocks, known-fix articles and basic software install checks.

**Tier 2 (systems/network):** handles server, network and Active Directory
issues such as VPN configuration, Group Policy (GPO) problems and log
analysis on the domain controller.

**Escalate from Tier 1 to Tier 2 when:**
- the ticket can't be resolved within the agreed time
- the root cause is infrastructure (server, network, AD)
- more than one user is affected
- admin rights beyond Tier 1 are needed

**A handover note must include:**
- what the user reported
- what was already tried
- relevant error messages or event IDs
- the business impact
