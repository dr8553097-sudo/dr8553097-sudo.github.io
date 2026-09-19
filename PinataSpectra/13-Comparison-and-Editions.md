# ⚖️ 13. Comparison & Edition Matrix

> [!IMPORTANT]
> **WHY PINATASPECTRA LITE HAS A SEPARATE REPOSITORY**  
> PinataSpectra Sovereign is our commercial, enterprise-grade event engine designed for high-concurrency production networks (50-200+ players).  
> **PinataSpectra Lite** is a lightweight, open-source community edition intended for small private SMP servers (<10 players). It is maintained in a completely separate repository with its own simplified codebase and docs to ensure zero proprietary IP leakage and clear separation of dependencies.

---

## 📊 Master Feature Comparison Matrix

| Feature / Capability | 👑 PinataSpectra Sovereign | ⚡ PinataSpectra Lite | 📦 Legacy Plugins (e.g. PinataParty) |
| :--- | :---: | :---: | :---: |
| **Target Concurrency** | **80 - 200+ Players** | < 10 Players | 10 - 20 Players |
| **Display Architecture** | **Native 3D ItemDisplay Entities** | Static ItemDisplay | Outdated Invisible ArmorStands |
| **Physics Engine** | **Harmonic Catenary Rope + Recoil** | None | Rigid Teleportation Only |
| **Boss Combat Phases** | **4 Stages (Shield, Minions, Frenzy)** | Single Stage | Single Stage (Click-only) |
| **Facial Emotions** | **4 Real-time Texture Morphs** | Static Model | None |
| **Particle Engine** | **Async Parametric LOD Equations** | Basic Spiral | Sync Single Circle (Causes Lag) |
| **Memory Safe Sweeper** | **Async Scavenger GC Thread** | Basic Despawn | Despawn Timers (Entity Leaks) |
| **Leaderboards & GUIs** | **Paginated GUI + Async MySQL** | Chat Text Only | FlatFile / YAML |
| **Scheduler Engine** | **Quartz Cron + NuVotifier Hook** | Simple Tick Timer | Tick Timer |
| **Folia Multi-Threading** | **Full Folia Region Threading** | Partial | ❌ Incompatible |
| **Tick Cost (80 Players)** | **< 0.04 ms** | ~0.35 ms | **3.20+ ms (Causes TPS Drops)** |
| **License & Source** | **Proprietary Commercial EULA** | Open Source (MIT) | Various |

---

<div align="space-between">

[**← 12. Developer API & Events**](12-Developer-API-and-Events.md) | [**14. FAQ & Troubleshooting →**](14-FAQ-and-Troubleshooting.md)

</div>