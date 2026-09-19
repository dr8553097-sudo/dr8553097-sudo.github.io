# ⏳ 09. Auto-Scheduler & Vote Party Engine (`events.yml`)

PinataSpectra Sovereign includes enterprise automation tooling to run scheduled server events, player-driven vote parties, and Discord webhooks automatically via the dedicated `events.yml` configuration file.

---

## ⏰ 1. Quartz-Style Cron Auto-Scheduler

Configure recurring automated spawns in `events.yml` without requiring external scheduler plugins:

```yaml
# ==============================================================================
#                  PINATASPECTRA SOVEREIGN - EVENTS & AUTOMATION
# ==============================================================================
auto-scheduler:
  enabled: true
  timezone: "UTC"
  events:
    - name: "daily_afternoon_party"
      cron: "0 0 16 * * ?"      # Every day at 4:00 PM
      pinata_id: "cosmic_unicorn"
      location: "spawn, 0.5, 75.0, 0.5, 0.0, 0.0"
      pre_broadcast_minutes: [15, 5, 1]
    - name: "weekend_infernal_boss"
      cron: "0 0 20 ? * SAT,SUN" # Saturdays & Sundays at 8:00 PM
      pinata_id: "infernal_dragon"
      location: "arena, 150.5, 64.0, -220.5, 0.0, 0.0"
      pre_broadcast_minutes: [30, 10, 5, 1]
```

---

## 🗳️ 2. Vote Party Integration (NuVotifier Hook)

Automatically track player votes across your server network and spawn celebratory piñatas when the milestone is achieved:

```mermaid
flowchart LR
    V[Player Votes on Server List] --> N[NuVotifier Listener]
    N --> M{Vote Counter >= Threshold?}
    M -->|No| P[Update Actionbar & BossBar Progress]
    M -->|Yes (e.g. 50/50)| S[🎉 Trigger Piñata Vote Party Event!]
    S --> R[Reset Counter to 0 & Save to DB]
```

* **Dynamic BossBar & Actionbar Progress:** Display live progress (e.g., `⚡ Vote Party: 42/50 Votes`).
* **PlaceholderAPI Support:** Expose `%pinata_voteparty_current%` and `%pinata_voteparty_needed%` on scoreboards.

---

<div align="space-between">

[**← 08. Leaderboards GUI & Stats**](08-Leaderboards-GUI-and-Stats.md) | [**10. Master Configuration Reference →**](10-Master-Configuration-Reference.md)

</div>