# 💻 12. Developer API & Event Hooks

PinataSpectra Sovereign provides a rich Java API and custom Bukkit/Paper event listeners for developers building server custom plugins or minigames.

---

## 📦 Maven & Gradle Setup

<!-- tabs:start -->

#### **Maven (`pom.xml`)**
```xml
<repositories>
  <repository>
    <id>pinataspectra-repo</id>
    <url>https://repo.pinataspectra.dev/releases</url>
  </repository>
</repositories>

<dependencies>
  <dependency>
    <groupId>com.pinataspectra</groupId>
    <artifactId>pinataspectra-api</artifactId>
    <version>1.0.0</version>
    <scope>provided</scope>
  </dependency>
</dependencies>
```

#### **Gradle (`build.gradle.kts`)**
```kotlin
repositories {
    maven("https://repo.pinataspectra.dev/releases")
}

dependencies {
    compileOnly("com.pinataspectra:pinataspectra-api:1.0.0")
}
```
<!-- tabs:end -->

---

## 🎯 Custom Event Listeners

PinataSpectra fires asynchronous and synchronous Bukkit events at key points during the boss lifecycle:

```java
import com.pinataspectra.api.event.PinataSpawnEvent;
import com.pinataspectra.api.event.PinataDamageEvent;
import com.pinataspectra.api.event.PinataPhaseChangeEvent;
import com.pinataspectra.api.event.PinataDeathEvent;
import org.bukkit.event.EventHandler;
import org.bukkit.event.Listener;

public class MyCustomBossPlugin implements Listener {

    @EventHandler
    public void onPinataSpawn(PinataSpawnEvent event) {
        String tierId = event.getPinata().getId();
        event.getPinata().getWorld().strikeLightningEffect(event.getPinata().getLocation());
    }

    @EventHandler
    public void onPinataDamage(PinataDamageEvent event) {
        if (event.isShieldAbsorbed()) {
            event.getPlayer().sendMessage("§cThe boss is shielded! Destroy the minions!");
        }
    }

    @EventHandler
    public void onPinataDeath(PinataDeathEvent event) {
        Player mvp = event.getTopDamager();
        if (mvp != null) {
            System.out.println("Boss defeated! MVP: " + mvp.getName());
        }
    }
}
```

---

<div align="space-between">

[**← 11. Commands & Placeholders**](11-Commands-Permissions-and-Placeholders.md) | [**13. Edition Comparison & Matrix →**](13-Comparison-and-Editions.md)

</div>