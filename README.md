A custom modpack created for me and my friends, with some mods to keep everyone interested!

## Themes for the pack

- Automation
- Magic
- Technology

## Playing the pack

To install this pack is to use the [packwiz installer bootstrap](https://github.com/packwiz/packwiz-installer-bootstrap/releases). I've tested this setup using
both [ATLauncher](https://atlauncher.com/downloads) and [Prism Launcher](https://prismlauncher.org/download/windows/) - there's probably others that work, but the following instructions are for those two.

1. Create a new instance
2. Set the Minecraft version to `1.21.1`
3. Set `NeoForge` as the mod loader, and select version `21.1.172`
4. Add the following pre-launch command to install the latest version of this pack each launch (see below for specific installtion)

`"$INST_JAVA" -jar packwiz-installer-bootstrap.jar https://fuzzymelon94.github.io/FuzzCraft-3/pack.toml`

### ATLauncher

1. Click "Settings"
2. Go to the "Commands" tab
3. Set "Enable commands?" to "Yes"
4. Add the above command to "Pre-launch command"
5. Click "Save"

### Prism Launcher

1. Right-click on the instance, then "Edit"
2. Go to "Settings"
3. Open the "Custom commands" tab
4. Tick "Custom Commands"
5. Add the above command to "Pre-launch command"
6. Click "Close"

## Setting up development

Using `packwiz` to get this set up and versioned nicely.

1. Clone this repo
2. Make sure `packwiz` is [installed](https://packwiz.infra.link/installation/) and running properly
3. Use `packwiz serve` to get a local "downloadable" for ATLauncher ([command on instance](https://packwiz.infra.link/tutorials/installing/packwiz-installer/))
   - Note: can use `-s server` to download "non-client" mods
4. Use `packwiz [mr|cf] add [URL|name]` to install mods
   - `mr` sources from Modrinth
   - `cf` sources from CurseForge
   - `URL` takes a direct link to the mod page
   - `name` searches the site for the mod name - returns options if required
