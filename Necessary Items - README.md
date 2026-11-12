# Necessary Items

Version `d2026.11.12.1`

Necessary Items adds a **Mark Necessary** entry to the inventory context menu,
next to SortingPlus's Favorite and Junk. Every item of a marked type then stays
in your inventory when you use the Move all button, a stack's move all or drop
all, Fast Transfer, companion Give All, SortingPlus's automatic junk selling,
the Unusable Parts Handler or, with a magazine mod, Quick Release. A second
entry, **Mark Item Necessary**, gives the same protection to one particular
item, such as your own rifle or suit, without marking every other item of its
kind. You can still move, drop or sell a marked item one at a time when you
really mean to part with it. The marks do not change how your inventory is
sorted.

## What it does

- Right-click an item in your inventory, a loot or stash screen, or a trade
  screen and choose **Mark Necessary**. Choose **Unmark Necessary** to remove
  the mark.
- The mark applies to the item type, not to one item: marking one medkit marks
  every medkit of the same kind.
- To protect one item only, choose **Mark Item Necessary**, just below Mark
  Necessary, and **Unmark Item Necessary** to remove it. See Marking a single
  item below.
- Marked items show a short coloured tab along the top of their cell in your
  inventory and in stash, loot and trade lists. It moves aside for GAMMA's stack
  count and artefact condition. The colour says which marks the item has:
  green for Favorite, red for Junk, bone for Necessary, blue for Favorite +
  Necessary and magenta for Junk + Necessary. A single marked item shows the
  same tab as a marked type. Equipment, belt and quick slots and the two trade
  offer panes show no tab.
- Marks are saved in your save file. Each save has its own set of marked types
  and items.
- Necessary works alongside Favorite and Junk: a type can be Favorite +
  Necessary or Junk + Necessary. Favorite and Junk still control the sort
  order; Necessary only controls whether bulk and automatic actions may move the
  item.

Marked types and marked items stay with you during:

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
- the auto-stacking in GAMMA's Auto-Stacking Items, which merges partly used
  items of one kind in your inventory and deletes the emptied ones: it leaves a
  kind alone while you carry a partly used item of it marked with Mark Item
  Necessary;
- the auto-stacking in Jack Harris's Anti Lag (GAMMA's development branch), which
  would otherwise merge partly used items with an open stash or body. Partly
  used items of a marked type, or of a kind with a partly used marked item, stay
  separate there, even inside your inventory.

What it deliberately leaves alone:

- Single-item **Move**, **Drop** and manual selling still work on marked items.
  That is the intended way to part with a marked item.
- Taking items out of a stash, a body or a trader is never blocked.
- It adds no sort category and never re-sorts your inventory.
- Other mods that honour SortingPlus's Favorite through their own settings keep
  doing so.

Marking a single item:

- **Mark Item Necessary** appears on an item you carry when it is a kind that
  can take an item mark and its type is not already marked Necessary, since a
  type mark already covers every item of the type. **Unmark Item Necessary**
  appears on a marked item wherever it is listed: your inventory, a stash, a
  body or a trader. Neither entry appears on the repair screen.
- The marked item leaves its stack and gets a cell of its own, with the same
  tab as a marked type. Unmarking puts it back into the stack.
- Every action listed above except auto-stacking keeps it back, exactly like a
  marked type, while identical unmarked items of the same kind move as usual.
  Auto-stacking works per kind instead, as described above.
- Items that can take an item mark: guns, grenade launchers and knives;
  binoculars; armour, exoskeletons and helmets; devices such as detectors,
  flashlights, night vision and your own PDA; artefacts and other belt items;
  workshop toolkits; keepsakes such as the watch, the photo, guitars, the
  harmonica and the field cooker; items that wear out with use and then vanish,
  such as disassembly tools and perk artefacts; exoskeleton power units;
  scopes, silencers, underbarrel grenade launchers and other weapon
  attachments; artefact containers and the artefacts packed in them; and, with
  a magazine mod (see Requirements), magazines, mag pouches, side saddles and
  backpacks.
- Items that cannot: consumables such as food, drinks and medicine,
  ammunition, grenades, repair and cleaning kits, weapon and armour parts,
  money, recipes, batteries, tents and sleeping bags, glowsticks and lamps,
  quest items and hideout furniture. A type mark still works on all of these.

The mark belongs to that one item and follows it:

- through saving and loading, level changes and stashes, and in a trader's
  stock until the trader restocks;
