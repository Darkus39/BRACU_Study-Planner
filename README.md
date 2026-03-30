> **[🖥️ Prefer a visual README? Click here for the GUI version →](https://bracu-study-planner.vercel.app/)**

---

# 🎓 BRACU Study Planner v2.0

> Academic management system for BRACU students — Java 21 · Spring Boot 3.2 · JavaFX 21

[![Java](https://img.shields.io/badge/Java-21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.2.4-6DB33F?style=flat-square&logo=spring-boot&logoColor=white)](https://spring.io/projects/spring-boot)
[![JavaFX](https://img.shields.io/badge/JavaFX-21.0.2-007396?style=flat-square)](https://openjfx.io/)
[![Platform](https://img.shields.io/badge/Platform-Win%20·%20Mac%20·%20Linux-555?style=flat-square)](https://github.com/Darkus39/BRACU_Study-Planner)

---

## What It Does

| Feature | Description |
| --- | --- |
| 📊 Dashboard | Live CGPA tracker, semester overview, and progress stats at a glance |
| 📚 Course Manager | Add, edit, and track courses from a built-in BRACU database of ~340 courses |
| 🗓️ Study Schedule | Auto-generated study schedules and topic roadmaps per course |
| 🎯 CGPA Forecast | Target CGPA simulation — see exactly what grades you need to hit your goal |
| 💾 Local Persistence | All data saved locally as JSON. Never leaves your device |
| 🌑 Dark UI | Fully custom dark theme with Syne + JetBrains Mono typography |

---

## One-Click Installers

Download the repo, place the script in the `StudyPlannerFX/` folder, and run it. Java and Maven are installed automatically if missing.

### 🪟 Windows
```
# Right-click install-windows.bat → Run as Administrator
# Required for winget to install JDK/Maven if not present
```

Manual:
```
winget install Microsoft.OpenJDK.21
winget install Apache.Maven
cd StudyPlannerFX && mvn javafx:run
```

### 🍎 macOS
```
chmod +x install-macos.sh && ./install-macos.sh
# Works on Intel & Apple Silicon. Installs Homebrew, JDK 21, Maven if needed.
```

Manual:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install --cask temurin@21
brew install maven
cd StudyPlannerFX && mvn javafx:run
```

### 🐧 Linux
```
chmod +x install-linux.sh && ./install-linux.sh
# Auto-detects apt (Ubuntu/Debian) or dnf (Fedora/RHEL). Sudo required.
```

Manual — Ubuntu/Debian:
```
sudo apt update && sudo apt install openjdk-21-jdk maven
cd StudyPlannerFX && mvn javafx:run
```

Manual — Fedora/RHEL:
```
sudo dnf install java-21-openjdk-devel maven
cd StudyPlannerFX && mvn javafx:run
```

---

## Developer Commands
```
# Run in dev mode (fastest)
mvn javafx:run

# Build fat JAR then run
mvn clean package
java -jar target/StudyPlannerFX-2.0.0.jar

# Build native installer — Linux / macOS
chmod +x build-installer.sh && ./build-installer.sh

# Build native installer — Windows
.\build-installer.bat
```

---

## Native Installer (No Java Required for End Users)

Use `build-installer.sh / .bat` to produce a platform-native package with a bundled JRE.

| Platform | Output | Install |
| --- | --- |
| Windows | `.exe` installer | Double-click to install |
| macOS | `.dmg` disk image | Open → drag to Applications |
| Fedora / RHEL | `.rpm` package | `sudo dnf install *.rpm` |
| Ubuntu / Debian | `.deb` package | `sudo dpkg -i *.deb` |

---

## Data Storage

All student data is saved locally as human-readable JSON. Nothing is ever sent to any server.

| OS | Location |
| --- | --- |
| Windows | `%USERPROFILE%\Documents\BRACUStudyPlanner\student_data.json` |
| macOS | `~/Documents/BRACUStudyPlanner/student_data.json` |
| Linux | `~/BRACUStudyPlanner/student_data.json` |

---

## Project Structure
```
StudyPlannerFX/
├── install-windows.bat
├── install-macos.sh
├── install-linux.sh
├── build-installer.sh / .bat
├── pom.xml
└── src/main/java/com/bracu/studyplanner/
    ├── app/
    │   ├── Launcher.java
    │   ├── StudyPlannerApp.java
    │   └── SpringConfig.java
    ├── model/
    │   ├── Student.java
    │   ├── CourseEntry.java
    │   └── SemesterInfo.java
    ├── service/
    │   ├── StudentService.java
    │   ├── CgpaService.java
    │   ├── CourseRepository.java
    │   ├── PersistenceService.java
    │   └── ScheduleService.java
    └── view/
        ├── screens/
        │   ├── SetupScreen.java
        │   ├── MainScreen.java
        │   └── tabs/
        │       ├── DashboardTab.java
        │       ├── CoursesTab.java
        │       ├── ScheduleTab.java
        │       └── SettingsTab.java
        └── components/
            ├── FormField.java
            ├── StatCard.java
            └── StatusBadge.java
```

---

Built by [Ayanokouji](https://github.com/Darkus39) · Founder @ [Spectre Flow](https://spectre-flow-website.vercel.app) · CSE Undergrad Y2
