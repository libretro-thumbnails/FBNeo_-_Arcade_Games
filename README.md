Just like the core, this repository gets updates directly from upstream.
For this reason, it is recommended to post your Snaps/Titles upstream following the guidelines at https://wiki.neo-source.com/contribute, otherwise your changes are likely to get overwritten.

Unlike upstream, RetroArch has some limitations when displaying thumbnails :
- it can't apply a game's DAR (Display Aspect Ratio)
- it can't display thumbnails larger than 512px

In an attempt to provide the best overall thumbnails despite those limitations :
- romsets whose native resolution and DAR are deemed too different from each other are resized to a width of 512px and their DAR is applied
- romsets whose width is larger than 512px are resized to a width of 512px and their DAR is applied
- all other thumbnails use the game's native resolution

The rule for comparing native resolution against DAR goes like this :
- divide longer side by smaller side for native resolution and DAR
- compare the 2 decimals obtained
- if they aren't within a margin of 0.2 from each other, resize

Lanczos method is used for resizing.

If you disagree with any of those rules, feel free to discuss them in the issue tracker.
