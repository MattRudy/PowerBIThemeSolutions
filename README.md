# PowerBIThemeSolutions
[![Inline docs](http://inch-ci.org/github/MattRudy/PowerBIThemeSolutions.svg?branch=main&style=shields)](http://inch-ci.org/github/MattRudy/PowerBIThemeSolutions)
[![Validate JSONs](https://github.com/MattRudy/PowerBIThemeSolutions/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/MattRudy/PowerBIThemeSolutions/actions/workflows/tests.yml)
<br>I'm often approached with Power BI Theme Problems. This is an evergreen catalogue of their solutions as the tool evolves.

In an ideal world, I'd like to have permanent solutions in Themes for problems like 'I want to always have layer order maintained' and 'I want to always have visual headers hidden'. In the ever-evolving state of Power BI we constantly see new visuals released and changes to the UI that often mean universal settings that should apply to everything only apply to a subset of the current visuals.

This repository is dedicated to tracking the current solutions for these problems using themes, and cataloguing known issues and last manually verified date & version so you can trust the solutions you see are fresh.

The approach taken will be to include both the global and visual-specific settings to succeed in as many cases as possible - we're looking for situations that we can't control by theme at global or visual-specific levels.

Read on for a list of problems!

## Currently Ignoring the following:
* R Custom Visual
* Python Custom Visual
* PowerApps Visual
* Visuals other than default and preview visuals bundled with the latest version of Power BI (If you had to add it manually or get it from AppSource, it's not covered here)

## Best Defaults for Custom Backgrounds
[![Build](https://img.shields.io/badge/Build-Unverified-yellow.svg)](https://github.com/MattRudy/PowerBIThemeSolutions/edit/main/README.md) [Link to unnamed.json](https://github.com/MattRudy/PowerBIThemeSolutions/edit/main/README.md)
<br>**Why?** Includes setting all backgrounds to transparent, setting page background transparency to 0 and background to 'fit' so that custom backgrounds show under all visuals.
<br>**Last Checked (Version):** Never (No Version)
<br>**Known Problems:** None

## Always have outlines on every visual
[![Build](https://img.shields.io/badge/Build-Unverified-yellow.svg)](https://github.com/MattRudy/PowerBIThemeSolutions/edit/main/README.md) [Link to AlwaysHaveOutlines.json](https://github.com/MattRudy/PowerBIThemeSolutions/blob/main/src/AlwaysHaveOutlines.json)
<br>**Last Checked (Version):** Never (No Version)
<br>**Known Problems:** None

## Always have a background on every visual and page
[![Build](https://img.shields.io/badge/Build-Verified-brightgreen.svg)](https://github.com/MattRudy/PowerBIThemeSolutions/blob/main/src/AlwaysHaveBackgrounds.json) [Link to AlwaysHaveBackgrounds.json](https://github.com/MattRudy/PowerBIThemeSolutions/blob/main/src/AlwaysHaveBackgrounds.json)
<br>**Why?** Ensures that all visuals and pages have backgrounds enabled.
<br>**Last Checked (Version):** April 28, 2021 ( 2.92.706.0 64-bit (April, 2021) )
<br>**Known Problems:** None

## Always set fonts on every visual (Minimal Approach)
[![Build](https://img.shields.io/badge/Build-Failing-orange.svg)](https://github.com/MattRudy/PowerBIThemeSolutions/blob/main/src/SetGlobalFonts_Minimal.json) [Link to SetGlobalFonts_Minimal.json](https://github.com/MattRudy/PowerBIThemeSolutions/blob/main/src/SetGlobalFonts_Minimal.json)
<br>**Why?** Power BI's documentation ([link](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-report-themes#setting-formatted-text-defaults)) states that 4 text classes should handle text formatting for all cases. This template ensures that Font is set for every part of all visuals in the current set of default & preview visuals.
<br>**Last Checked (Version):** April 27, 2021 ( 2.92.706.0 64-bit (April, 2021) )
<br>**Known Problems (Global Settings):**
* Don't apply to Gauge Visual - Callout Value
* Don't apply to Key Influencers Visual - UI Prompt
* Don't apply to Shape Visual - Text Value
* Untested on PowerApps Visual

## Always have 'Maintain Layer Order' turned on for every visual
[![Build](https://img.shields.io/badge/Build-Verified-brightgreen.svg)](https://github.com/MattRudy/PowerBIThemeSolutions/blob/main/src/MaintainLayerOrder.json) [Link to MaintainLayerOrder.json](https://github.com/MattRudy/PowerBIThemeSolutions/blob/main/src/MaintainLayerOrder.json)
<br>**Why?** Ensures that visuals behind other visuals in the layer order don't "jump" in front when selected. Previously this was controlled with bookmarks.
<br>**Last Checked (Version):** April 25, 2021 ( 2.92.706.0 64-bit (April, 2021) )
<br>**Known Problems (Global Settings):** None
<br>**Known Problems (Per-Visual Settings):**
* Specific settings for new 'Power Apps' visual not yet stable.
* Some shapes respond to 'basicShape' and some to 'shape' so both should be set in templates unless using global settings.

## Always have Visual Headers hidden for every visual
[![Build](https://img.shields.io/badge/Build-Verified-brightgreen.svg)](https://github.com/MattRudy/PowerBIThemeSolutions/blob/main/src/HideVisualHeaders.json) [Link to HideVisualHeaders.json](https://github.com/MattRudy/PowerBIThemeSolutions/blob/main/src/HideVisualHeaders.json)
<br>**Why?** Ensures a custom-built app feel for users. Individual visual headers aren't popping up when hovering over visuals or objects on pages.
<br>**Last Checked (Version):** April 26, 2021 ( 2.92.706.0 64-bit (April, 2021) )
<br>**Known Problems (Global Settings):** None
<br>**Known Problems (Per-Visual Settings):**
* Specific settings for new 'Power Apps' visual not yet stable.
* Some shapes respond to 'basicShape' and some to 'shape' so both should be set in templates unless using global settings.
