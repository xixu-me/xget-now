<!-- renoise-banner -->
<p align="center">
  <a href="https://renoise.ai/plugin?utm_medium=github&utm_source=xixu">
    <img src="https://raw.githubusercontent.com/renoise-ai/renoise-plugins-official/main/assets/icon.svg" alt="Renoise" width="96">
  </a>
</p>

<p align="center">
  <a href="https://renoise.ai/plugin?utm_medium=github&utm_source=xixu">Renoise MCP</a> · <a href="https://github.com/renoise-ai/renoise-plugins-official">Renoise Skills &amp; CLI</a><br><br>
  <strong>Find a reference in the browser, download it in one click, and turn it into a talking-head video without manual editing.</strong>
</p>

# Xget Now

***[汉语](README.md)***

A cross-browser extension for Chromium and Firefox that accelerates file downloads by seamlessly forwarding them to an [Xget](https://github.com/xixu-me/Xget) instance.

> [!NOTE]
> Quick start: install the store version, enter your Xget domain such as `xget.xi-xu.me`, and leave the target platform toggles enabled.

## Overview

Xget Now detects real download links on supported websites, rewrites them to your Xget domain, and keeps the browser's native download flow intact. You do not need to modify the original site or manually copy download URLs.

## Features

- Automatic download acceleration: seamlessly redirect downloads through Xget for faster speeds.
- Configurable settings: customize your Xget domain and platform preferences.
- Smart notifications: visual feedback when downloads are redirected.
- Privacy-first: all processing happens locally in your browser.
- Per-platform control: enable or disable acceleration for specific platforms.
- Cross-browser support: works on both Chromium and Firefox browsers.

## Supported Platforms

- Code hosting: GitHub, GitLab, Gitea, Codeberg, SourceForge, AOSP.
- AI / ML: Hugging Face.
- Package and distribution platforms: npm, PyPI, PyPI Files, Conda, Conda Community, Maven Central, Apache Downloads, Gradle Plugin Portal, RubyGems, CRAN, CPAN, CTAN, Go Modules, NuGet, Crates.io, Packagist.
- Other platforms: arXiv, F-Droid.

## Installation

### Store Availability

- [Chrome Web Store](https://chromewebstore.google.com/detail/ajiejgobfcifcikbahpijopolfjoodgf?hl=en)
- [Chrome Web Store Mirror](https://chromewebstore.xi-xu.me/detail/ajiejgobfcifcikbahpijopolfjoodgf)
- [Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/xget-now/)
- [Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/jigpfhbegabdenhihpplcjhpfdcgnalc)

### Manual Installation

If you prefer manual installation, or if a store listing is unavailable, you can install Xget Now from GitHub releases or directly from source.

#### Option 1: Install from GitHub Releases

1. Go to the [Releases page](https://github.com/xixu-me/Xget-Now/releases/latest).
2. Download the package for your browser:
   - `Xget-Now_x.x.x.chromium.zip`: for Chromium-based browsers such as Chrome, Edge, and Opera.
   - `Xget-Now_x.x.x.firefox.xpi`: for Firefox.
3. Install in Chrome:
   - Extract the Chromium `.zip` package.
   - Open `chrome://extensions/`.
   - Enable "Developer mode" in the top-right corner.
   - Click "Load unpacked" and select the extracted folder.
4. Install in Firefox:
   - Open `about:debugging`.
   - Click "This Firefox".
   - Click "Load Temporary Add-on".
   - Select the Firefox `.xpi` file, or the `manifest.json` file from an extracted package.
5. Install in Edge:
   - Extract the Chromium `.zip` package.
   - Open `edge://extensions/`.
   - Enable "Developer mode" in the left sidebar.
   - Click "Load unpacked" and select the extracted folder.
6. Install in other Chromium-based browsers:
   - Use the Chromium package.
   - Enable that browser's developer mode first.
   - Follow the browser-specific extension loading instructions.

#### Option 2: Install from Source

1. Clone the repository:

   ```bash
   git clone https://github.com/xixu-me/Xget-Now.git
   cd Xget-Now
   ```

2. Build the extension if needed:

   `build.py` only uses the Python standard library, so Python 3.7+ is enough.

   ```bash
   python build.py --platform chrome
   python build.py --platform firefox
   python build.py --platform all
   python build.py --platform all --package
   ```

3. Load it in the browser:
   - Chromium browsers:
     - Open `chrome://extensions/` or `edge://extensions/`.
     - Enable "Developer mode".
     - Click "Load unpacked" and select either the repository root, or `build/chrome/` if you built the packaged version.
   - Firefox:
     - Open `about:debugging`.
     - Click "This Firefox".
     - Click "Load Temporary Add-on".
     - Select `manifest-firefox.json` from the repository root, or `build/firefox/manifest.json` from a build output.

#### Verify Installation

After installation, you should see the Xget Now icon in the browser toolbar. Click it, configure your Xget domain, and start accelerating downloads.

## Configuration

1. Click the extension icon in the browser toolbar.
2. Enter your Xget domain, for example `xget.xi-xu.me`.
3. Enable the extension and toggle supported platforms on or off as needed.
4. Visit any supported platform and click download links as usual.
5. Downloads will automatically be routed through Xget.

## How It Works

1. Detection: the extension monitors download links on supported platforms.
2. Transformation: URLs are converted to an Xget-compatible format.
3. Redirection: downloads are routed through your configured Xget domain.
4. Acceleration: Xget's CDN and optimization features provide faster download speeds.

## Requirements

### Browser Support

- Chrome: 88+.
- Edge: 88+.
- Opera: 74+.
- Other Chromium-based browsers: versions with Manifest V3 support.
- Firefox: 109+.
- Firefox ESR: 109+.

### Xget Instance

Use the pre-deployed instance `xget.xi-xu.me`, or deploy your own by following the [Xget deployment documentation](https://github.com/xixu-me/Xget#-deployment).

## Privacy and Security

- Local processing: all URL transformations happen in your browser.
- No data collection: the extension does not collect or transmit personal data.
- Minimal permissions: it only requests permissions needed for the feature set.
- Open source: the full source code is available for inspection.

See the [Privacy Policy](PRIVACY_POLICY.md) for complete details.

## Troubleshooting

### Common Issues

**Extension not working?**

- Ensure you configured a valid Xget domain.
- Check whether the extension is enabled in the popup.
- Verify that the target platform is enabled.
- Refresh the page after changing settings.

**Downloads not being redirected?**

- Refresh the page after changing settings.
- Check the browser console for error messages (`F12` -> Console).
- Ensure the link is a recognized download type.
- Confirm that you clicked an actual download link rather than a navigation link.

**Xget domain issues?**

- Enter the domain without the `https://` protocol.
- Example: `xget.xi-xu.me`, not `https://xget.xi-xu.me`.
- Check whether the domain is reachable in your browser.
- Try the default pre-deployed instance first: `xget.xi-xu.me`.

**Performance issues?**

- Check your network connection.
- Try another Xget domain if one is available.
- Verify that the target platform is responding normally.
- Clear the browser cache and reload the extension.

**Firefox-specific issues?**

- Ensure Firefox is version 109 or newer.
- Check whether the extension is correctly loaded in `about:debugging`.
- Firefox may require a restart to fully apply extension settings.
- Review Firefox Privacy & Security settings to make sure they are not blocking extension behavior.

### Debug Mode

In Chromium browsers, open DevTools and inspect the Console tab. In Firefox, open `about:debugging`, click "This Firefox", find Xget Now, click "Inspect", and review the console output there.

Common debug messages:

- Extension loaded: `Xget Now: Content script loaded`
- Download redirect: `Redirecting download: [original] -> [Xget]`
- Settings changed: `Settings updated! Click to refresh page`

## FAQ

### Is this extension free?

Yes. The extension is completely free and open source under GPL-3.0.

### Can I use my own Xget server?

Yes. You can deploy your own Xget instance from the [Xget repository](https://github.com/xixu-me/Xget) and point the extension to your own domain.

### Why are some downloads still going through the original server?

The extension only redirects recognized download links. Navigation links, preview links, and some dynamic content may not be redirected.

### Will my browsing data be collected?

No. The extension runs entirely locally, and no browsing data is collected or transmitted. See the [Privacy Policy](PRIVACY_POLICY.md) for details.

### How much faster are the downloads?

Speed improvements depend on your location, network conditions, and file size. Typical gains range from roughly 2x to 10x.

### Can I disable the extension for specific websites?

Yes. Use the per-platform toggle switches in the popup to disable acceleration for specific supported platforms.

### Why are there different versions for Chrome and Firefox?

The two versions are optimized for different browser architectures:

- Chrome version: uses Manifest V3 and newer extension APIs.
- Firefox version: uses Manifest V2 for Firefox compatibility.

The core behavior remains the same, while the implementation details differ slightly.

### Can I use it in Chrome and Firefox at the same time?

Yes. You can install Xget Now in multiple browsers at once, and each browser keeps its own settings.

## Support

If Xget Now is useful to you, consider:

- Starring the repository.
- Leaving a review:
  - [Chrome Web Store](https://chromewebstore.google.com/detail/ajiejgobfcifcikbahpijopolfjoodgf?hl=en)
  - [Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/xget-now/)
  - [Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/jigpfhbegabdenhihpplcjhpfdcgnalc)
- Reporting bugs or suggesting features via [GitHub Issues](https://github.com/xixu-me/Xget-Now/issues).
- Sharing it with others who might benefit from faster downloads.

> [!NOTE]
> This repository is licensed under GPL-3.0. See [LICENSE](LICENSE) for the full text.
