# 📜 10. Master Configuration Reference (`config.yml`)

Below is the complete, annotated reference for the master `config.yml` file in PinataSpectra Sovereign Edition.

```yaml
# ==============================================================================
#                 PINATASPECTRA SOVEREIGN EDITION - MASTER CONFIG
# ==============================================================================

settings:
  language: "en_US"
  debug_mode: false
  metrics: true

# Database storage backend (SQLite for local, MySQL/MariaDB for networks)
database:
  type: "SQLITE" # Options: SQLITE, MYSQL, MARIADB
  mysql:
    host: "127.0.0.1"
    port: 3306
    database: "pinataspectra"
    username: "root"
    password: "password123"
    pool_size: 10
    connection_timeout_ms: 5000

# 3D Display Entity & Suspension Physics
physics:
  enabled: true
  harmonic_oscillation:
    frequency: 1.2
    amplitude: 0.15
    air_damping: 0.96
  recoil:
    hit_impulse_multiplier: 1.4
    max_tilt_degrees: 45.0
  rope:
    enabled: true
    particle: "DUST"
    dust_color: "#e2e8f0"
    points_per_meter: 4

# Performance & Particle LOD Throttling
performance:
  particle_lod:
    enabled: true
    full_density_radius: 8.0
    medium_density_radius: 24.0
    cull_radius: 48.0
  tps_guard:
    enabled: true
    minimum_tps_threshold: 18.5
    action: "REDUCE_PARTICLES" # Options: REDUCE_PARTICLES, DISABLE_AURA

# Ephemeral Candies & Scavenger Sweeper
candies:
  instant_pickup: true
  auto_despawn_seconds: 30
  max_concurrent_in_world: 250
  sound_on_pickup: "ENTITY_ITEM_PICKUP"
```

---

> [!NOTE]
> **Modular Architecture Notice:**
> - **Scheduled Events, Vote Parties & Discord Webhooks:** Configured separately in [`events.yml`](09-Auto-Scheduler-and-Vote-Party.md).
> - **Piñata Profiles & Templates:** Configured in individual files inside the [`pinatas/`](05-Custom-Pinata-Creation-Guide.md) folder.

---

<div align="space-between">

[**← 09. Auto-Scheduler & Vote Party**](09-Auto-Scheduler-and-Vote-Party.md) | [**11. Commands & Placeholders →**](11-Commands-Permissions-and-Placeholders.md)

</div>