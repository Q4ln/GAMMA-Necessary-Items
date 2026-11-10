# Necessary Items

Version `d2026.11.9.2`

Necessary Items adds a **Mark Necessary** entry to the inventory context menu,
next to SortingPlus's Favorite and Junk. Every item of a marked type then stays
in your inventory when you use the Move all button, a stack's move all or drop
all, Fast Transfer, companion Give All, SortingPlus's automatic junk selling,
the Unusable Parts Handler or, with a magazine mod, Quick Release. You can still
move, drop or sell a marked item one at a time when you really mean to part
with it. The mark does not change how your inventory is sorted.

## What it does

- Right-click an item in your inventory, a loot or stash screen, or a trade
  screen and choose **Mark Necessary**. Choose **Unmark Necessary** to remove
  the mark.
- The mark applies to the item type, not to one item: marking one medkit marks
  every medkit of the same kind.
- Marked items show a short coloured tab along the top of their cell in your
  inventory and in stash, loot and trade lists. It moves aside for GAMMA's stack
  count and artefact condition. The colour says which marks the item type has:
  green for Favorite, red for Junk, bone for Necessary, blue for Favorite +
  Necessary and magenta for Junk + Necessary. Equipment, belt and quick slots
  and the two trade offer panes show no tab.
- Marks are saved in your save file. Each save has its own set of marked types.
- Necessary works alongside Favorite and Junk: a type can be Favorite +
  Necessary or Junk + Necessary. Favorite and Junk still control the sort
  order; Necessary only controls whether bulk and automatic actions may move the
  type.

Marked types stay with you during:

- the **Move all** button (and its keyboard shortcut) in a loot or stash
  screen;
- a stack's **move all**, including Ctrl bulk moves into a stash or a trade
  offer;
- **any Shift-hover transfer** with GAMMA's Fast Transfer, whether of a stack or
  of a single item;
- a stack's **drop all**;
- the **Quick Release** emergency backpack drop (needs a magazine mod, see
  Requirements);
- companion dialogue **Give All**, including its carry-weight check;
- SortingPlus putting Junk into the trade offer automatically when trade opens;
- the **Unusable Parts Handler** deleting, donating, selling or dumping parts;
- the auto-stacking in Jack Harris's Anti Lag (GAMMA's development branch), which
  would otherwise merge partly used items with an open stash or body. Partly
  used items of a marked type stay separate there, even inside your inventory.

What it deliberately leaves alone:

- Single-item **Move**, **Drop** and manual selling still work on marked items.
  That is the intended way to part with a marked type.
- Taking items out of a stash, a body or a trader is never blocked.
- It adds no sort category and never re-sorts your inventory.
- Other mods that honour SortingPlus's Favorite through their own settings keep
  doing so.

## Requirements

- S.T.A.L.K.E.R. Anomaly 1.5.3.
- GAMMA, modpack definition 920. Built and checked against it; only briefly
  tested in game, see Known issues. SortingPlus, with RAX Dynamic Custom
  Functors (puts the menu entry next to Favorite and Junk) and RAX Dynamic Icon
  Layers (draws the tabs), is part of GAMMA.
- For Quick Release retention only: a magazine mod that provides
  `actor_stash_patch.script`, for example Anomaly Magazines Redux
  ("Mags Redux", by Arti and RavenAscendant), which GAMMA's mod list carries as
  an optional mod that is off by default
  (`207- Mags Redux (Disable G.A.M.M.A. Unjam Reload)`), or GAMMA Mags Reloaded
  (by Priler, released by andtheherois), a separately downloaded fork of Mags
  Redux that is not part of GAMMA. Mags Redux needs GAMMA's
  `G.A.M.M.A. Unjam Reload on the same key`, on by default, switched off, and
  both are full magazine systems that change how weapons are loaded. Without
  one, Quick Release drops marked types like any other item; every other
  protection still works.
- Fast Transfer and the Unusable Parts Handler are optional. When either is
  missing, its protection is simply skipped.
- No Modded Exes feature is needed: the mod uses only script functions that
  Anomaly 1.5.3 and GAMMA already provide.

## Installation

Install the archive with Mod Organizer 2 and enable it. It overwrites no files;
MO2 priority does not matter. Restart the game after installing or updating.

