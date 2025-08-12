# How to manage translations

Banshy Store assets are designed with multilingual support to help you adapt them to your preferred language. Translations are typically stored in a `local` folder within each asset, making it easy to manage and customize language content.

## Where to find translations
- Default translation files are located in the `local` folder of each asset.
- In some cases, translation strings may also exist in other configurable files. Check config files when translating your asset.

## Pre-built translations
- Most assets ship with at least English and Spanish translations to help you get started quickly.
- For other languages, you have two options:
  - Translate it yourself by editing the files in `local/`.
  - Use community-provided translations (if available) or collaborate with your team.

## Suggested workflow
1. Back up the original translation files.
2. Duplicate an existing language folder as a template (for example, copy `en` to `fr`).
3. Translate the strings carefully, keeping placeholders intact (for example, `%s`, `%d`).
4. Test in-game and verify characters render correctly (UTF-8 recommended).

## Good practices
- Keep naming consistent across locales to avoid lookups failing.
- Avoid adding new keys casually; reuse existing ones where possible.
- Validate JSON/Lua syntax before deploying.
- Maintain a changelog of updated keys to help collaborators.

Last updated: today


