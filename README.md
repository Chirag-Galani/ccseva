# CCSeva 🤖

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub release](https://img.shields.io/github/release/Iamshankhadeep/ccseva.svg)](https://github.com/Iamshankhadeep/ccseva/releases)
[![Build Status](https://img.shields.io/github/actions/workflow/status/Iamshankhadeep/ccseva/ci.yml?branch=main)](https://github.com/Iamshankhadeep/ccseva/actions)
[![Downloads](https://img.shields.io/github/downloads/Iamshankhadeep/ccseva/total.svg)](https://github.com/Iamshankhadeep/ccseva/releases)
[![macOS](https://img.shields.io/badge/macOS-10.15%2B-blue)](https://github.com/Iamshankhadeep/ccseva)

A beautiful macOS menu bar app for tracking your Claude Code usage in real-time. Monitor token consumption, costs, and usage patterns with an elegant interface.

## Screenshots

![Dashboard](./screenshots/dashboard.png)
![Analytics](./screenshots/analytics.png)
![Terminal](./screenshots/terminal.png)

## Features

- **Real-time monitoring** - Live token usage tracking with 30-second updates
- **Menu bar integration** - Percentage indicator with color-coded status
- **Smart plan detection** - Auto-detects Pro/Max5/Max20/Custom plans
- **Updated token limits** - Pro: 44k, Max5: 88k, Max20: 220k (2026 limits)
- **Accurate tracking** - Cache tokens excluded from usage calculations
- **Usage analytics** - 7-day charts, model breakdowns, and trend analysis
- **Smart notifications** - Alerts at 70% and 90% thresholds with cooldown
- **Cost tracking** - Daily cost estimates and burn rate calculations
- **Beautiful UI** - Gradient design with glass morphism effects

## Token Limits (2026)

CCSeva uses the updated Claude token limits:

| Plan | Tokens/Session | Monthly Cost |
|------|---------------|--------------|
| **Pro** | 44,000 | $20 |
| **Max5** | 88,000 | $100 |
| **Max20** | 220,000 | $200 |
| **Custom** | User-defined | - |

> **Note:** Cache read/write tokens are **excluded** from usage calculations for accurate tracking.

## Installation

### Download (Recommended)
Download the latest release from [GitHub Releases](https://github.com/Iamshankhadeep/ccseva/releases):
- **macOS (Apple Silicon)**: `ccseva-apple-silicon-1.3.1.dmg`

### ⚠️ First Launch - Bypass Gatekeeper

macOS will show **"CCSeva is damaged"** because the app is not signed with an Apple Developer certificate.

**Option 1: Terminal Command (Quickest)**
```bash
xattr -cr /Applications/CCSeva.app
```

**Option 2: System Settings**
1. Try to open CCSeva (it will be blocked)
2. Open **System Settings** → **Privacy & Security**
3. Scroll down and click **"Open Anyway"** next to CCSeva
4. Click **"Open"** in the confirmation dialog

After this one-time step, CCSeva will launch normally! ✨

### Build from Source
```bash
git clone https://github.com/Iamshankhadeep/ccseva.git
cd ccseva
npm install
npm run build
npm start
```

### Development
```bash
npm run electron-dev  # Hot reload development
```

## Usage

1. **Launch** - CCSeva appears in your menu bar
2. **Click** - View detailed usage statistics
3. **Right-click** - Access refresh and quit options

The app automatically detects your Claude Code configuration from `~/.claude` directory and updates every 30 seconds.

## Requirements

- macOS 10.15+
- Node.js 18+ (for building from source)
- Claude Code CLI installed and configured

## Tech Stack

- Electron 36 + React 19 + TypeScript 5
- Tailwind CSS 3 + Radix UI components
- ccusage package for data integration

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Credits

Built with ❤️ using [Electron](https://electronjs.org), [React](https://reactjs.org), [Tailwind CSS](https://tailwindcss.com), and [ccusage](https://github.com/ryoppippi/ccusage).

---

**Note**: This is an unofficial tool for tracking Claude Code usage. Requires valid Claude Code installation and configuration.