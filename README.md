# Birthday Surprise Website — README

This project is a single-page birthday surprise website. The main website and its customizer are contained in `index.html`.

## Open the Secret Box

Use one of the hidden access methods built into the page:

1. **Keyboard:** press **Alt + Shift + S**.
2. **Bottom-right corner:** tap/click the hidden corner control five times.
3. **Double-click:** double-click the hidden bottom-right control.
4. **Press and hold:** hold the hidden bottom-right control for about 1.8 seconds.
5. **Brand/title:** tap/click the website brand/title five times.

If one method does not work in your browser, try the keyboard shortcut first.

## General editing workflow

1. Open the Secret Box.
2. Find **Choose a scene to edit** and select the scene you want.
3. Edit its available text fields and add media using that scene's upload controls.
4. For fields that accept multiple entries separated by `|`, use one vertical bar between entries. Example:

   `First message|Second message|Third message`

5. Save using the customizer's save controls. If you use the GitHub save workflow, check that it reports success.
6. Refresh the published page and test the change.

The exact field labels may vary slightly by version of `index.html`. Only fields shown in your current Secret Box can be edited for that scene.

## Scene-by-scene editing guide

### Scene 1 — Birthday countdown / opening
- Edit the birthday date and time in the global settings, if those fields are shown.
- Update the opening scene's text/title using its scene fields.
- Save, reload, and verify the countdown changes every second.
- The countdown celebration is intended to lead to the final celebration scene.

### Scene 2 — Envelope / letter
- Edit the letter's message in the scene text field.
- Add or replace the scene image if an image upload control is provided.
- Test that the letter is hidden initially and appears after the envelope is tapped.

### Scene 3 — What I Love About You
- Enter the messages in the love-notes field.
- Separate multiple messages with `|` if the field requests it.
- The initial interaction uses three capsules; after revealing, all messages entered in the Secret Box should appear.
- Add a scene image if the scene offers an image upload field.

### Scene 4 — Our Story
- Edit the story/chapter text in the story field.
- Where multiple chapters are supported, separate entries with `|`.
- If chapter titles have a separate field, keep the titles in the same order as their chapters and follow the separator hint shown in the customizer.
- Add or replace scene images using the available upload controls.
- Test the chapter navigation after saving.

### Scene 5 — Birthday wishes jar
- Enter all wishes/messages in the wishes field, using `|` between entries if prompted.
- Add or replace the jar/genie scene image if an image control is available.
- Reveal the jar in the page to check that the genie and all configured wishes appear as expected.
- The jar should remain its standard size; the reveal interaction should not resize it.

### Scene 6 — Our Moments / photos
- Use the photo upload control to add multiple photos.
- Check the photo list/asset manager if available; remove any unwanted image there.
- The **Say cheese!** interaction should advance to the next photo.
- Save and revisit the scene to confirm the photos persist.

### Scene 7 — Our Places
- Enter place names and their descriptions in the place fields.
- Separate multiple entries with `|` when the customizer indicates that format.
- Add or remove place entries using the controls shown in the Secret Box.
- Revisit the scene and test that each place can be browsed.

### Scene 8 — Our Song
- Use the song/audio upload control to choose the personal song.
- Save the page/configuration after the upload finishes.
- Visit Our Song and press play to test playback.
- The personal song is intended to pause/replace the birthday music while playing; browser autoplay restrictions may require a tap.

### Scene 9 — Candle blowing
- Edit the scene text using the fields provided.
- Add a scene image if supported.
- Test the hold-to-blow interaction. The candles should go out and the overall page should dim.
- Leaving and returning to the candle scene should reset it so the visitor can blow again.

### Scene 10 — Final celebration
- Edit the final scene's title/message in the fields provided.
- Add or replace the scene image if available.
- Test the celebration and **Watch again** / gift buttons after saving.
- Verify that navigation reaches this scene correctly.

## Photos, audio, and other uploaded files

- Use the upload control belonging to the relevant scene.
- Wait for the customizer to confirm the file has been added.
- Use the asset manager, when available, to review or remove uploaded photos, audio, or scene images.
- Save after changing assets. Then refresh and verify that the files remain.
- Large media files can exceed GitHub/API limits. Resize images or compress audio if saving fails.

## GitHub save workflow and security

1. Open the Secret Box and make your edits.
2. Use the GitHub save workflow and follow its prompts.
3. Confirm that the save succeeds and targets the intended repository and `index.html`.
4. Wait for GitHub Pages to publish, then hard-refresh the site.

**Keep your GitHub token private.** Do not put it in this README, share it in screenshots, or commit it into public source code. A token entered into a browser-side page may be exposed to someone who can inspect that page. Use only permissions and repositories you understand.

## Troubleshooting

### Countdown is frozen
- Check the configured date and time.
- Reload the page after saving.
- If it remains frozen, open the browser developer console and look for the first JavaScript error.

### Changes do not appear
- Confirm the customizer saved successfully.
- Verify that you are opening the correct published URL and repository file.
- Hard-refresh or try a private/incognito window to rule out stale cached content.

### Audio does not play
- Click the play button; browsers often block autoplay until a user gesture.
- Check volume and use a browser-supported audio format.

### Uploaded files disappear after refresh
- Confirm the upload completed and save succeeded.
- Reduce media size if GitHub saving fails.
- Reopen the same published site and refresh without cache.

## Safe editing checklist

1. Keep a backup of your known-working `index.html`.
2. Change one thing at a time.
3. Test locally or in a private browser window.
4. Save/publish and test the live page.
5. If something breaks, restore the backup before trying another change.
