# How to update my server

To ensure your FiveM server runs smoothly and avoids critical issues, it’s essential to keep your framework, artifacts, and gamebuild up to date. Here's a detailed guide.

## Framework
Your server framework is the most important component. We generally recommend ESX, but the process below applies to both QBCore and ESX.

## Artifacts
Artifacts are the core server binaries — effectively the brain of your server. Staying current ensures compatibility and stability.

## Gamebuild
The gamebuild is the GTA V build/DLC version your server enforces. Using a recent build avoids feature and compatibility problems.

## Framework Update: qb-core or es_extended
Updating your framework is a crucial step before proceeding with artifacts and gamebuild updates. Follow these steps carefully.

### Download the official framework
- For QBCore: get the latest version from the official QBCore repository.
- For ESX (es_extended): get the latest version from the official ESX repository.

### Replace your current framework folder
- Completely remove your existing framework folder and replace it with the latest version from the official repository.
- Avoid merging files, as this may leave outdated files in place and cause unexpected issues.

### Do not rename the framework folder
- Keep the folder name exactly as provided (for example: `qb-core` or `es_extended`).
- Renaming it can cause severe compatibility problems with scripts, which often reference specific folder names.
- Renaming your framework does not make it “custom” — it makes it prone to breakage.

## Update Artifacts
Artifacts are the core files needed to run your server. Keeping them updated is essential for compatibility with the latest FiveM features.

### Remove old artifacts
- Delete your current artifacts folder entirely to avoid leftover files causing issues.

### Download latest artifacts
- Get the latest version of artifacts for your operating system from the official FiveM sources.
  - Windows artifacts
  - Linux artifacts

### Extract and replace
- Extract the downloaded artifacts and fully replace your old artifacts folder.

## Update Gamebuild
Using the latest gamebuild ensures access to new features and prevents compatibility errors.

### Open your `server.cfg`
- Locate and open your `server.cfg`. In the header, add your desired gamebuild.

### Edit your server configuration
Add the following line to enforce a recent stable build:

```cfg
sv_enforceGameBuild 3258
```

## Why is this important?
- Keeping your framework, artifacts, and gamebuild updated ensures your server is compatible with the latest scripts and features.
- Not updating can lead to crashes, bugs, or incomplete functionality.
- Avoid renaming folders or using unofficial versions of frameworks, as this often causes critical errors.

By following these steps, you ensure a stable, well-functioning server that minimizes common issues.

## Media
- Video: [Placeholder – walkthrough of artifacts, framework, and gamebuild update]
- Screenshots: [Placeholder – server.cfg edit, artifact folder replacement]


