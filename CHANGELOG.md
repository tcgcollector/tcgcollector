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
- The card detail page has been slightly reworked and now displays *Evolves from* information for Pokémon.
- Reworked premium card collection management by making it more intuitive to use. Card amounts can now be increased/decreased by default (not disabled) even if no card variant type, card condition or card language is selected (by assuming defaults *Unlimited*, *English* and *Mint*).
- Moved the card variant type, card language and card conditions options to a convenient card collection options modal/dialog for premium users.
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

- Due to technical limitations, card edits can no longer be submitted (for now). If you notice an error or missing data, please leave a comment on the card detail page instead.

### Fixed

- Fixed a bug causing the filtering of expansion series to ignore certain checkboxes.

## 0.3.1 - 2017-09-29

### Fixed

- When viewing all cards of a single expansion on the cards page, the displayed card amount did not change change if a certain card variant type was active (card collection options). For example, an expansion with 169 cards would still display 169 instead of e.g. 122 if *Reverse Holo* was active.
- The card image is now sized consistently on all card detail pages even if the image has a greater or lower resolution.

## 0.3.2 - 2017-10-05

### Changed

- The overal performance of the cards page has been improved because from now on the card filters are only loaded when the *card filters* button is clicked (and not on page load).

### Fixed

- The card filters now get updated correctly when using the browser back and forward buttons (history).
- Fixed a bug causing an error when logging in after verifying your email address.
- Fixed a bug causing the wrong card counts to be shown on the expansions page.
- Fixed a bug causing the card filter *multiple* and *exclude* switches to remain active even if they were not checked by the user.
- Fixed a bug causing the random card feature to link to a non-existent card on rare occasions.
- Made some minor visual improvements to the card detail page.
- Fixed some minor user interface bugs.

## 0.4.0 - 2017-10-21

### Added

- Expansions can now be added or removed to/from your card collection. Premium users can also add expansions to their collection based on their active card collection options.

### Changed

- Pages on which card collection information is shown (expansions, cards and card detail page) are no longer cached by browser history. This means using the browser back and forward buttons will always give an up to date version of the page from now on.
- Previously, if a single expansion card filter was active along with one or more other non-expansion card filters, the cards overview would switch to "search mode". This is no longer the case.
- Improved security for card collection management (CSRF).
- Made some performance optimizations to card collection management.
- Improved the card collection options "more info" text (premium).
- Improved the info messages in the card collection card modal/dialog when decreasing an aggregated or non-default card amount (premium).

### Fixed

- When viewing your card collection on the cards page, the cards in your collection ratio didn't get updated if a specific card variant was selected.
- Fixed a bug causing the card text and illustrator name card filters not to be filled in when active.
- Fixed a bug causing the card submission card image to be uploaded even after it was reset.
