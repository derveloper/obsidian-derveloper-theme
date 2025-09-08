# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is an Obsidian theme repository using the official sample theme template as its basis. The theme applies a flat, minimalist design with no rounded corners (radius-0 styling).

## Commands

### Version Management
- **Bump version**: `npm run version` - Updates manifest.json and versions.json with new version from package.json

### Release Process
1. Update version in package.json
2. Run `npm run version` to sync manifest.json and versions.json
3. Commit changes
4. Create and push a git tag (e.g., `git tag 1.0.1 && git push origin 1.0.1`)
5. GitHub Actions will automatically create a release with the required assets

## Key Files

- **theme.css**: Main theme styles - all customizations go here
- **manifest.json**: Theme metadata (name, version, minAppVersion, author)
- **versions.json**: Maps theme versions to minimum Obsidian versions
- **version-bump.mjs**: Script that syncs version from package.json to manifest/versions

## Theme Architecture

The theme uses CSS custom properties to override Obsidian's default styling:
- Sets all radius variables to 0px for flat design
- Removes tab header pseudo-elements
- Applies square line caps to SVG elements
- Adjusts menu padding and separators
