# Proctly - Desktop Application Downloads

[![Latest Release](https://img.shields.io/github/v/release/i-internet/proctly.com?label=Latest%20Version)](https://github.com/i-internet/proctly.com/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/i-internet/proctly.com/total?label=Total%20Downloads)](https://github.com/i-internet/proctly.com/releases)

**Proctly** is an advanced online proctoring desktop application designed for secure exam monitoring. This repository hosts the official release builds for Windows, macOS, and Linux.

---

## Download Latest Version

| Platform | Download | Architecture |
|----------|----------|--------------|
| **Windows** | [Download .exe](https://github.com/i-internet/proctly.com/releases/latest/download/Proctly.Setup.3.0.5.exe) | 64-bit |
| **Windows** | [Download .exe (32-bit)](https://github.com/i-internet/proctly.com/releases/latest/download/Proctly.Setup.3.0.5.ia32.exe) | 32-bit |
| **macOS** | [Download .dmg](https://github.com/i-internet/proctly.com/releases/latest/download/Proctly-3.0.5-arm64.dmg) | ARM64 |
| **Linux** | [Download .AppImage](https://github.com/i-internet/proctly.com/releases/latest/download/Proctly-3.0.5.AppImage) | 64-bit |
| **Linux** | [Download .deb](https://github.com/i-internet/proctly.com/releases/latest/download/proctly.com_3.0.5_amd64.deb) | 64-bit (Debian/Ubuntu) |

> **Note:** For the most up-to-date download links, always check the [Releases page](https://github.com/i-internet/proctly.com/releases).

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

1. Download the `.exe` installer from the [Releases page](https://github.com/i-internet/proctly.com/releases)
2. Run the installer (`Proctly Setup X.X.X.exe`)
3. Follow the installation wizard
4. Choose installation directory (optional)
5. Launch Proctly from the Start Menu or Desktop shortcut

### macOS

1. Download the `.dmg` file from the [Releases page](https://github.com/i-internet/proctly.com/releases)
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

All releases are available on the [Releases page](https://github.com/i-internet/proctly.com/releases).

### Version Numbering

- **Major (X.0.0)** - Significant new features or breaking changes
- **Minor (0.X.0)** - New features, backward compatible
- **Patch (0.0.X)** - Bug fixes and minor improvements

---

## For Developers

### Technology Stack

- **Framework:** Electron 27.x
- **Runtime:** Node.js 18.x
- **Build Tool:** electron-builder 24.x
- **UI:** Bootstrap 5.3, SweetAlert2
- **Storage:** electron-store
- **Face Detection:** face-api.js

### Local Development Setup

```bash
# Clone the repository
git clone https://github.com/i-internet/monitoring-app-client.git
cd monitoring-app-client

# Install dependencies
npm install

# Run in development mode (with hot reload)
npm run dev

# Run normally
npm start
```

### API Configuration

In `main.js`, switch the `API_BASE_URL` depending on environment:

```javascript
// Production
var API_BASE_URL = 'https://api.proctly.com/proctor/api';

// Local development
// var API_BASE_URL = 'http://localhost:8080/monitoring-app-server/proctor/api';

// ngrok tunnel (for mobile/remote testing)
// var API_BASE_URL = 'https://your-tunnel.ngrok-free.app/monitoring-app-server/proctor/api';
```

> **Important:** Always make sure `API_BASE_URL` points to **production** before committing and pushing.

### Local Builds

```bash
# Windows 64-bit
npm run build:win

# Windows 32-bit
npm run build:win32

# macOS
npm run build:mac

# Linux AppImage
npm run build:linux-appimage

# Linux .deb
npm run build:linux-deb
```

Build output goes to the `dist/` folder.

### Deploying a New Release (CI/CD)

The project uses **GitHub Actions** to automatically build and release for all platforms. Here's how to push a new version:

#### Step 1: Make your changes

Edit the code as needed (e.g., `main.js`, HTML files, etc.)

#### Step 2: Bump the version in `package.json`

```json
"version": "X.Y.Z"
```

#### Step 3: Commit and push

```bash
git add main.js package.json          # Add changed files
git commit -m "vX.Y.Z - Description of changes"
git push origin main
```

#### Step 4: Tag and push the tag (triggers the build)

```bash
git tag vX.Y.Z
git push origin vX.Y.Z
```

> **This is the key step!** Pushing a `v*` tag triggers the GitHub Actions workflow which:
> 1. Builds **Windows** (.exe x64 + x32) on `windows-latest`
> 2. Builds **macOS** (.dmg + .zip) on `macos-latest`
> 3. Builds **Linux** (.AppImage + .deb) on `ubuntu-latest`
> 4. Creates a **GitHub Release** in the public repo [`i-internet/proctly.com`](https://github.com/i-internet/proctly.com) with all artifacts
> 5. Syncs `Builds.md` as README to the public repo

#### If a build fails and you need to re-tag

```bash
# Delete the old tag locally and remotely
git tag -d vX.Y.Z
git push origin :refs/tags/vX.Y.Z

# Fix the issue, commit, and push
git add .
git commit -m "vX.Y.Z - Fix description"
git push origin main

# Re-create and push the tag
git tag vX.Y.Z
git push origin vX.Y.Z
```

#### Manual trigger (without tagging)

You can also trigger the build manually from the **GitHub Actions tab** → **Build and Release** → **Run workflow**. Note: manual triggers will build but won't create a release (releases require a tag).

### Build Pipeline Overview

```
git push origin vX.Y.Z
        │
        ▼
┌─────────────────────────────────────────────┐
│           GitHub Actions Workflow             │
├──────────┬──────────┬───────────────────────┤
│ Windows  │  macOS   │  Linux                │
│ .exe x64 │  .dmg    │  .AppImage            │
│ .exe x32 │  .zip    │  .deb                 │
└────┬─────┴────┬─────┴────┬──────────────────┘
     │          │          │
     ▼          ▼          ▼
┌─────────────────────────────────────────────┐
│  Release created in i-internet/proctly.com  │
│  with all build artifacts attached          │
└─────────────────────────────────────────────┘
```

### Project Structure

```
monitoring-app-client/
├── main.js                  # Electron main process (core app logic)
├── preload.js               # IPC bridge between main and renderer
├── errorLogger.js           # Centralized error logging
├── package.json             # Dependencies, scripts, build config
│
├── registration.html/js     # Student login with token
├── consent.html/js          # Permission consent screen
├── welcome.html             # Welcome screen
├── splash.html/js           # Splash/onboarding screen
├── test-preview.html/js     # Pre-test permissions check
├── session-qr.html/js       # QR code and photo capture
├── test-environment.html/js # Main monitoring interface
├── renderer.js              # Webcam and screen capture
├── index.html               # Test webview container
├── styles.css               # Global styles
│
├── build/                   # App icons (icon.ico, icon.png)
├── images/                  # Branding assets
├── .github/workflows/       # CI/CD pipeline
│   └── build.yml            # Build and release workflow
└── dist/                    # Build output (gitignored)
```

---

## License

Proctly is proprietary software. All rights reserved.

- The application binaries are provided for authorized use only
- Redistribution without permission is prohibited
- Use is subject to your institution's license agreement

---

## Links

- **Releases:** [GitHub Releases](https://github.com/i-internet/proctly.com/releases)
- **Website:** [proctly.com](https://proctly.com)

---

*Last updated: February 2026*
