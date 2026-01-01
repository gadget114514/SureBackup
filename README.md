# Introduction: SureBackup

SureBackup is a professional, native Win32 application designed for robust folder synchronization and data integrity. Built from the ground up for the Windows environment, it provides a high-performance alternative to generic backup tools, offering bit-perfect mirroring with strict adherence to NTFS file system specifics.

Whether you are managing large-scale server backups or synchronizing personal local drives, SureBackup provides the precision and transparency required for enterprise-grade data management.

## 🌟 Core Value Proposition

*   **Native Performance**: Leverages pure Win32 APIs for a zero-dependency, high-speed execution.
*   **Data Fidelity**: Preserves the complete identity of your files, including Alternate Data Streams (ADS), Symbolic Links, and exact timestamps.
*   **High-Speed Parallelism**: A modern multithreaded engine that saturates storage bandwidth while providing granular monitoring.
*   **Total Transparency**: Every action is logged and verified, ensuring you have a complete audit trail of your backup session.

*   **Native Precision**: Built 100% with the Win32 API. No heavy frameworks, just pure Windows performance.
*   **High-Speed Parallel Engine**: Multithreaded backup and synchronization engine with real-time worker dashboards and aggregate progress tracking.
*   **Advanced NTFS Support**: Full support for **Alternate Data Streams (ADS)** and **Symbolic Links** (files and directories).
*   **Bit-Perfect Verification**: Optional 16KB block-level byte-by-byte comparison to ensure data integrity beyond simple timestamp checks.
*   **High-Fidelity Metadata**: Strictly preserves file/directory modification and creation times.
*   **Flexible Sync Modes**:
    *   **Copy (Append)**: Process only new or updated files.
    *   **Sync (Mirror)**: Perfectly mirror source to target, including orphan removal.
    *   **Verify Only**: Simulation/Preview pass without any file modifications.
*   **Globalized**: Fully localized for **English, Japanese, French, German, and Spanish**.
*   **Reliable Scheduling**: Integrated daily/weekly task scheduler with persistence.

## 🛠 Multi-Engine Architecture

SureBackup dynamically selects the best strategy for your task:
- **Standard**: Sequential processing for maximum stability on any media.
- **Parallel**: Optimized for SSDs and high-speed networks using a producer-consumer worker pool.
- **Comparison**: Dedicated integrity checking engine.
- **Experimental**: Support for VSS (Snapshot) and Block Clone strategies.

## 🖥 User Interface

*   **Management Tree**: Organize and batch process multiple "Backup Units" grouped into "Backup Sets".
*   **Integrated Explorers**: Quick-select source and target folders using the built-in file system discovery trees.
*   **Task Dashboard**: Detailed execution logs with a "Maximize" mode for deep review.
*   **Quick Edit**: Change backup modes and engines directly from the main window without nesting deep into dialogs.

## 📂 Project Structure

- `src/`: Core Win32 application logic and backup engines.
- `src/Strategies/`: Modular implementations of different backup/sync strategies.
- `doc/`: Detailed requirements, architecture, and UI mappings.

## 🏗 Build Requirements

- **Platform**: Windows 10/11
- **Compiler**: MSVC (C++17 recommended)
- **Build System**: CMake

```powershell
mkdir build
cd build
cmake ..
cmake --build . --config Release
```

## ⚖ License

Copyright (c) 2026. All rights reserved.
