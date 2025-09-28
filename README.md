A custom modpack created for me and my friends, with some mods to keep everyone interested!

## Themes for the pack

- Automation
- Magic
- Technology

## Playing the pack

This pack is put together using [packwiz](https://packwiz.infra.link),so we'll use their bootstrap to automatically install the latest version of the pack before each launch.

I've tested this setup using
both [ATLauncher](https://atlauncher.com/downloads) and [Prism Launcher](https://prismlauncher.org/download/windows/) - there's probably others that work (e.g. MultiMC), but the following instructions are for the two I know.

### Pre-requisites

- Download a launcher that supports pre-launch commands
- Download the latest version of [`packwiz-installer-bootstrap.jar`](https://github.com/packwiz/packwiz-installer-bootstrap/releases)
- At least 8GB of RAM - don't forget to adjust the instance in your launcher

### ATLauncher

1. Click "Create Pack"
2. Add in a name and description as you like
3. Set "Minecraft Version" to `1.21.1`
4. Set "Loader?" to `NeoForge`
5. Set "Loader Version" to `21.1.209`
6. Click "Create Instance" and let it build
7. Once complete, click "Instances"
8. Find your new instance, and click "Settings"
9. Go to the "Commands" tab
10. Set "Enable commands?" to "Yes"
11. Add the following command to "Pre-launch command"

`"$INST_JAVA" -jar packwiz-installer-bootstrap.jar https://fuzzymelon94.github.io/FuzzCraft-3/pack.toml`

12. Click "Save"
13. Click "Open Folder"
14. Make sure you're in the folder with `instance.json` file and the `mods` folder (among others)
15. Place your `packwiz-installer-bootstrap.jar` in here
16. Go back to ATLauncher and hit "Play"

### Prism Launcher

1. Click "Add Instance"
2. Add in a name and description as you like
3. Set "Minecraft Version" to `1.21.1`
4. Set "Loader?" to `NeoForge`
5. Set "Loader Version" to `21.1.209`
6. Click "OK"
7. Right-click on the instance, then "Edit"
8. Go to "Settings"
9. Open the "Custom commands" tab
10. Tick "Custom Commands"
11. Add the following command to "Pre-launch command"

`"$INST_JAVA" -jar packwiz-installer-bootstrap.jar https://fuzzymelon94.github.io/FuzzCraft-3/pack.toml`

12. Click "Close"
13. Right-click the instance, then "Folder"
14. Go into the "Minecraft" folder - you should see the `mods` folder
15. Place your `packwiz-installer-bootstrap.jar` in here
16. Go back to Prism and double click the instance to launch

## Setting up a server

- Using [`docker-minecraft-server`](https://docker-minecraft-server.readthedocs.io/en/latest/#using-docker-compose) to run a server.
- Using [`setupmc's configurator`](https://setupmc.com/java-server/) for the `compose.yml`
- Launch with `docker compose up -d`
- Run commands by first running `docker exec -i fuzzcraft3-mc-1 rcon-cli`
  - Note, `fuzzcraft3-mc-1` will likely be different, run `docker ps` to get the container name
- To restart the server, just run `docker compose up -d` again
- View the logs with `docker compose logs -f`

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
