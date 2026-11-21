# Source of the overrides in this `minecraft/` override folder

Currently empty on purpose.

The Warped Door "glass" look and the FNAF curtain/tile decor both used to live
here as global texture overrides on real vanilla blocks (`minecraft:warped_door`,
and later a handful of command-block-family blocks) - meaning every real
vanilla instance of those blocks rendered with our custom look too, not just
our own custom blocks disguised as them.

We've since decided every custom block/item the mod adds must be a genuinely
separate thing from day one, never a global reskin of a real vanilla block -
some players don't want their own real doors turned into glass, for example.

Both of these now ship as real, unique-looking blocks via Polymer's
`polymer-blocks` module instead (`eu.pb4.polymer.blocks.api.PolymerTexturedBlock`),
with their own models and textures bundled directly in the mod jar
(`geeksmpcore`'s `src/main/resources/assets/smpcore/...`) and served by
Polymer's own resource-pack module at runtime - not through this repo at all.
See `dev.smp.smpitems.SmpItemsMod` in the private `geeksmpcore` repo for the
current implementation and version history (GlassDoorBlock, FnafDecorBlock).

If a future override here ever again needs to touch a real vanilla block's
own texture globally, document it here the same way the old entries did, and
get it clearly signed off first - that tradeoff is no longer the default.