- when the game rebuilds a gun, as it does when you fit or remove a GAMMA scope
  or switch a 3DSS magnifier;
- through parts you fit and remove again. A marked scope, silencer or grenade
  launcher fitted to a gun, a magazine loaded into a gun, an exoskeleton power
  unit, a mag pouch on a suit, a side saddle on a gun, and a backpack deployed
  as a stash all come back marked when you take them off or pick them up.
  Disassembling a gun returns its marked attachments marked. While a part is
  fitted, the gun, suit or stash holding it does not itself count as
  Necessary, nothing on it shows the part's mark, and the part can only be
  unmarked once it is removed;
- into an artefact container: packing a marked artefact, or any artefact into a
  marked container, gives the packed item the mark, and opening it gives each
  its own mark back. A packed item you mark yourself gives its mark to the
  artefact when you open it;
- when you retool a marked magazine: the new magazine is marked.

The mark ends when the item is destroyed, used up or taken apart.

## Requirements

- S.T.A.L.K.E.R. Anomaly 1.5.3.
- GAMMA, modpack definition 920. Built and checked against it; only partly
  tested in game, see Known issues. SortingPlus, with RAX Dynamic Custom
  Functors (puts the menu entries next to Favorite and Junk) and RAX Dynamic
  Icon Layers (draws the tabs), is part of GAMMA.
- Type marks need no Modded Exes feature. Item marks need the Modded Exes'
  server object callbacks, which GAMMA ships. Without them Mark Item Necessary
  is never offered, and the log says
  `[Necessary Items] server object callbacks unavailable: Mark Item is not offered`.
- For Quick Release retention: a magazine mod that provides
  `actor_stash_patch.script`, for example Anomaly Magazines Redux
  ("Mags Redux", by Arti and RavenAscendant), which GAMMA's mod list carries as
  an optional mod that is off by default
  (`207- Mags Redux (Disable G.A.M.M.A. Unjam Reload)`), or GAMMA Mags Reloaded
  (by Priler, released by andtheherois), a separately downloaded fork of Mags
  Redux that is not part of GAMMA. Mags Redux needs GAMMA's
  `G.A.M.M.A. Unjam Reload on the same key`, on by default, switched off, and
  both are full magazine systems that change how weapons are loaded. Without
  one, Quick Release drops marked items like any other item; every other
  protection still works.
- Some kinds of item take an item mark only with the mod that handles them.
  Magazines need Mags Redux or GAMMA Mags Reloaded; mag pouches and side saddles
  come with GAMMA Mags Reloaded; backpacks need one of those two magazine mods.
  If a script that changes a kind of item is missing, or no longer has the
  functions this mod follows, that kind is simply not offered Mark Item
  Necessary.
- Fast Transfer and the Unusable Parts Handler are optional. When either is
  missing, its protection is simply skipped.

## Installation

Install the archive with Mod Organizer 2 and enable it. It overwrites no files;
MO2 priority does not matter. Restart the game after installing or updating.

When it loads, the game log (`xray_<user>.log` in Anomaly's `appdata\logs`
folder) contains one line naming the build:
`[Necessary Items] installed | build=d2026.11.12.1 | section and item marks and bulk guards active`.

## Compatibility and conflicts

- **SortingPlus:** SortingPlus's MCM option Block "Move all" for Favorites, on
  by default in GAMMA, keeps Favorites back when you use the Move all button.
  Necessary Items switches that protection off for the moment of each Move all,
  so that Necessary, not Favorite, decides what Move all leaves behind. Your
  SortingPlus setting itself is not changed, Favorite still sorts normally, and
  the setting works again as soon as this mod is removed. The tabs show Favorite
  and Junk whatever SortingPlus's own icon and highlight options are set to; if
  you turn those options on, its icons and highlights appear as well.
- **Fast Transfer, Unusable Parts Handler, companions, Quick Release,
  auto-stacking:** the mod adds a filter in front of each of these, including
  Auto-Stacking Items' `zatura_autostack.stack_item`, and otherwise passes every
  call through unchanged, so it composes with other mods that hook the same
  functions.
- **Inventory screen:** it wraps the inventory screen's Move all button, move,
  move all, drop all and SortingPlus junk-to-trade actions, and the inventory
  lists' stacking check (`UICellContainer:FindSimilar`), which it asks again
  with marked cells hidden, so the other stacking rules still decide. Its script
  name sorts late on purpose, so it wraps the final GAMMA versions of those
  actions.
