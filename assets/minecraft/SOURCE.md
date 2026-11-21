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

## FNAF curtain/tile decor (carpet + wool overrides)

`textures/block/{black,brown,white,cyan,gray,light_blue,lime,orange}_carpet.png`
and `textures/block/{white,black,blue,red,light_gray,gray,cyan,green}_wool.png`
here are also not our own art - taken from **"The Five Nights at Freddy's Mod"**
(`fnaf_mod` v4, the "4.6 Halloween Snapshot" build), a fan-made FNAF mod for
Minecraft 1.20.1 whose own `mods.toml` declares **"All Rights Reserved"**
(credits: Rashi, ItsIdyllic, MarceloGToonz, 9R4ND, RoyalB, DrLoganBlox07, Yuki,
Here'sJade, NiksonTF2, Mephilis, ClownfullProductions, Hollow Studios, AnXavers;
"FNaF Belongs to Scott Cawthon"). See `../../fnaf_decor_refs/SOURCE.md` in the
private geeksmpcore mod-source repo for the fuller note on that license.

These back 16 `smpcore:fnaf_curtain_*` / `smpcore:fnaf_tile_*` blocks (see
`dev.smp.smpitems.SmpItemsMod`), each Polymer-disguised as one specific colored
vanilla Carpet (curtains) or Wool (tiles) block - so this override reskins that
one color, server-wide, for every real vanilla carpet/wool block of that color too.

