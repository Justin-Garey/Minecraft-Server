# Minecraft Server
An easy way to launch a Minecraft Server. Made specifically for a Raspberry Pi but also tested on Ubuntu.

## Usage
Start by giving execution permissions to the setup and launch scripts
```
chmod +x ./setup ./launch
```

Then run the setup script
```
./setup
```
- Run with -h to see options

The setup script will make sure everything needed is installed, add optimizations, and pre-enter the eula.

After setup is complete, just launch the server!
```
./launch
```
- The launch script is set to use 7G of RAM, change this as you please.

## Other useful tools

### Screen
If you have the server running and you would like to ssh into the machine to see the logs or run commands, I recommend using screen. It allows you to run a task and put it in the background by detaching from it. You can later re-attach to interact again.

To install
```
sudo apt install screen
```

To use
```
screen
```

Once the server is running; detach with ctrl+a, d.

When you want to re-attach, use
```
screen -r
```
- If you have multiple instances of screen you will need to specify the id to re-attach

### World Pregeneration
When running on a smaller server such as a Raspberry Pi, lag can be a big issue. World pregeneration can help stop some lag spikes, especially in the early game. Try this [plugin](https://www.spigotmc.org/resources/fast-chunk-pregenerator.74429/) or if you know a better one, feel free to recommend it.

## Future Enhancements
- Get the correct version of Java for the Minecraft version.
- Check if the passed version to use exists in the info file.
- Add vanilla, bukkit, spigot, purple, and pufferfish servers availability in setup script.
- Modded Minecraft server setup.