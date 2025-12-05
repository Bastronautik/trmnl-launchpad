# Launchpad - Upcoming Rocket Launches

A space enthusiast's plugin for TRMNL that displays information about upcoming rocket launches from around the world.

## Overview

Stay informed about the next frontier of space exploration! This plugin shows details about upcoming rocket launches, including mission information, launch providers, timing, and more. Data is sourced from The Space Devs API and updated regularly.

## Features

- **Live launch data** - Information about upcoming rocket launches worldwide
- **Randomized selection** - Choose to display 1-10 upcoming launches at random
- **Detailed mission info** - Launch provider, rocket name, mission details, and location
- **Countdown timer** - Shows time remaining until launch (T-minus format)
- **Launch images** - Visual representation when available
- **UTC timing** - Launch times displayed in UTC for accuracy

## Settings

### Amount of Launches, Randomized
- **Type:** Dropdown
- **Description:** Select the amount of launches you would like to randomize
- **Options:** 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
- **Help Text:** Select 1 if you always want the latest
- **Default:** 1

## Technical Details

- **Strategy:** Polling
- **Polling URL:** `https://trmnl.achtnegen.nl/launchpad/launch/upcoming?limit={{ amount }}`
- **Polling Method:** GET
- **Refresh Interval:** 1440 minutes (24 hours)
- **Screen Padding:** Yes
- **Dark Mode Support:** No

## How It Works

The plugin fetches data from The Space Devs API (thespacedevs.com), an open API for space launch information. To respect API rate limits, the data is cached on the developer's server and refreshed every 15 minutes. 

When you configure the plugin to show multiple launches, it randomly selects from the upcoming launches, giving you variety each time the display refreshes.

### Displayed Information

- **Launch Name** - Mission designation
- **Rocket** - Vehicle configuration name
- **Provider** - Launch service provider
- **Mission Type** - Purpose of the mission
- **Orbit** - Target orbit (if applicable)
- **Launch Pad** - Specific pad and location
- **Launch Time** - Date and time in UTC
- **Countdown** - Time remaining (days/hours or hours/minutes)
- **Status** - Current launch status

## API Information

This plugin uses data from [The Space Devs](https://thespacedevs.com), an open API for space flight data. The data is:
- Cached and served through the developer's server
- Refreshed every 15 minutes
- Subject to API limitations and availability

## Layout Support

This plugin supports all TRMNL layout sizes:
- Full screen (recommended for maximum detail)
- Half horizontal
- Half vertical
- Quadrant