When it loads, the game log (`xray_<user>.log` in Anomaly's `appdata\logs`
folder) contains one line naming the build:
`[Necessary Items] installed | build=d2026.11.9.2 | section marks and bulk guards active`.

## Compatibility and conflicts

- **SortingPlus:** SortingPlus's MCM option Block "Move all" for Favorites, on
  by default in GAMMA, keeps Favorites back when you use the Move all button.
  Necessary Items switches that protection off for the moment of each Move all,
  so that Necessary, not Favorite, decides what Move all leaves behind. Your
  SortingPlus setting itself is not changed, Favorite still sorts normally, and
  the setting works again as soon as this mod is removed. The tabs show Favorite
  and Junk whatever SortingPlus's own icon and highlight options are set to; if
  you turn those options on, its icons and highlights appear as well.
- **Fast Transfer, Unusable Parts Handler, companions, Quick Release:** the mod
  adds a filter in front of each of these and otherwise passes every call
  through unchanged, so it composes with other mods that hook the same
  functions.
- **Inventory screen:** it wraps the inventory screen's Move all button, move,
  move all, drop all and SortingPlus junk-to-trade actions. Its script name
  sorts late on purpose, so it wraps the final GAMMA versions of those actions.
- No known conflicts.

## Options

No options. The mark is set per item type from the context menu.

## Adding or removing mid-save

- **Adding:** safe. Existing saves load with no marked types; the first save
  you make afterwards stores the mod's marks.
- **Removing:** safe. The marks stay in your save under the mod's own key, but
  nothing reads them, so they are inert. Items return to normal behaviour
  immediately.

## Uninstall

Disable or remove the mod in MO2. Nothing else needs to be undone: it changes no
settings, and the leftover marks in your saves are ignored.

## Known issues

- This build passed a scripted in-game check at 1920x1080 on the author's own
  install of GAMMA modpack definition 920, with GAMMA Mags Reloaded and other
  mods added, covering the tabs, marks from an existing save, the Move all
  button, a stack's move all and drop all, Fast Transfer of a stack and
  single-item moves out of the inventory. A script called those actions, so real
  clicks and the open context menu were not part of it. Not yet checked in game:
  the trade screen and automatic junk selling, companion Give All, Quick Release,
  the Unusable Parts Handler, the Anti Lag auto-stacking, a single-item Drop,
  taking marked items out of a stash or body, a single-item Fast Transfer, the
  belt, adding the mod to a save or removing it, a save written by this build,
  other resolutions and the Russian menu text.
- Without RAX Dynamic Icon Layers the tabs are not drawn, and the log says so.
  The marks and every protection still work.
- Without SortingPlus, tabs show only Necessary.
- On cells a trader refuses, the red tint also colours the tab, so Junk,
  Necessary and Junk + Necessary look alike there.
- On screens wider than about 22:9, such as 32:9, the stack count can still
  cover part of the tab on stacked items one cell wide.
- Without Mags Redux or GAMMA Mags Reloaded enabled (GAMMA's default has
  neither), Quick Release does not keep marked types.
- While this mod is enabled, SortingPlus's MCM option Block "Move all" for
  Favorites (on by default in GAMMA) has no effect, so the Move all button moves
  Favorite types; mark those types Necessary instead.

## Changelog

### d2026.11.9.2

- First public release.

## Credits

Necessary Items copies no code or assets from other mods. It integrates with
them through their public functions, and thanks their authors:

- RavenAscendant: SortingPlus, RAX Dynamic Custom Functors and RAX Dynamic Icon
  Layers.
- Ishmaeel (Ishy): Fast Transfer.
- G_FLAT: Unusable Parts Handler.
- Arti and RavenAscendant: Anomaly Magazines Redux (Mags Redux), whose
  `actor_stash_patch.script` Quick Release hook this mod adds its condition to.
- Priler and andtheherois: GAMMA Mags Reloaded, which carries the same hook.
- The GAMMA team: GAMMA, the Better Quick Release System and the GAMMA Fast
  Transfer fix.

## Licence

The mod's own code is licensed under CC BY-NC-SA 4.0. See `Necessary Items - LICENSE.txt`.
