# 🎮 roblox-codex-launcher-studio

![tool](https://img.shields.io/badge/tool-MIT-green?style=flat-square) ![Version](https://img.shields.io/badge/Version-1.2.0-blue?style=flat-square) ![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey?style=flat-square) ![Python](https://img.shields.io/badge/Python-3.11%2B-3776AB?style=flat-square&logo=python&logoColor=white) ![Stars](https://img.shields.io/github/stars/ericlopezlab92p8/roblox-codex-launcher-studio?style=flat-square) ![Last Commit](https://img.shields.io/github/last-commit/ericlopezlab92p8/roblox-codex-launcher-studio?style=flat-square)

Roblox-codex-launcher — — pixel detection, crosshair overlay, configurable settings

## 📥 Download

[![Download Latest](https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge&logo=github)](../../releases/latest)

1. Download the latest release from the link above
2. Extract the archive (WinRAR / 7-Zip)
3. Run `python main.py` (or see Usage below)
4. Configure settings in `config.yaml`

### Contributing

Got ideas? Found a bug? Great! Here's how you can help:

* Fork the repository.
* Create a new branch for your changes (`git checkout -b my-new-feature`).
* Commit your changes (`git commit -am 'Add some feature'`).
* Push to the branch (`git push origin my-new-feature`).
* Create a new Pull Request.

We appreciate your contributions!

### Basic Usage

Okay, so you've downloaded it. Now what?

1. **Install dependencies:** `pip install -r requirements.txt`
2. **Run the launcher:** `python engine.py`
3. **Configure**: Edit `config.yaml` to your liking. See the Config section below.
4. **Let it run**: The launcher will sit in the background, doing its thing.

### Config

The `config.yaml` file is where you control everything. Here's an example:

```yaml
overlay:
 enabled: true
 color: "red"
 thickness: 2
 size: 25

pixel_detection:
 enabled: true
 region: [100, 100, 200, 200]
 color: [255, 0, 0]
 threshold: 10
 interval: 0.1

hotkeys:
 tool: "F1"
 de: "F2"

ports:
 web_server: 8080
 data_stream: 8081

paths:
 log_file: "logs/launcher.log"
```

* `overlay.enabled`: Turns the crosshair overlay on or off.
* `pixel_detection.region`: The area of the screen to scan (x1, y1, x2, y2).
* `hotkeys`: Customize your hotkeys. Make sure they don't conflict with other apps!

### FAQ

<details>
 <summary>The overlay isn't showing up. What's wrong?</summary>
 <ul>
 <li>Make sure <code>overlay.enabled</code> is set to <code>true</code> in your config.</li>
 <li>Check that the game isn't running in fullscreen mode. Try borderless windowed.</li>
 <li>Verify that no other overlays are conflicting (e.g., Discord, Steam).</li>
 </ul>
</details>

<details>
 <summary>Pixel detection is unreliable. Any tips?</summary>
 <ul>
 <li>Adjust the <code>threshold</code> value. A lower value is more sensitive.</li>
 <li>Double-check the <code>region</code> coordinates. Are you looking in the right place?</li>
 <li>Ensure the <code>color</code> value matches the pixel you're trying to detect. Use a color picker tool.</li>
 </ul>
</details>

<details>
 <summary>Can I change the crosshair color?</summary>
 <p>Yep! Edit the <code>overlay.color</code> value in <code>config.yaml</code>. Use a common color name (e.g., "red", "blue") or a hex code (e.g., "#FF0000").</p>
</details>

### Requirements

You'll need Python 3.11+ to run this. Also, make sure you have these packages installed:

* `PyYAML`
* `Pillow`
* `pynput`
* `opencv-python`

Install them using pip:

```bash
pip install -r requirements.txt
```

TODO: Add a check for missing dependencies on startup.

---

Contributions are welcome! Feel free to open a PR.