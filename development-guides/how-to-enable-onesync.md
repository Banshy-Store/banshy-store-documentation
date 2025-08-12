# How to enable OneSync

OneSync is a feature in FiveM that allows for larger server capacities and improved synchronization of entities and players. Enabling OneSync is a straightforward process that requires a simple edit to your `server.cfg` file.

## Steps to enable OneSync

### 1) Open the `server.cfg` file
Navigate to your server's root directory and locate the `server.cfg` file. Open it with a text editor (for example, Notepad++ or Visual Studio Code).

### 2) Add the OneSync command
Add the following line to your `server.cfg` to enable OneSync:

```cfg
onesync on
```

This ensures OneSync is active for your server.

### Optional: enable Infinity mode
If your server needs support for more than 64 players (up to 1024), enable OneSync Infinity by adding this line:

```cfg
onesync_enableInfinity 1
```

Infinity mode is designed for large-scale servers and requires proper resource optimization.

### 3) Save and restart your server
Save the changes to the `server.cfg` file and restart your server to apply the OneSync settings.

## Media
- Video: [Placeholder – enabling OneSync and Infinity]
- Screenshots: [Placeholder – server.cfg lines and console verification]


