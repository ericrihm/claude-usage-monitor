# Claude Usage Widget v1.7.2

This release brings multi-organization support, real-time system tray indicators, enhanced security, and improved platform documentation.

## What's New

### Multi-Organization Support
Users with both Personal and Teams Claude accounts can now select which organization to monitor directly from Settings. The organization selector appears automatically when multiple chat-enabled organizations are detected, defaulting to Teams when available. Switching organizations triggers an immediate refresh of usage data.

### System Tray Usage Indicators
Two compact tray icons provide at-a-glance monitoring of your Claude usage without opening the widget. The left icon (blue) displays Weekly usage; the right icon (purple) shows Session usage. Each icon renders percentage values using a crisp 8×11 bitmap font optimized for legibility at system tray scale. When usage reaches 99-100%—the realistic threshold where Claude API requests begin to fail—icons automatically switch to a red X indicator. Currently available on Windows; macOS and Linux support is planned for a future release.

### Enhanced Login Security
Login flow now enforces strict navigation controls, restricting the login window to trusted authentication domains only (claude.ai, Google, Apple, Microsoft OAuth providers). Popup windows are blocked, and the current URL is displayed in the window title bar for full transparency. These measures prevent phishing attacks and login flow hijacking attempts.

### Expanded Platform Documentation
Linux users now have access to comprehensive setup instructions for creating application launchers and configuring auto-start behavior, contributed by community member [@sergkuzn](https://github.com/sergkuzn).

## Bug Fixes

### Semantic Versioning Compliance
Corrected update checker logic to properly handle pre-release version comparisons. The checker previously treated stable versions (e.g., 1.7.1) as newer than pre-release candidates (e.g., 1.7.2-rc.1), causing incorrect update notifications. Version comparison now strictly follows semantic versioning standards.

---

**Full Changelog**: [v1.7.1...v1.7.2](https://github.com/SlavomirDurej/claude-usage-widget/compare/v1.7.1...v1.7.2)
