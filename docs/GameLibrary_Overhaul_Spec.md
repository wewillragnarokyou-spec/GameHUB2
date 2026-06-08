# Game Library Overhaul Specification

## Goal
Replace the current right-click driven List Editor workflow with a dedicated Game Library management interface while preserving the existing Rainmeter architecture, visual style, and configuration format.

## Rename
List Editor -> Game Library

## Primary Objectives
- Eliminate right-click driven asset management.
- Add visible Add Game and Edit Library controls in the launcher UI.
- Provide a unified game editor.
- Automatically fetch game assets.
- Allow manual asset overrides.
- Support drag-and-drop reordering.
- Maintain Rainmeter compatibility.

## New Workflow
1. Add Game
2. Select executable or Steam AppID
3. Auto-detect metadata
4. Fetch assets
5. Preview assets
6. Save entry

## Data Sources
### Steam Store
- Metadata
- App information

### SteamDB
Preferred assets:
- main_capsule_2x (primary background)
- raw_page_background (fallback background)
- library_capsule_2x (cover art)
- library_logo image/english (logo)

### SteamGridDB API
Fallback and alternative assets:
- Heroes
- Grids
- Logos

## Asset Processing
### Logo Processing
Automatically:
- Preserve alpha channel
- Convert visible pixels to white
- Save transparent PNG

### Background Priority
1. main_capsule_2x
2. raw_page_background
3. SteamGridDB hero

## Game Library Window
Features:
- Card-based game list
- Asset previews
- Edit button
- Delete button
- Drag-and-drop ordering
- Manual asset replacement
- Re-fetch assets button

## Rainmeter Technology Constraints
UI:
- Rainmeter skins

Logic:
- Lua

Networking:
- PowerShell

Optional image processing:
- ImageMagick

## UI Adjustments
- Reduce launcher close button size.
- Lower top navigation bar approximately 10px.
- Match existing launcher styling.
- Use full-screen modal management screens.

## Deliverables
- New Game Library interface
- Add Game modal
- Asset discovery workflow
- Automatic asset downloading
- Automatic logo whitening
- Drag-and-drop ordering system
- Asset override support
- Backward-compatible configuration migration where possible