- **Item marks:** to follow marked items, it also wraps these functions while
  the game runs; each wrapper reads what it needs, then calls the original with
  the same arguments and returns its results unchanged. Anomaly's
  `alife_clone_weapon`, `item_parts.disassembly_weapon`,
  `utils_item.attach_addon` and `detach_addon`, and `item_weapon.attach_scope`,
  `detach_scope` and `toggle_silencer`; G.A.M.M.A. Armors repair like WPO's
  `item_exo_device.install_psu` and `remove_psu`; G.A.M.M.A. Better Quick
  Release System's `item_backpack.actor_on_item_take_from_box`; G.A.M.M.A.
  Artefacts Reinvention's `itms_manager.dropdrop_ArtyContainer` and
  `use_arty_container`; the magazine mods' `magazines.retool_mag_functor` and
  `timer_eject_magazine`; GAMMA Mags Reloaded's `mag_pouches.install_pouch`,
  `remove_pouch`, `speed_loaders.install_loader` and `remove_loader`;
  Interaction Dot Marks' `ui_hud_dotmarks.deploy_backpack` and
  `remove_placed_backpack`; the Quick Action Wheel's `QScopeWheelOption`
  `Attach` and `Detach`; and 3DSS's `magnifier_switch.bind_dummy`. It listens
  to the Modded Exes' server object callbacks and to `actor_on_item_take` and
  `actor_on_before_stash_create`. The pouch, saddle and backpack pick-up
  functions are wrapped as the scripts load, the rest at game start after
  Toggle Scope and the magazine mods have added their own wrappers. When one of
  these mods is missing, only the kinds of item it handles lose Mark Item
  Necessary.
- No known conflicts.

## Options

No options. Marks are set per item type or per item from the context menu.

## Adding or removing mid-save

- **Adding:** safe. Existing saves load with no marked types or items; the
  first save you make afterwards stores the mod's marks.
- **Removing:** safe. The marks stay in your save under the mod's own keys, and
  a marked magazine keeps one extra entry in its magazine mod's record, which
  the magazine mods ignore. Nothing reads them, so they are inert. Items return
  to normal behaviour immediately, and parts removed later come back unmarked.
- **Adding it back after playing without it:** marked types return as they
  were. Item marks are checked when the save loads and dropped for items that
  no longer exist. In rare cases an item of the same kind that the game created
  while the mod was off reuses a destroyed marked item's internal number and
  then shows as marked; unmark it if that happens.

## Uninstall

Disable or remove the mod in MO2. Nothing else needs to be undone: it changes no
settings, and the leftover marks in your saves and magazine records are ignored.

## Known issues

- Type marks passed a scripted in-game check on the previous build, and item
  marks on this one, both at 1920x1080 on the author's own install of GAMMA
  modpack definition 920 with GAMMA Mags Reloaded and other mods added. A script
  called the actions and the context menu's own entries directly, without
  clicking, so real clicks were not part of either. Item marks were checked over
  two launches, the second loading a save written by the first: the two menu
  entries in the inventory screen, their place right after Mark Necessary, and
  Mark Item appearing on keepsakes, helmets, a gun, scopes, a silencer,
  magazines, a power unit, a mag pouch, a side saddle, an artefact and a
  backpack you carry but not on food; the cell of its own and its tab;
  unmarking and marking again; the Move all button, a stack's move all and drop
  all (also with a marked item inside the stack), Fast Transfer and single-item
  moves; fitting and removing a GAMMA scope and a silencer; a gun's
  disassembly; loading, ejecting and retooling a magazine; exoskeleton power
  units, mag pouches and side saddles; packing a marked artefact into a
  container and opening it; a backpack's Create stash and pick-up; a destroyed
  item losing its mark; and marks on items and fitted parts surviving a save
  and reload.
- Not yet checked in game: Quick Release itself (only the check that keeps an
  item back was run); the trade screen and automatic junk selling; companion
  Give All; the Unusable Parts Handler; both kinds of auto-stacking; a
  single-item Drop; taking marked items out of a stash or body; the belt; the
  menu entries in a stash, body or trade list, on the repair screen and on a
  type already marked Necessary; Mark Item on knives, binoculars, armour,
  devices, workshop toolkits, wear-out items and artefact containers; a marked
  container or a packed item marked by hand; the silencer key; Interaction Dot
  Marks' backpack deploy and pick-up; the Quick Action Wheel; Toggle Scope;
  3DSS dummy scopes and magnifier switches; underbarrel grenade launchers;
  engine scopes such as the PU; a scope's own Use action; level changes; a
  trader restocking; adding the mod to a save or removing it; other
  resolutions; and the Russian menu text.
