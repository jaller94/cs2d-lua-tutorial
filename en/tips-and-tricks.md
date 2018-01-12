## Tips and tricks

### Removing info boxes when joining
Whenever joining a server the server info and map briefing gets displayed. To fasten the testing process those messages should be removed.

Delete the file `sys/serverinfo.txt` to remove the server info.

Delete all text files in the folder `maps` to remove the map briefings.

Deleting all infos:
```bash
rm sys/serverinfo.txt
rm maps/*.txt
```

#### Deactivate / Activate the info boxes
If you wish to temporarily remove the messages, rename the files.

Deactivate info boxes:
```bash
mv sys/serverinfo.txt sys/serverinfo.inactive.txt
mkdir maps/briefings
mv maps/*.txt maps/briefings
```

Re-activate info boxes:
```bash
mv sys/serverinfo.inactive.txt sys/serverinfo.txt
mv maps/*.txt maps/briefings
rmdir maps/briefings
```

### Validate Lua Skripts
To detect syntax errors before starting the server, use the official lua compiler.

If you are using Atom, install the package `linter-lua`. You can do this in the settings or by running `apm install linter-lua`.
