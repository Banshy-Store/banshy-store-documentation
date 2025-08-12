# Upgrading an old script

Follow these steps to safely upgrade an existing script to a newer version.

## 1) Back up first
- Save a copy of the resource folder and your database.

## 2) Read the release notes
- Check the changelog for breaking changes or required config/database updates.

## 3) Replace files cleanly
- Remove the old resource folder entirely.
- Extract the new version into the same path.
- Avoid merging files; stale files cause subtle bugs.

## 4) Re-apply configuration
- Reconfigure `config.lua` and any `.env` variables.
- Do not rename the resource or framework folders.

## 5) Run database migrations (if required)
- Apply any SQL changes included with the update.

## 6) Test thoroughly
- Start the server, check console for errors.
- Verify all critical flows in-game.

## 7) Rollback plan
- If issues appear, revert to the backup while you investigate.

Last updated: today


