# Changelog
All notable changes to this project will be documented in this file.

## [0.3.6] - NOT RELEASED
##### Changed
- Changed position of the "Reset zoom" button in the charts

## [0.3.5] - 2020-03-29
##### Added
- Added the ability to filter stash tabs in the tab breakdown chart
##### Fixed
- Fixed a performance issue introduced with the last update
    - We now limit the snapshots to a count of 50 in the tab breakdown chart

## [0.3.4] - 2020-03-28
##### Added
- Added a new chart for breakdown per tab
- Added a chart toolbox to the net worth chart, for selecting different timespans
- Minor chart improvements

## [0.3.3] - 2020-03-27
##### Added
- Added a filter section for the item table
    - Added a multiselect which lets you filter based on stash tabs
- Added a new column that displays the tab names an item exists in (solo only)
- Added a search icon to the search field
- Minor style tweaks across the app
##### Changed
- Reworked the stash tab dropdown entirely in the profile dialog
    - Better positioning of the popup
    - Ability to clear all in the selection
    - Ability to remove individual stash tabs without opening the popup
- Reduced the padding on rows in the item table, to fit more items per page
- Changed position of the pricing league dropdown in the profile dialog
##### Fixed
- Fixed a bug where some jewels and jewellry without value were listed in the item table
- Fixed a bug where the support button would be placed on top of the scrollbar

## [0.3.2] - 2020-03-24
##### Added
- Added support for pricing delirium orbs
- Added support for pricing vials
- Added a small cross for clearing the search field in the item table
##### Changed
- Changed the default setting for auto snapshotting
    - Now enabled by default
##### Fixed
- Fixed a bug where the overlay sometimes would not stay on top of the game

## [0.3.1] - 2020-03-20
##### Fixed
- Fixed a bug with the new character selection that would interrupt the snapshot chain
- Fixed a missing translation for the new error handling

## [0.3.0] - 2020-03-20
##### Added
- Added a game overlay for the net worth component
- Added optional character selection to profiles
    - Added an option to include equipment in profiles
    - Added an option to include inventory in profiles
- Added fallback for error messages in case message is missing
- Added separate colors in the net worth chart for each group member
- Added redirection to login when the current session has expired
##### Fixed
- Fixed a bug where the status messages would sometimes display an incorrect stash tab count

## [0.2.12] - 2020-03-17
##### Added
- Added support for storing up to 1000 snapshots, up from 100
##### Fixed
- Fixed a bug where normal and magic maps were priced as red maps

## [0.2.11] - 2020-03-12
##### Added
- Added the ability to zoom in the chart
    - Select a portion of the chart with the mouse to zoom in
- Added a support tab that redirects to Discord
- Added the ability to show/hide the chart
- Added the ability to show/hide the item table
##### Changed
- Changed position of the Patreon logo, to allow for more space
- No longer persists snapshots on server (temporarily) to decrease load
##### Fixed
- Fixed a bug where auto snapshotting would stop working
- Fixed a bug where magic maps weren't priced

## [0.2.10] - 2019-02-13
##### Added
- Added support for pricing fragments
- Added support for pricing maps (outside of the map tab)
- Added support for pricing other common items

## [0.2.9] - 2019-02-13
##### Added
- Added support for pricing watchstones
- Added support for pricing incubators
##### Changed
- Improved the retry policy for SignalR
##### Fixed
- Fixed a bug where corrupted unique items were not priced
- Fixed a bug where users sometimes could not sign in from multiple locations

## [0.2.8] - 2019-02-11
##### Added
- Added detailed status messages to the toolbar
- Minor style tweaks
##### Changed
- Changed the lower limit of the auto snapshot interval to 2 minutes
##### Fixed
- Fixed a bug where uniques with quality were not priced correctly
- Fixed a bug where some uniques with links were not priced correctly
- Fixed a bug where the snapshot button would be disabled after relogging

## [0.2.7] - 2020-02-04
##### Added
- Added the ability to trigger manual snapshots while auto snapshotting is turned on
- Minor style tweaks
- Minor client optimizations
##### Changed
- Changed the input field styles in the profile dialog
##### Fixed
- Fixed a bug where failed stash tab requests would trigger an infinite loop for init session
- Fixed a bug where the stash tab dropdown position sometimes would change when selecting a stash tab
- Fixed a bug where part of the scrollbar was hidden beneath the toolbar
- Fixed a bug where the table row borders would sometimes be distorted

## [0.2.6] - 2020-02-02
##### Added
- Added support for private leagues
- Added a introduction tour for new users that will be displayed once
- Added styled tooltips when hovering icon buttons
- Added persistance of item table sort order
##### Changed
- Changed default sort order in item table
    - The total column is now the default (descending)
