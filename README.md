# **Plugin Permissions**

> A repository holding plugin permissions for [Ultra Permissions][uperms].

- [Discord][discord]
- [Spigot][spigot]
- [Contributors][contributors]

---

## **Overview**

[Ultra Permissions][uperms] simplifies searching for permissions by suggesting them based on installed plugins. The permission suggestions will be retrieved from [this file][permissions].

After that, it will try to extract missing permission nodes from the plugin JARs.

That means that the database will always have priority.

If you can't find suggestions for your installed plugins, that means this specific plugin is not included in our database yet and [Ultra Permissions][uperms] was not able to extract the nodes automatically.

In that case, you can contribute new permissions here.


## **Contribute permissions**

Contributing permissions is a tedious process but is highly appreciated to complete the database!

### **Instructions**
- pick a plugin that hasn't been added yet or one that needs updates
- add all its permissions line by line
  - make sure to keep the format which is shown below
  - for easier editing use the tool shown below
- create a [pull request]
  - provide a link to the plugin page
  - provide a link to the plugin permissions
  - only add one plugin per pull request
  - when adding permissions for a premium plugin, please provide the plugin.yml
    - the plugin.yml can be found inside the plugin JAR
    - use WinZip or other programs to open it
    - **DON'T** SHARE THE WHOLE JAR OF A PREMIUM PLUGIN

### **Formatting**
Permissions:<br>
``Plugin + Permission + Description + / optional Command``

Permission commands:<br>
``/ Command <required argument> [optional argument]``

### **Examples**
Permission without a command:<br>
``Essentials+essentials.fly+Allows the player to fly.``

Permission with a command:<br>
``Essentials+essentials.fly+Allows the player to fly.+/fly``

Permission with multiple commands:<br>
``Essentials+essentials.fly+Allows the player to fly.+/fly,/playerfly``

Permission with a placeholder:<br>
``Essentials+essentials.fly.[world]+Allows the player to fly in a specific world.``

Permission with command and required argument:<br>
``Essentials+essentials.fly+Give someone fly mode.+/fly <player>``

Permission with command and required argument to choose:<br>
``Essentials+essentials.fly+Give someone fly mode.+/fly <player|mob>``

Permission with command, required and optional argument:<br>
``Essentials+essentials.fly+Give someone fly mode.+/fly <player> [world]``

### **Editing Tool**
If you are using [Visual Studio Code][vscode] as your editor, you can now use an extension that
provides syntax highlighting for the [permission database][permissions].

You can get it [here][extension].

---

<!-- Links -->
[uperms]: https://www.spigotmc.org/resources/ultra-permissions.42678/
[discord]: https://discord.gg/3JuHDm8
[spigot]: https://www.spigotmc.org/resources/authors/techscode.29620/
[contributors]: CONTRIBUTORS.md
[pull request]: https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests
[permissions]: https://github.com/TechsCode-Team/PluginPermissions/blob/master/Permissions/Database.updb
[vscode]: https://code.visualstudio.com/
[extension]: https://marketplace.visualstudio.com/items?itemName=RLNT.uperms-db-syntax
