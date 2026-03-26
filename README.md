# 🛰️ BRACU Study Planner v2.0

> **[ 🖥️ CLICK HERE TO OPEN THE FULL INTERACTIVE README ](https://darkus39.github.io/BRACU_Study-Planner/)**
>
> *View the specialized Cyber-Mecha UI, installation guides, and architecture tree.*

<br>

### // ⚡ QUICK START & EXTRACTION

The core automation scripts and application files are bundled within this repository. To begin your setup:

<br>

1. **Download/Clone** the repository to your local machine (Optimized for Fedora, Kali, and Windows environments).

<br>

2. **Extract All Content:** If you downloaded the project as a `.zip` file, ensure you extract it to a dedicated folder rather than running files from within the archive.

<br>

3. **Maintain Directory Integrity:** It is crucial that the installer scripts (`.sh` / `.bat`) remain in the same root directory as the `src/` folder. Moving scripts to the desktop individually will break the automated dependency paths.

<br>

4. **Execute Installer:** Run the script corresponding to your operating system. The automation layer will handle JDK 21 and Maven configuration if they are not detected on your system.

<br>

### // 🛠️ CORE FEATURES

<br>

* **Dynamic Dashboard:** Real-time CGPA tracking and automated semester summaries with progress visualization.

<br>

* **Course Intelligence:** A pre-loaded database featuring ~340 BRACU courses for instant management and academic planning.

<br>

* **Agentic Scheduling:** Auto-generated study roadmaps and topic-wise schedules tailored to your course load.

<br>

* **Linux Stability Fix:** Includes a specialized `Platform.runLater()` implementation to prevent UI deadlocks on Fedora 43/GTK environments.

<br>

// 🔑 SYSTEM REQUIREMENTS

<br>

Java Runtime: Version 21 (Automated detection and install included).

Build Tool: Maven 3.9+ (Configured automatically via installation scripts).

Hardware: Compatible with x64 and ARM64 architectures.

<br>

### // 📂 REPOSITORY STRUCTURE

<br>

```text
StudyPlannerFX/
├── install-windows.bat   <-- Run as Administrator (Windows)
├── install-linux.sh      <-- Run on Fedora/Kali (chmod +x)
├── install-macos.sh      <-- Run on Apple Silicon/Intel
├── build-installer.sh    <-- Native Jpackage Builder
└── src/                  <-- Source Code & Internal Assets

