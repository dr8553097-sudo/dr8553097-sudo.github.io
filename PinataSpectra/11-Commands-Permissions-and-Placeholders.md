# 🧩 11. Commands, Permissions & PlaceholderAPI

PinataSpectra Sovereign provides a clean, tab-completable command structure for administrators and players, alongside extensive PlaceholderAPI support.

---

## 💻 1. Command Syntax & Permissions

| Command | Permission | Description |
| :--- | :--- | :--- |
| `/pinata help` | `pinataspectra.use` | Displays interactive help menu. |
| `/pinata top [tier]` | `pinataspectra.top` | Opens paginated leaderboards GUI. |
| `/pinata stats [player]` | `pinataspectra.stats` | Shows player combat statistics and hit counts. |
| `/pinata spawn <id> [x y z]` | `pinataspectra.admin.spawn` | Spawns a 3D piñata boss at location. |
| `/pinata killall` | `pinataspectra.admin.killall` | Despawns all active piñatas and cleans candies. |
| `/pinata reload` | `pinataspectra.admin.reload` | Hot-reloads all configs, piñatas, and GUIs. |
| `/pinata votes set <amount>` | `pinataspectra.admin.votes` | Manually modifies vote party counter. |

---

## 🏷️ 2. PlaceholderAPI Reference

Use these placeholders anywhere PlaceholderAPI is supported (TAB, Scoreboard, Chat, Holograms, DeluxeMenus):

| Placeholder | Output Example | Description |
| :--- | :--- | :--- |
| `%pinata_active%` | `true` / `false` | Whether any piñata event is currently active. |
| `%pinata_active_name%` | `Infernal Dragon` | Name of the currently spawned piñata. |
| `%pinata_active_health%` | `342` | Current health of active piñata. |
| `%pinata_active_health_max%` | `500` | Max health of active piñata. |
| `%pinata_active_health_percent%` | `68.4%` | Health percentage formatted. |
| `%pinata_active_phase%` | `Phase 2 (Shield)` | Current combat phase status. |
| `%pinata_top_1_player%` | `Dafealru` | Current #1 top damage dealer in event. |
| `%pinata_top_1_damage%` | `142` | Damage dealt by current #1 player. |
| `%pinata_player_damage%` | `58` | Caller's total damage in current event. |
| `%pinata_player_hits%` | `14` | Caller's total hits landed. |
| `%pinata_voteparty_current%` | `38` | Current votes accumulated. |
| `%pinata_voteparty_needed%` | `50` | Total votes needed for next party. |
| `%pinata_voteparty_percent%` | `76.0%` | Vote party progress bar percentage. |

---

<div align="space-between">

[**← 10. Master Configuration Reference**](10-Master-Configuration-Reference.md) | [**12. Developer API & Events →**](12-Developer-API-and-Events.md)

</div>