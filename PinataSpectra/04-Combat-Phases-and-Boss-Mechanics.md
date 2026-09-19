# ⚔️ 04. Combat Phases & Boss Mechanics

PinataSpectra transforms typical piñata click-fests into a multi-stage, MMO-style boss fight with escalating tactical mechanics.

---

## 🛡️ The 4 Combat Stages

```mermaid
flowchart TD
    Phase1["🟢 Phase 1: Calm Encounter (100% → 75% HP)<br>• Gentle bobbing & festive chat lines<br>• Initial player engagement"]
    Phase2["🔵 Phase 2: Orbital Shield & Minion Swarm (75% → 50% HP)<br>• 100% Damage Immunity Barrier<br>• 3-5 Guardian Minions Spawned<br>• Must eliminate guardians to unlock boss"]
    Phase3["🔴 Phase 3: Enraged Shockwaves (50% → 25% HP)<br>• Fiery particle vortex<br>• Radial kinetic knockback pulses<br>• Lightning strike visual effects"]
    Phase4["🟣 Phase 4: Final Stand & Detonation (25% → 0% HP)<br>• Hyper-speed rotation<br>• Multi-tiered progressive loot explosion<br>• Ephemeral candy scatter & fireworks"]

    Phase1 --> Phase2
    Phase2 --> Phase3
    Phase3 --> Phase4
```

---

## 🛑 Phase 2: Orbital Invulnerability Shield

During Phase 2, the piñata deploys a spherical particle shield preventing all direct damage:

> [!WARNING]
> While the shield is active, direct attacks deal **0 damage** to the boss.  
> Players must focus down the **Guardian Minions** floating around the arena. Defeating all minions shatters the shield with an acoustic glass-break sound and exposes the boss to vulnerability.

---

## 💥 Phase 3: Radial Shockwave Mechanics

In Phase 3, the boss periodically emits outward kinetic pulses:

$$v_{\text{knockback}} = \frac{K_{\text{force}}}{\max(1.0, d)} \cdot \hat{r}$$

* $d$: Distance from the player to the piñata center ($m$).
* $\hat{r}$: Unit vector pointing radially outward from the boss.
* $K_{\text{force}}$: Configurable knockback coefficient in `pinatas/*.yml`.

---

<div align="space-between">

[**← 03. 3D Display Entities & Physics**](03-3D-Display-Entities-and-Physics.md) | [**05. Creating Custom Piñatas →**](05-Creating-Custom-Pinatas.md)

</div>