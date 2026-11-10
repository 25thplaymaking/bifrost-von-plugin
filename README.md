# Bifrost VON TeamSpeak Plugin

The TeamSpeak 3 plugin for [Bifrost VON](https://github.com/25thplaymaking/bifrost-von), the Arma Reforger radio mod.
Install it to talk on the in-game radio through TeamSpeak.

> **Credit where it's due.** Bifrost VON and this plugin are built on **Coalition VON** and the **Coalition
> TeamSpeak Plugin** by [CoalitionArma](https://github.com/CoalitionArma/Coalition-VON). They made the radio system
> and released it as open source; Bifrost VON adds to their work under the Arma Public License (APL). This fork is
> not made or endorsed by CoalitionArma, so please report Bifrost VON problems
> [here](https://github.com/25thplaymaking/bifrost-von-plugin/issues), not to them.

## Download

**[Latest release](https://github.com/25thplaymaking/bifrost-von-plugin/releases/latest)**: version 3.1.0,
file `Bifrost_VON_TeamSpeak_Plugin_3.1.0.ts3_plugin`
([direct download](https://github.com/25thplaymaking/bifrost-von-plugin/releases/download/v3.1.0/Bifrost_VON_TeamSpeak_Plugin_3.1.0.ts3_plugin)).

Task Force Halberd members: **Bifrost Comms installs and updates this plugin for you.** Use the steps below only if
you'd rather do it by hand, or Bifrost Comms can't.

## What you need

- Windows, 64-bit.
- **TeamSpeak 3**, version 3.6 or newer, 64-bit. TeamSpeak 5 and 6 can't run TeamSpeak 3 plugins; you can keep them
  installed next to TeamSpeak 3.
- Microsoft's **Visual C++ runtime (x64)**:
  [vc_redist.x64.exe](https://aka.ms/vs/17/release/vc_redist.x64.exe). Most PCs already have it.
- A server running the **Bifrost VON** mod.

## Install by hand

1. **Quit TeamSpeak 3 completely**: right-click its tray icon, then Quit. TeamSpeak keeps the old plugin file locked
   while it runs.
2. **Download** the `.ts3_plugin` file from the [latest release](https://github.com/25thplaymaking/bifrost-von-plugin/releases/latest).
3. **Double-click it.** TeamSpeak's Addon Installer opens; click **Yes** to install, then **OK**.
4. **Start TeamSpeak 3** and open Tools > Options > Addons > Plugins. **Bifrost VON TeamSpeak Plugin (Coalition VON
   fork)**, version 3.1.0, should be there and ticked. If it isn't ticked, tick it and restart TeamSpeak.
5. **Check it in game:** join a Bifrost VON server. A few seconds after you spawn, the join notice says
   "Plugin 3.1.0" and whether you're in the VON channel.

Had the Coalition plugin before? You don't need to remove it. Both use the same file name, so this one replaces it.

### If double-clicking doesn't open the installer

Copy the plugin file in yourself:

1. Quit TeamSpeak 3.
2. Rename `Bifrost_VON_TeamSpeak_Plugin_3.1.0.ts3_plugin` to `.zip` and open it.
3. Copy `plugins\CRF_Teamspeak_Plugin_Main.dll` into `%APPDATA%\TS3Client\plugins` (paste that into Explorer's
   address bar). If you told TeamSpeak's installer to keep its settings in its own folder, the place is
   `<TeamSpeak folder>\config\plugins` instead.
4. Replace the file when Windows asks, then carry on from step 4 above.

## When it doesn't work

| What you see | What to do |
|---|---|
| The game says **"Teamspeak Plugin Not Detected"** | TeamSpeak 3 has to be running, connected to your unit's server, with that server's **tab selected** (the plugin only works on the selected tab). Check the plugin is ticked (step 4). |
| The plugin is listed but won't load | Install the Visual C++ runtime (link above) and restart TeamSpeak. |
| **"Version Mismatch"** on a **Coalition VON** server | Coalition VON servers need Coalition's own plugin (3.0.1). Bifrost VON servers take 3.0.1 or newer and ask for 3.1.0. Install the plugin that matches the server's mod. |
| You start Reforger with `-profile` | The plugin only looks in `Documents\My Games\ArmaReforger\profile`. Remove `-profile`, or link that folder to the one you use. |

To remove the plugin: TeamSpeak 3, Tools > Options > Addons, select it, then Remove.

## Checksums (SHA-256)

| File | SHA-256 |
|---|---|
| `Bifrost_VON_TeamSpeak_Plugin_3.1.0.ts3_plugin` | `b57ceb1445edf740085790cc148232d89d6a31634d92ddd473c959b7c921e430` |
| `plugins/CRF_Teamspeak_Plugin_Main.dll` inside it | `933c843b5efd68885152e80f1116f2d311bec73c574a2ef628169109ac168ca6` |

## Source and license

The plugin's source is in [25thplaymaking/bifrost-von](https://github.com/25thplaymaking/bifrost-von), folder
`CoalitionTeamspeakPlugin`. Licensed under the [Arma Public License (APL)](LICENSE.md), like the original:
attribution, non-commercial, Arma only, share alike.

Original work: Coalition VON and the Coalition TeamSpeak Plugin by CoalitionArma (Salamiboio / SalamiBoiDev, Troy /
the tanaKa, Njpatman, Björn Dahlgren and contributors), https://github.com/CoalitionArma/Coalition-VON.
Fork: Task Force Halberd.
