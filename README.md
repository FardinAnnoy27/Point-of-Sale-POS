# SmartPOS — Android Point of Sale (POS) Application

SmartPOS is a native Android application designed for retail shops, inventory management, and field services to automate sales and billing operations. The application seamlessly integrates with Bluetooth thermal printers to generate real-time invoices and receipts on the go.

## 🚀 Key Features
- **Mobile Point of Sale (POS):** Efficiently process sales transactions directly from an Android device.
- **Bluetooth Printer Integration:** Uses the Woosim systems mobile driver library for wireless on-spot receipt printing.
- **Offline Capability:** Process and manage core transaction data locally on the device without active internet.
- **Optimized & Secure:** ProGuard rules are applied to minimize application size and protect source code via obfuscation.

---

## 🏗️ Architecture & Project Structure

The project follows a standard native Android architecture built using the modern Gradle build system. Here is the structural layout of the codebase:
SmartPOS/
├── app/                        # Main Application Module
│   ├── libs/

│   │   └── WoosimLib231.jar    # Woosim Mobile Printer SDK/Driver
│   ├── release/

│   │   └── app-release.apk     # Final compiled production package
│   ├── build.gradle            # App-level module configuration & SDK targets
│   └── proguard-rules.pro      # Code shrinking, optimization, and obfuscation rules
├── gradle/                     # Gradle wrapper directory for build automation
├── build.gradle                # Top-level build file configuring global dependencies (AGP v8.7.0)
├── settings.gradle             # Defines root project name and includes app modules
└── gradle.properties           # Project-wide JVM memory configuration & AndroidX settings

### Component Breakdown:
1. **Hardware Integration Layer (`app/libs/`):** Houses the `WoosimLib231.jar` SDK, which manages low-level Bluetooth communication and print commands for physical thermal printers.
2. **Build Configurations (`build.gradle` & `settings.gradle`):** Managed via Android Gradle Plugin (AGP) version `8.7.0` utilizing `google()` and `mavenCentral()` to fetch safe development libraries.
3. **Jetifier & AndroidX Ready:** Configured inside `gradle.properties` to ensure backwards compatibility with legacy third-party support libraries.

---

## 🛠️ Technology Stack
- **Platform:** Native Android
- **Build Automation System:** Gradle (v8.7.0)
- **IDE:** Android Studio
- **External Dependency:** Woosim Mobile Thermal Printer SDK


📄 License
This project is built as an enterprise utility application for retail and smart point of sale automation. All rights reserved.
