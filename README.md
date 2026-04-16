Just like the core, this repository gets updates directly from upstream.
For this reason, it is recommended to post your Snaps/Titles upstream following the guidelines from https://wiki.neo-source.com/contribute, otherwise your changes are likely to be overwritten.

RetroArch has some limitations upstream doesn't have when displaying thumbnails :
- it can't apply a game's DAR (Display Aspect Ratio)
- it can't display thumbnails larger than 512px

In an attempt to provide the best overall thumbnails despite those limitations :
- romsets whose native resolution and DAR are deemed too different are resized to a width of 512px and their DAR is applied
- romsets whose width is larger than 512px are resized to a width of 512px and their DAR is applied
- all other thumbnails use the game's native resolution