- An NPC who picks a marked item up from the ground ends its mark, except on a
  gun.
- Quest hand-ins and crafting choose items by type, so they can take a marked
  item.
- The Knot turning into Lucifer and the Bat's transmutation produce an unmarked
  artefact.
- Using items up by hand can spend a marked item, for example as melter fuel,
  for the Lucifer sacrifice or as a repair-support item.
- A Fast Transfer of a stack that somehow contains a marked item moves that
  item too. A marked item normally never joins a stack.
- Nothing shows the mark of a part fitted to a gun, suit or stash; remove the
  part to see or change it.
- A magazine offers Mark Item Necessary only once the magazine mod has set it
  up, a moment after it appears.
- Without RAX Dynamic Icon Layers the tabs are not drawn, and the log says so.
  The marks and every protection still work.
- Without SortingPlus, tabs show only Necessary.
- On cells a trader refuses, the red tint also colours the tab, so Junk,
  Necessary and Junk + Necessary look alike there.
- On screens wider than about 22:9, such as 32:9, the stack count can still
  cover part of the tab on stacked items one cell wide.
- Without Mags Redux or GAMMA Mags Reloaded enabled (GAMMA's default has
  neither), Quick Release does not keep marked items, and backpacks are not
  offered Mark Item Necessary.
- While this mod is enabled, SortingPlus's MCM option Block "Move all" for
  Favorites (on by default in GAMMA) has no effect, so the Move all button moves
  Favorite types; mark those types Necessary instead.

## Changelog

### d2026.11.12.1

- New **Mark Item Necessary** and **Unmark Item Necessary** entries mark one
  item instead of its whole type. The marked item gets a cell of its own with
  the Necessary tab and is kept back by the same bulk and automatic actions as
  a marked type, while identical unmarked items move as usual.
- An item mark follows its item through saves, level changes, stashes and
  traders, gun rebuilds, parts fitted and removed again (weapon attachments,
  magazines, exoskeleton power units, mag pouches, side saddles), packed
  artefacts and deployed backpacks.
- A stack's move all and drop all keep back a marked item that sits inside the
  stack. GAMMA's Auto-Stacking Items leaves a kind alone while you carry a
  partly used item of it marked with Mark Item Necessary.
- Item marks need the Modded Exes' server object callbacks, which GAMMA ships.
  Type marks still need none.
- Each integration now installs on its own: one that fails is logged once and
  costs only itself.
- The install log line now ends `section and item marks and bulk guards active`.

### d2026.11.9.2

- First public release.

## Credits

Necessary Items copies no code or assets from other mods. It integrates with
them through their public functions, and thanks their authors:

- RavenAscendant: SortingPlus, RAX Dynamic Custom Functors, RAX Dynamic Icon
  Layers and the stacking control the magazine mods carry.
- Ishmaeel (Ishy): Fast Transfer.
- G_FLAT: Unusable Parts Handler.
- Arti and RavenAscendant: Anomaly Magazines Redux (Mags Redux), whose
  `actor_stash_patch.script` Quick Release hook this mod adds its condition to,
  and whose magazine records carry item marks.
- Priler and andtheherois: GAMMA Mags Reloaded, which carries the same hook and
  the mag pouches and side saddles that item marks follow.
- demonized: the Modded Exes, whose server object callbacks item marks rely on.
- Arti, Momopate and Fermuto: Weapon Parts Overhaul, Barrel Condition Effects
  Display and Part Disassembly Fix, which make up the weapon disassembly the
  mod follows.
- Catspaw: Interaction Dot Marks.
- HarukaSai: Quick Action Wheel.
- Redotix99, andtheherois and party50: 3DSS for GAMMA.
- Zatura: Auto-Stacking Items, and Jack Harris, whose Anti Lag carries an
  improved copy of it.
- The GAMMA team: GAMMA, the Better Quick Release System, the GAMMA Fast
  Transfer fix, Artefacts Reinvention and Armors repair like WPO.

## Licence

The mod's own code is licensed under CC BY-NC-SA 4.0. See `Necessary Items - LICENSE.txt`.
