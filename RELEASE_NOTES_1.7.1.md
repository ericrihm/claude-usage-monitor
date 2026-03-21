## v1.7.1 — Security & Stability Release

This release focuses on security hardening, bug fixes, and enhanced reliability. While there are no major new features, 1.7.1 includes significant improvements to app security and user experience.

### Security Enhancements
- **macOS Code Signing**: Builds are now properly signed with Developer ID and notarized by Apple — no more Gatekeeper warnings
- **Content Security Policy**: Renderer process locked to self-only resources, preventing external code injection
- **OS Keychain Integration**: Session credentials now stored securely using Windows DPAPI and macOS Keychain
- **URL Validation**: External links restricted to allowlist (claude.ai, github.com, paypal.me)
- **Bundled Fonts**: Google Fonts dependency removed — Libre Baskerville bundled locally
- **History Rotation Cap**: 10,000-sample limit prevents unbounded storage growth

### New Features
- **Configurable Refresh Interval**: Set auto-refresh frequency (15s, 30s, 1min, 2min, 5min) via settings
- **Dynamic Threshold Colors**: All usage bars now display orange/red based on warning/danger thresholds
- **Compact Mode Refresh Button**: Visible refresh button with spin animation in compact mode

### Bug Fixes & Improvements
- **Always-on-Top Fix**: Periodic re-assertion (5-second interval) prevents window from falling behind other apps
- **Settings Panel Crash**: Fixed undefined `refreshInterval` crash in electron-store
- **Compact Mode Stability**: No longer expands to full size on data refresh
- **Graph Redraw**: Time format changes now immediately update the graph
- **Login Screen UI**: Settings/refresh/graph buttons properly hidden during login
- **State Persistence**: Graph and expanded rows state correctly restored across restarts
- **Timer Management**: Countdown timer properly stopped on logout
- **Alert State Reset**: New sessions no longer inherit suppressed alerts from previous logins
- **In-Flight Fetch Guard**: Overlapping API calls now dropped instead of queued

### Platform-Specific
- **macOS**: Widget width increased to 590px (vs 560px Windows/Linux) to prevent date/time clipping
- **macOS**: Correct copyright info in About dialog (`NSHumanReadableCopyright`)

### Performance
- Debounced window position writes (reduces disk I/O during dragging)
- Debounced state saves for compact mode and view settings
- Settings panel layout consolidated into 2-column rows

---

**For detailed changes, see [CHANGELOG.md](CHANGELOG.md)**

-Damon1974
