# TCG Collector Changelog

All notable changes to the TCG Collector project will be documented in this file.

## 0.1.0 - 2017-07-03

Beta release

## 0.2.0 - 2017-09-15

### Added

- Expansion series can now be filtered (shown or hidden) on the expansions page.
- If the card search engine has a single expansion filter active, all the cards of this expansion will be shown by default without pagination.
- A *my card collection* option has been added on the cards page.
- Premium users can now add cards with a specific language to their collection. Cards added to your collection before this feature will have *English* as default language.
- Premium users can now view the amount of each card variant type, card language or card condition per card in their collection using the card collection modal/dialog.
- Premium users can now add cards to their personal wishlist (and a *my card wishlist* option has also been added on the cards page).

### Changed

- The *check all/clear all* button for card filters has been split into 2 separate buttons.
- The card detail page has been slightly reworked and now displays *Evolves from* information for Pokémons.
- Reworked premium card collection management by making it more intuitive to use. Card amounts can now be increased/decreased by default (not disabled) even if no card variant type, card condition or card language is selected (by assuming defaults *Unlimited*, *English* and *Mint*).
- Premium users: moved the card variant type, card language and card conditions options to a convenient card collection options modal/dialog.
- As a result of the changes mentioned above, premium users are now able to completely ignore managing cards by their card variant type, card language or card condition if they want.
- Many minor usability and design enhancements.

### Fixed

- Cards without an *Unlimited* card variant type can now be added to your card collection without failing.
- Many small bugs and security fixes.

## 0.3.0 - 2017-09-27

### Added

- A card image can now be added when submitting a card.
- Added a "random card" link to the site navigation.

### Changed

- Due to technical limitations, card edits can no longer be submitted (for now). If you notice an error or missing data, please leave a comment instead.

### Fixed

- Fixed a bug causing the filtering of expansion series to ignore certain checkboxes.

## 0.3.1 - 2017-09-29

### Fixed

- When viewing all cards of a single expansion, the displayed card amount did change change if a certain card variant type was active (card collection options). For example, an expansion with 169 cards would still display 169 instead of e.g. 122 if *Reverse Holo* was active.
- The card image is now sized consistently on all card detail pages even if the image has a greater or lower resolution.
