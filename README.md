# 🎂 10-Scene Birthday Surprise Website

A customizable birthday surprise webpage delivered as a single HTML file. It includes 10 interactive scenes, a secret customization panel, a countdown timer, birthday animations, and optional GitHub-based shared settings.

## 📁 Files

- `index.html` — the main website.
- `README.md` — project instructions.

## 🚀 Getting Started

1. Download the HTML file.
2. Open it in Chrome, Edge, Firefox, or another modern browser.
3. Explore the birthday scenes and interactive effects.

No installation or build process is required.

## 🔐 Open the Secret Customization Panel

1. Open the birthday page.
2. Tap or click the bottom-right corner **5 times**.
3. Edit the available settings.
4. Click **Save changes**.

Depending on the version, settings may include:

- Birthday person's name and age
- Birthday date and celebration time
- Birthday messages and scene text
- Photos, music, and celebration effects
- GitHub shared-settings configuration

## ⏰ Test the Countdown Celebration

The scheduled celebration should happen on **Scene 1**, without automatically navigating to Scene 10.

1. Open the secret customization panel.
2. Set the birthday date to today.
3. Set the celebration time to approximately 1–2 minutes in the future, using your device's local time.
4. Save your settings.
5. Keep the page open until the countdown reaches zero.

Expected behavior:
- The page remains on Scene 1.
- The celebration message appears.
- Confetti and the configured celebration animations play.

The remaining scenes can still be explored manually.

## 🎉 Age Customization

Enter an age in the optional age field and save your settings. The page is intended to display an age-related birthday message when an age is provided. Leave the field blank to omit it.

## ☁️ GitHub Shared Settings

If GitHub synchronization is enabled in your HTML version, it can be used to load and save shared birthday settings.

1. Create a GitHub repository.
2. Configure a JSON file for the shared settings.
3. Create a fine-grained GitHub Personal Access Token with only the necessary repository permissions.
4. Enter the repository, branch, file path, and token in the secret panel.
5. Save settings to GitHub from the editing copy.
6. Load the latest settings in another copy of the page.

### Security

- Never hard-code a write-enabled GitHub token into a public HTML file.
- Do not share your token with recipients.
- For a public website used by multiple people, use a secure server-side service to perform write operations.

## 🔄 Keeping Settings Up to Date

For shared settings, the page can fetch the latest JSON without relying on the browser's cached response.

Recommended implementation:
- Fetch settings with `cache: "no-store"`.
- Load the latest settings when the page opens.
- Optionally check for changes every 30–60 seconds.
- Track a version number or updated timestamp.
- Avoid allowing stale local browser storage to overwrite newer shared settings.

Updating shared settings does not automatically update the HTML or JavaScript code itself.

## 🛠️ Troubleshooting

**The secret panel won't open**
- Tap the bottom-right corner five times.

**The countdown doesn't trigger**
- Verify the date and time.
- Make sure the target time is in the future.
- Save changes and leave the page open.

**The celebration jumps to another scene**
- Check the countdown completion logic; it should trigger the celebration effects on Scene 1 rather than navigate automatically to Scene 10.

**Age or other changes don't appear**
- Save the settings, then reload the page.
- Confirm the scene includes the corresponding display element.
- If necessary, the HTML may need a code adjustment.

**GitHub settings appear outdated**
- Confirm the repository, branch, and JSON path.
- Check the token permissions and repository access.
- Reload the shared settings from GitHub.

**Changes aren't visible on another device**
- Confirm the other copy is configured to load the same shared JSON.
- A standalone HTML file cannot automatically synchronize local edits without a shared online source.

## 📌 Notes

The project is designed for local browser use, with optional online settings synchronization when configured. Feature availability depends on the exact HTML version being used.