- Changed retry intervals for initiating/validating sessions
##### Fixed
- Fixed a bug where the label displaying the time since snapshot wasn't updating properly
##### Updated
- Updated Electron framework to version 7

## [0.2.5] - 2020-01-29
##### Changed
- Changed the position and behaviour of the scrollbar
##### Fixed
- Fixed a bug where the app would crash when switching profiles
- Fixed a bug where the app would crash when removing all snapshots

## [0.2.4] - 2020-01-28
##### Added
- Added a setting for scaling the user interface
- Added a new card for income (gain per hour)
    - Currently based on the past 1 hour, but will be configurable later on
- Added a label to the net worth card that displays the diff for the last two snapshots
- Added a label to the snapshot card that displays the time since the last snapshot occured
- Added group support for the chart
    - Now displays one line per player
- Added styling for tooltips
- Now displays a text when an update is ready
    - Ability to update manually from within the app
##### Changed
- Changed the look and feel of the cards in the top of the net worth page
- Changed order of the sections in the toolbar
- Changed how the scroll behaves on the net worth page, to allow for more control
- Changed how the price treshold setting works
    - It now updates the actual value on the snapshot, which means you have to wait for a new snapshot for changes
##### Fixed
- Fixed a bug where the font was not properly set for some users

## [0.2.3] - 2020-01-26
##### Removed
- Removed a forgotten console log

## [0.2.2] - 2020-01-26
##### Added
- Added a new chart widget (replaces the smaller one)
- Adding spacing to the "Total" column in the item table
##### Changed
- Changed default state for navigation menu
- Changed position for Discord and Patreon logos, to be more visible
##### Removed
- Removed the smaller chart widget
##### Fixed
- Fixed a bug where some users would not be connected to our servers properly
    - Caused by multiple connections on the same client
- Fixed a bug where redirects in the app would only work the first time
- Fixed a bug where dropdown menus would linger after signing out

## [0.2.1] - 2020-01-23
##### Added
- Added setting for auto snapshotting with custom intervals
- Added a spinner for when new prices are being fetched
##### Changed
- Changed how prices are calculated for currency items
    - This fixes the overpricing we previously had with certain items
    - They are now a direct reflection of the 'Buy' price at http://poe.ninja instead of the estimated value
    - They will only be included if there are at least 10 items for sale (unless low confidence is turned on)
##### Fixed
- Fixed a bug where low confidence pricing was enabled even though the setting was turned off
- Fixed a bug where users would get force-kicked from the server if trying to login twice
- Fixed a bug where multiple sessions could be initiated at the same time
- Fixed a bug where users sometimes would end up with no active profile after removal

## [0.2.0] - 2020-01-22
##### Added
- Added group system
    - Added the ability to create/join/leave a group
    - Added optional password protection for groups
    - Added the ability to select multiple players in the group
- Added OAuth2 authentication
    - Ability to confirm that you are the owner of the account
    - Secure data persistance
    - Support for multiple accounts
- Added integration with our servers
    - Added synchronization of profiles
    - Added synchronization of snapshots with items
    - Added new notifications related to the server integration
    - Added indicator that shows if you're disconnected from our servers
    - Communication via websockets, with automatic reconnect
        - Using the messagepack protocol (binary)
- Added a basic chart that displays snapshot history
- Added migrations to client
- Added description to notifications
- Added link to Patreon page
##### Changed
- Reduced spacing in item table for a more minimalistic look
- Replaced the warning text in the item table with an icon
##### Removed
- Removed account name field at login screen (fetched via OAuth2 instead)
##### Fixed
- Fixed a bug where the client would loop the validation if it failed on the login page
- Fixed a bug where the relative time on notifications was not displayed correctly
- Fixed a bug where the redirection logic was not working properly in some cases
- Fixed a bug where the login container would get pushed if the menu was previously open
- Fixed a potential memory leak where we stored displayed alerts forever (in a session)

## [0.1.2] - 2019-12-18
##### Added
- Added a spinner for when a session is being initiated
##### Changed
- Changed color of a placeholder text in the item table
##### Fixed
- Fixed a bug where the error "No characters in league" would be displayed even though you had characters in the league

## [0.1.1] - 2019-12-17
##### Added
- Added settings page
    - Added setting for toggling low confidence pricing
    - Added setting for controlling the price treshold
- Added automatic retry for validate session at 30 second intervals if it fails
- Added an asterisk to profile name field in profile dialog
##### Changed
- Now displays "N/A" in the links column if the item has no links
- Stash tabs are now required to be selected before saving a profile
- Minor styling improvements to item table
##### Fixed
- Fixed a bug where some uniques were incorrectly priced as 6-links

## [0.1.0] - 2019-12-13
- Initial release
