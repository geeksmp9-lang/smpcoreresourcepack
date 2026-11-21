# Source of the overrides in this `minecraft/` override folder

## Warped Door (glass look)

`textures/block/warped_door_bottom.png`, `textures/block/warped_door_top.png`, and
`textures/item/warped_door.png` here are **not our own art** - they're taken from
**"GlassDoors"**, a third-party community resource pack add-on by **TheKobro**
(~2020, targets resource `pack_format: 5`), which reskins vanilla door textures
with genuine binary-alpha ("cutout") transparency so the door looks like real glass.

These specifically back `smpcore:glass_door` (see `dev.smp.smpitems.SmpItemsMod` in
the mod source) - a real custom door block/item that Polymer-disguises as a vanilla
Warped Door, so this global override of `minecraft:warped_door`'s own textures is
what actually makes it look like glass. Heads up: this swap is global, so any real
vanilla Warped Door placed on the server will also render as glass.

Not redistributed as a standalone pack - just these three files, folded into our
own resourcepack, with this note kept so the origin stays clear since this repo
is public.

## FNAF curtain/tile decor (v2 - command-block-family overrides)

A first version reskinned 16 real Carpet/Wool colors server-wide and hit normal
builds using those colors - reverted. This version instead reskins the small set
of vanilla blocks nobody can obtain or place without commands: `command_block`,
`chain_command_block`, `repeating_command_block`, `structure_block`, `jigsaw`.
Same global-reskin mechanism as everything else here, but since these never show
up in anyone's actual building, the trade costs nothing this time.

`textures/block/command_block_{front,back,side}.png`,
`chain_command_block_{front,back,side}.png`,
`repeating_command_block_{front,back,side}.png` (each a 16x64 sheet - 4 identical
stacked frames, since these textures animate in vanilla and the frames need to
match for that not to look broken - with their original `.mcmeta` files copied
alongside), plus `structure_block*.png` (all 4 mode variants) and
`jigsaw_{top,side,bottom}.png`, are FNAF-mod art (see `fnaf_decor_refs/SOURCE.md`
in the private geeksmpcore repo for the full attribution/license note - same
"All Rights Reserved" fan mod as before).

Backs 5 of the 16 planned `smpcore:fnaf_curtain_*`/`fnaf_tile_*` blocks (see
`dev.smp.smpitems.SmpItemsMod`) - the other 11 are registered in code but have
no texture override yet, pending a proper fix (Polymer virtual block models +
Geyser custom blocks) that doesn't run out of safe vanilla blocks to borrow.

