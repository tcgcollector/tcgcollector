# TCG Collector Changelog

All notable changes to the TCG Collector project will be documented in this file.

## 0.1.0 - 2017-07-03

Beta release

## 0.2.0 - 2017-09-15

### Added

- Expansion series can now be filtered (shown or hidden) on the expansions page.
- If a single expansion card filter is active on the cards page, all cards of this expansion will be shown by default without pagination.
- A *my card collection* option has been added to the cards page.
- The card details page now displays *Evolves from* information for Pokémon.
- Premium users can now add cards with a specific language to their collection. Cards added to your collection before this feature will have *English* as default language.
- Premium users can now view the amount of each card variant type, card language or card condition per card in their collection using the card collection modal/dialog.
- Premium users can now add cards to their personal wishlist.
- A *my card wishlist* option has been added to the cards page).

### Changed

- The *check all/clear all* button for card filters has been split into 2 separate buttons.
- Reworked premium card collection management by making it more intuitive to use. Card amounts can now be increased/decreased by default (not disabled) even if no card variant type, card condition or card language is selected (by assuming defaults *Unlimited*, *English* and *Mint*).
- Moved the card variant type, card language and card conditions options to a convenient card collection options modal/dialog for premium users.

### Fixed

- Cards without an *Unlimited* card variant type can now be added to your card collection without failing.

## 0.3.0 - 2017-09-27

### Added

- A card image can now be uploaded when submitting a card.
- Added a "random card" link to the site navigation.

### Changed

- Due to technical limitations, card edits can no longer be submitted (for now). If you notice an error or missing information, please leave a comment on the card details page instead.

### Fixed

- The filtering of expansion series no longer ignores certain checkboxes.

## 0.3.1 - 2017-09-29

### Fixed

- When viewing all cards of a single expansion on the cards page, the displayed card amount did not change change if a certain card variant type was active (card collection options). For example, an expansion with 169 cards would still display 169 instead of e.g. 122 if *Reverse Holo* was active.
- The card image is now sized consistently across all card detail pages.

## 0.3.2 - 2017-10-05

### Changed

- The overal performance of the cards page has been improved because card filters are now loaded on demand instead of on page load.

### Fixed

- The card filters now get updated correctly when using the browser back and forward buttons (history).
- The switching of logged in users no longer fails after verifying the email address of a different user than the logged in one.
- Fixed a bug causing the wrong card counts to be shown on the expansions page.
- Fixed a bug causing the card filter *multiple* and *exclude* switches to remain active even if they were not checked by the user.
- Fixed a bug causing the random card feature to link to a non-existent card on rare occasions.

## 0.4.0 - 2017-10-21

### Added

- Expansions can now be added or removed to/from your card collection. Premium users can also add expansions to their collection based on their active card collection options.
- Improved security for card collection management (CSRF).

### Changed

- Pages on which card collection information is shown (expansions, cards and card details page) are no longer cached by browser history. This means using the browser back and forward buttons will always give an up to date version of the page from now on.
- Previously, if a single expansion card filter was active along with one or more other non-expansion card filters, the cards page would switch to "search mode" showing pagination. This is no longer the case.
- Made some performance optimizations to card collection management.
- Improved the card collection options "more info" text (premium).
- Improved the info messages in the card collection card modal/dialog when decreasing an aggregated or non-default card amount (premium).

### Fixed

- When viewing your card collection on the cards page, the cards in your collection ratio didn't get updated if a specific card variant type was active (card collection options).
- Fixed a bug causing the card text and illustrator name card filters not to be filled in after reloading the cards page.
- Fixed a bug causing the card submission card image to be uploaded even after it was reset.

## 0.5.0 - 2017-10-25

### Added

- Cards can now be sorted by their National Pokédex number.
- A overview of missing card images per expansion has been added. It can be accessed from the contribute section on the about page.
- Dropdowns now remember the position of the selected option.

### Fixed

- Changing the *Sort by* option on the cards page now correctly resets the card search result to the first page.
- Sorting cards by name now correctly sorts cards with the same name.

## 0.6.0 - 2017-12-13

### Added

- Images of cards which are not in your card collection now appear lighter (opacity).
- Cards can be edited again using the card submission system via the card details page (was temporarily removed in 0.3.0).
- A proper content management system for cards and expansions has been added for administrator users.
- The card details page now displays *Evolves into* information for Baby Pokémon.
- Card effects, attacks, attack energies, rules, weaknesses and resistances can now be sorted.
- An *in card collection* switch has been added to the overview of missing card images.
- More detailed error messages have been added.

### Changed

- Cards no longer have all languages by default: each language version of a card is now a card variant on its own.

### Fixed

- The "go to series" button on the mobile version of the expansions page works again.
- Clearing all card filters now collapses all card filter panels instead of only the active ones.
- The card list columns are now aligned correctly if a column contains truncated text and if the card collection checkbox/buttons column is shown.
- The *page* query string parameter now gets cleared from the URL after resetting to the first page of a card search result.
- Fixed a bug causing the card details page to hang while loading.
- Fixed a bug causing the card collection options to remain active on the card details page.
- Users now get forcefully logged out if any security related changes (such as password) were made from another session.
- The *remember me* login option no longer causes unexpected behavior.
- AJAX routes now return HTTP unauthorized (401) and HTTP forbidden (403) instead of redirecting (302) to the login page.
