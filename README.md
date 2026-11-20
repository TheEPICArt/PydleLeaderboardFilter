# PydleLeaderboardFilter
A Chrome extension for the daily python programming game ["Pydle"](https://github.com/anyhotcountry/pydle-public) to filter out hardcoded solutions on the leaderboard and see your standing amongst players how you like to play!

## Features
- **Inline Leaderboard Controls:** Injects a filter bar directly into the leaderboard dialog above the solution list or code view with spacing preserved across views.
- **Literal-Aware Filtering:**
  - **No &gt;4-digit num:** Flags decimal integers with 5 or more digits as well as large hex (`0x...`) or binary (`0b...`) literals.
  - **No &gt;7-char str:** Scans individual single-, double-, and triple-quoted string and bytes literals (including `b"..."`, `r"..."`, `f"..."`, and escaped characters) to check whether any single literal exceeds 7 characters/bytes.
- **Automatic Username Detection:** Reads and caches your username from the **Settings** modal (`#gamer-tag`) so your rank is calculated without manual entry.
- **Hide Disqualified & Filtered Navigation:** Optionally hides disqualified rows, renumbers remaining visible entries sequentially, disables boundary navigation arrows when no valid previous/next entry exists, locks modal height, and displays a loading overlay during scans and filtered entry transitions to prevent layout jumps and flashing.

## Installation in Google Chrome

1. **Download the repository from GitHub**
   - Click the green **Code** button at the top of the repository page and choose **Download ZIP**.
   - Extract the ZIP archive into a permanent folder on your computer (for example, `~/Extensions/PydleLeaderboardFilter-main` or `C:\Extensions\PydleLeaderboardFilter-main`). Keep this folder in place because Chrome points directly to this directory and will break if you move or delete it later.

3. **Open Chrome's Extensions page and enable Developer mode**
   - In Google Chrome, go to `chrome://extensions/` (or click the **three-dot menu** → **Extensions** → **Manage Extensions**).
   - Toggle **Developer mode** on in the top-right corner.

4. **Load the unpacked extension**
   - Click **Load unpacked** in the top-left toolbar.
   - Select the folder containing `manifest.json` and `content.js` and confirm.
   - The extension will appear in your extensions list with a toggle enabled.

5. **Open Pydle**
   - Visit `https://pydle.net` (or refresh the tab if it is already open). Once you solve a puzzle, open the leaderboard to use the filter controls.
