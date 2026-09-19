# ⚙️ 02. Installation & Server Setup

This guide provides step-by-step instructions for installing and configuring PinataSpectra Sovereign Edition on your Minecraft server environment.

---

## 📋 System & Server Requirements

| Component | Minimum Requirement | Recommended Specification |
| :--- | :--- | :--- |
| **Server Software** | Paper / Purpur 1.20.1+ | Purpur / Folia 1.21.4+ |
| **Java Runtime** | Java 17 | Java 21 (GraalVM Enterprise recommended) |
| **CPU Allocation** | 2 Dedicated Cores (3.5+ GHz) | 4+ Dedicated Cores (4.5+ GHz) |
| **RAM Allocation** | 4 GB | 8 GB+ |

---

## 📦 Soft & Optional Dependencies

PinataSpectra works completely standalone out-of-the-box, but seamlessly integrates with the following plugins if detected:

* **[Vault](https://www.spigotmc.org/resources/vault.34315/):** Enables dynamic economy money drops upon piñata hits and boss defeat.
* **[PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/):** Exposes 20+ real-time placeholders for scoreboards, tablists, and custom chat formats.
* **[DecentHolograms](https://www.spigotmc.org/resources/decentholograms.96927/) / [FancyHolograms](https://www.spigotmc.org/resources/fancyholograms.107777/):** Renders dynamic floating holographic leaderboards and live combat health bars.
* **[NuVotifier](https://www.spigotmc.org/resources/nuvotifier.13444/):** Connects your server voting listeners directly to the automated Piñata Vote Party engine.

---

## 🛠️ Step-by-Step Installation

<!-- tabs:start -->

#### **Step 1: Download Jar**
Place `PinataSpectra-1.0.0-RELEASE-pro.jar` directly into your server's `/plugins/` directory.

#### **Step 2: First Boot**
Start or restart your server to generate default configuration files:
```bash
# Start your Paper/Purpur server
java -Xms4G -Xmx8G -XX:+UseG1GC -jar server.jar nogui
```

#### **Step 3: Verification**
Verify successful initialization in console:
```log
[PinataSpectra] Enabling PinataSpectra v1.0.0-RELEASE (Sovereign Edition)
[PinataSpectra] [License] Proprietary Enterprise License Verified.
[PinataSpectra] [Physics] Initializing 3D Display Entity Kinematics Engine... OK
[PinataSpectra] [Database] Connected to SQLite database (pinata_data.db) in 12ms.
[PinataSpectra] PinataSpectra initialized successfully in 0.042s!
```
<!-- tabs:end -->

---

## 🗂️ Generated Folder Structure

```
plugins/PinataSpectra/
├── config.yml              # Master server settings & database credentials
├── messages.yml            # Fully customizable localized chat & boss phrases
├── gui.yml                 # Interactive GUI menu layouts
├── pinatas/                # Custom Piñata tier definitions
│   ├── common_donkey.yml
│   ├── cosmic_unicorn.yml
│   └── infernal_dragon.yml
└── database/               # Local SQLite database (if MySQL is disabled)
```

---

<div align="space-between">

[**← 01. Architecture & Performance**](01-Architecture-and-Performance.md) | [**03. 3D Display Entities & Physics →**](03-3D-Display-Entities-and-Physics.md)

</div>