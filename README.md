A custom modpack created for me and my friends, with some mods to keep everyone interested!

## Themes for the pack

- Automation
- Magic
- Technology

## Playing the pack

Easiest way to install this pack is to use the packwiz bootloader. I've tested this setup using
both [ATLauncher](https://atlauncher.com/downloads) and [Prism Launcher](https://prismlauncher.org/download/windows/) - there's probably others that work, but the following instructions are for those two.

1. Create a new instance
2. Set the Minecraft version to `1.21.1`
3. Set `NeoForge` as the mod loader, and select version `21.1.172`
4. Setup pre-launch commands to grab the latest version of this pack (see below)

### ATLauncher

1. Click "Settings"
2. Go to the "Commands" tab
3. Set "Enable commands?" to "Yes"
4. Add the following command to "Pre-launch command"
   `"$INST_JAVA" -jar packwiz-installer-bootstrap.jar https://fuzzymelon94.github.io/FuzzCraft-3/pack.toml`
5. Click "Save"

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
