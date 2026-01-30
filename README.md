# Proctly - Desktop Application Downloads

[![Latest Release](https://img.shields.io/github/v/release/i-internet/monitoring-app-server-builds?label=Latest%20Version)](https://github.com/i-internet/monitoring-app-server-builds/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/i-internet/monitoring-app-server-builds/total?label=Total%20Downloads)](https://github.com/i-internet/monitoring-app-server-builds/releases)

**Proctly** is an advanced online proctoring desktop application designed for secure exam monitoring. This repository hosts the official release builds for Windows, macOS, and Linux.

---

## Download Latest Version

| Platform | Download | Architecture |
|----------|----------|--------------|
| **Windows** | [Download .exe](https://github.com/i-internet/monitoring-app-server-builds/releases/latest/download/Proctly.Setup.3.0.0.exe) | 64-bit |
| **Windows** | [Download .exe (32-bit)](https://github.com/i-internet/monitoring-app-server-builds/releases/latest/download/Proctly.Setup.3.0.0.ia32.exe) | 32-bit |
| **macOS** | [Download .dmg](https://github.com/i-internet/monitoring-app-server-builds/releases/latest/download/Proctly-3.0.0.dmg) | Universal |
| **Linux** | [Download .AppImage](https://github.com/i-internet/monitoring-app-server-builds/releases/latest/download/Proctly-3.0.0.AppImage) | 64-bit |
| **Linux** | [Download .deb](https://github.com/i-internet/monitoring-app-server-builds/releases/latest/download/proctly.com_3.0.0_amd64.deb) | 64-bit (Debian/Ubuntu) |

> **Note:** For the most up-to-date download links, always check the [Releases page](https://github.com/i-internet/monitoring-app-server-builds/releases).

---

## What is Proctly?

Proctly is a comprehensive desktop proctoring solution that enables educational institutions and organizations to conduct secure online examinations. The application runs on the student's computer and provides real-time monitoring capabilities to ensure exam integrity.

### Key Features

#### Real-Time Monitoring
- **Screen Capture** - Periodic screenshots of all connected monitors
- **Webcam Recording** - Continuous webcam feed capture with face detection
- **Audio Recording** - Optional microphone monitoring during exams
- **Multi-Monitor Support** - Detects and captures all connected displays

#### Security Features
- **Kiosk Mode** - Locks the user into the exam environment
- **Application Blocking** - Prevents switching to other applications
- **Keyboard Shortcut Blocking** - Disables Alt+Tab, Win+D, and other shortcuts
- **Copy/Paste Monitoring** - Tracks and optionally restricts clipboard usage
- **URL Monitoring** - Tracks navigation within the test environment

#### AI-Powered Detection
- **Face Detection** - Ensures the registered student is present
- **Multiple Face Detection** - Alerts when additional people are detected
- **No Face Detection** - Alerts when the student leaves the frame

#### Violation Tracking
- **Window Focus Loss** - Detects when user clicks outside the exam
- **Application Switching** - Logs attempts to switch applications
- **Minimize Attempts** - Prevents and logs minimize attempts
- **Screenshot Capture on Violations** - Automatic evidence collection

#### User Experience
- **Embedded Test Browser** - Secure webview for test content
- **Navigation Controls** - Back, forward, refresh, zoom controls
- **Quick Links** - Easy access to allowed resources
- **Session Timer** - Displays elapsed exam time
- **Draggable Webcam Preview** - Adjustable webcam position

---

## System Requirements

### Windows
- **OS:** Windows 10 or later (64-bit recommended)
- **RAM:** 4 GB minimum, 8 GB recommended
- **Storage:** 500 MB free space
- **Webcam:** Required for proctored exams
- **Microphone:** Required if audio monitoring is enabled
- **Internet:** Stable broadband connection

### macOS
- **OS:** macOS 10.13 (High Sierra) or later
- **RAM:** 4 GB minimum, 8 GB recommended
- **Storage:** 500 MB free space
- **Webcam:** Built-in or external webcam
- **Microphone:** Built-in or external microphone
- **Internet:** Stable broadband connection

### Linux
- **OS:** Ubuntu 18.04+, Debian 10+, Fedora 32+, or compatible
- **RAM:** 4 GB minimum, 8 GB recommended
- **Storage:** 500 MB free space
- **Webcam:** USB or built-in webcam
- **Microphone:** USB or built-in microphone
- **Internet:** Stable broadband connection

---

## Installation Instructions

### Windows

1. Download the `.exe` installer from the [Releases page](https://github.com/i-internet/monitoring-app-server-builds/releases)
2. Run the installer (`Proctly Setup X.X.X.exe`)
3. Follow the installation wizard
4. Choose installation directory (optional)
5. Launch Proctly from the Start Menu or Desktop shortcut

### macOS

1. Download the `.dmg` file from the [Releases page](https://github.com/i-internet/monitoring-app-server-builds/releases)
2. Open the `.dmg` file
3. Drag Proctly to the Applications folder
4. On first launch, right-click and select "Open" (required for unsigned apps)
5. Grant necessary permissions (Camera, Microphone, Screen Recording)

### Linux

**AppImage (Universal):**
```bash
# Download the AppImage
chmod +x Proctly-X.X.X.AppImage
./Proctly-X.X.X.AppImage
```

**Debian/Ubuntu (.deb):**
```bash
sudo dpkg -i proctly.com_X.X.X_amd64.deb
sudo apt-get install -f  # Install dependencies if needed
```

---

## How Proctly Works

### Architecture Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                     PROCTLY ECOSYSTEM                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌──────────────┐    ┌──────────────┐    ┌──────────────┐      │
│  │   Student    │    │   Proctly    │    │   Proctly    │      │
│  │   Desktop    │◄──►│   Backend    │◄──►│   Dashboard  │      │
│  │     App      │    │    Server    │    │  (Proctor)   │      │
│  └──────────────┘    └──────────────┘    └──────────────┘      │
│         │                   │                    │               │
│         │                   │                    │               │
│         ▼                   ▼                    ▼               │
│  • Screen Capture    • Data Storage      • Live Monitoring      │
│  • Webcam Feed       • Violation Logs    • Violation Alerts     │
│  • Audio Recording   • Session Mgmt      • Student Review       │
│  • Face Detection    • Authentication    • Reports              │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Exam Flow

1. **Registration**
   - Student opens Proctly and enters credentials
   - Identity verification via webcam photo
   - QR code scanning for mobile webcam (optional)

2. **Pre-Exam Setup**
   - System compatibility check
   - Webcam and microphone permissions
   - Face detection calibration
   - Test environment preview

3. **During Exam**
   - Secure webview loads the test content
   - Continuous monitoring (screen, webcam, audio)
   - Real-time face detection
   - Violation tracking and logging

4. **Post-Exam**
   - Session data uploaded to server
   - Monitoring data synchronized
   - Session closed and cleared

### Auto-Update System

Proctly includes an automatic update system that checks for new versions on startup:

```
┌─────────────┐     ┌─────────────┐     ┌─────────────────────┐
│   Proctly   │────►│   GitHub    │────►│  This Repository    │
│    App      │     │    Gist     │     │  (Download Files)   │
└─────────────┘     └─────────────┘     └─────────────────────┘
      │                   │                       │
      │                   │                       │
      ▼                   ▼                       ▼
 Checks version      Contains latest        Hosts installer
 on startup          version info           files for all
                     and download URLs      platforms
```

1. App fetches version info from a GitHub Gist
2. Compares with current installed version
3. If newer version available, prompts user to update
4. Downloads installer from this repository
5. Runs installer to update the application

---

## Security & Privacy

### Data Collection

Proctly collects the following data during proctored sessions:

| Data Type | Purpose | Storage |
|-----------|---------|---------|
| Screenshots | Exam integrity verification | Encrypted server storage |
| Webcam images | Identity verification | Encrypted server storage |
| Audio (optional) | Environment monitoring | Encrypted server storage |
| Violation logs | Incident documentation | Encrypted server storage |
| Session metadata | Analytics and debugging | Encrypted server storage |

### Data Protection

- All data is transmitted over HTTPS (TLS 1.2+)
- Data is stored on secure, encrypted servers
- Access is restricted to authorized proctors only
- Data retention follows institutional policies
- GDPR and FERPA compliant

### Permissions Required

| Permission | Purpose |
|------------|---------|
| Camera | Face detection and identity verification |
| Microphone | Audio environment monitoring |
| Screen Recording | Screenshot capture for review |
| Network | Communication with proctoring server |

---

## Troubleshooting

### Common Issues

**App won't start:**
- Ensure your system meets minimum requirements
- Try running as administrator (Windows)
- Check if antivirus is blocking the application

**Webcam not detected:**
- Ensure webcam is connected and working
- Grant camera permissions in system settings
- Close other apps that might be using the webcam

**Face detection not working:**
- Ensure adequate lighting
- Position face clearly in the webcam frame
- Remove obstructions (hats, sunglasses)

**Connection issues:**
- Check internet connectivity
- Verify firewall isn't blocking the app
- Contact your institution's IT support

### Getting Help

- **Technical Support:** Contact your institution's exam administrator
- **Bug Reports:** Report issues through your institution

---

## Release History

All releases are available on the [Releases page](https://github.com/i-internet/monitoring-app-server-builds/releases).

### Version Numbering

- **Major (X.0.0)** - Significant new features or breaking changes
- **Minor (0.X.0)** - New features, backward compatible
- **Patch (0.0.X)** - Bug fixes and minor improvements

---

## For Developers

### Build Information

This repository only contains release binaries. The source code is maintained in a private repository.

**Build Pipeline:**
- Builds are automated using GitHub Actions
- Cross-platform builds: Windows, macOS, Linux
- Artifacts are automatically uploaded on tagged releases

**Technology Stack:**
- **Framework:** Electron 27.x
- **Runtime:** Node.js 18.x
- **Build Tool:** electron-builder
- **Face Detection:** face-api.js

---

## License

Proctly is proprietary software. All rights reserved.

- The application binaries are provided for authorized use only
- Redistribution without permission is prohibited
- Use is subject to your institution's license agreement

---

## Links

- **Releases:** [GitHub Releases](https://github.com/i-internet/monitoring-app-server-builds/releases)
- **Website:** [proctly.com](https://proctly.com)

---

*Last updated: January 2026*
