# ❓ 14. FAQ & Troubleshooting Guide

Frequently asked questions and troubleshooting diagnostics for server administrators running PinataSpectra Sovereign Edition.

---

## 🛠️ Common Administrator Scenarios

### 1. The piñata spawned but is not swinging when struck.
* **Check Physics Toggle:** Ensure `physics.enabled: true` in `config.yml`.
* **Client Model Alignment:** Ensure your server resource pack correctly links the `CustomModelData` defined in `pinatas/*.yml` to a valid JSON model.

### 2. Players cannot damage the piñata during Phase 2.
* **Intended Mechanic:** In Phase 2, the boss enters **Orbital Shield Mode**. The boss is 100% immune until players eliminate all spawned **Guardian Minions**. Once all minions are defeated, the shield breaks automatically.

### 3. Will dropped candies cause lag if hundreds of players participate?
* **Zero-Lag Guarantee:** Candies in Sovereign Edition use the **Ephemeral Sweeper Engine**. They have instant-proximity magnetic pickup with zero entity collision calculation, and an async scavenger thread wipes any uncollected candy within 30 seconds.

---

## 🔍 Console Error Codes & Solutions

| Error Code | Root Cause | Solution |
| :--- | :--- | :--- |
| `ERR_MYSQL_TIMEOUT` | Database connection timed out. | Check MySQL host, port, and credentials in `config.yml`. The plugin will automatically fallback to SQLite. |
| `ERR_PDC_CORRUPT` | Entity NBT tag modified by an external cleaner. | Disable external entity-cleaner plugins (like ClearLag) from touching `item_display` or `SpectraCandyUUID` items. |
| `ERR_FOLIA_REGION` | Thread cross-boundary execution attempt. | Update to latest Sovereign release; all region tasks are routed through Folia's `RegionScheduler`. |

---

<div align="space-between">

[**← 13. Comparison & Editions**](13-Comparison-and-Editions.md) | [**15. Benchmark & Scaling →**](15-Benchmark-and-Stress-Testing.md)

</div>