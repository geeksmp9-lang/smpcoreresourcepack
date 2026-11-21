# Source of the warped-door textures in this `minecraft/` override folder

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
