---
permalink: /user-guide
title: User Guide
---

## Installation

### Step 1: Download tera-proxy

The most convenient way for most users will be to download the latest ZIP from the [releases](https://github.com/tera-proxy/tera-proxy/releases) page. Go ahead and extract it anywhere that's convenient for you.

### Step 2: Download modules

tera-proxy does very little on its own. If you want something done, find (or [make]({{ '/developer-guide' | absolute_url }})!) a module for it.

Let's say you'd like to install [auto-vanguard](https://github.com/tera-mods/auto-vanguard) so you never forget to turn in a Vanguard quest ever again.

First, go to its [GitHub page](https://github.com/tera-mods/auto-vanguard). Near the top, it'll list the number of commits, branches, and releases. Click on [releases](https://github.com/tera-mods/auto-vanguard/releases) if there are any, and you can get download the prepackaged module from there.

However, auto-vanguard has no prepackaged releases, so instead you can click the green "Clone or download" button and click on "Download ZIP". Extract it anywhere convenient and you should have a folder called `auto-vanguard-master` with one file in it.

Over in your tera-proxy installation, go to: `tera-proxy/bin/node_modules/` and then put the folder in there. You’re done!

For the vast majority of modules, you *should* have a file in at least one of the following places:

- `tera-proxy/bin/node_modules/<module_name>/index.js` (most common)
- `tera-proxy/bin/node_modules/<module_name>/package.json`

If neither of those exist, you might have an extra folder. Try moving things up a folder until you have one of the files above.

**If you have an existing installation of tera-proxy,** you can simply copy over your old `tera-proxy/bin/node_modules`.

### Step 3: Run tera-proxy

In the provided tera-proxy download, there should be a file called `TeraProxy.bat`. Right-click it, select "Run as administrator", and you're set.

If you got tera-proxy from somewhere else and there is no `TeraProxy.bat`, follow whatever instructions you were given. If you didn't get instructions or forgot them, you're on your own.

### Step 4: Connect to tera-proxy

tera-proxy modifies the server list to allow you to connect to it.

If TERA is already open, you'll need to at least go back to the server select screen *after launching tera-proxy*.

If TERA is already closed when you launch tera-proxy, you're all set! Just start up the game and it should work fine.

### Step 5: Enjoy!

You're done! Go have fun with your fancy new modules.

## FAQ

#### There was a TERA patch and the proxy broke!

Unfortunately, you'll need to update tera-proxy every major patch. Check the [tera-proxy releases page](https://github.com/tera-proxy/tera-proxy/releases) to see if there's a new version. If you're in a region like KR, you may have to wait a day or so.

#### What's with this timeout error?

By default, tera-proxy attempts to proxy to the region set in the `tera-proxy/bin/config.json`. if you don't have that file, then you should run `server-select.exe` & pick your region, if you do then lets say for exmaple your region is JP, you have to go and edit the file at `tera-proxy/bin/config.json` and it should something like:

```json
{
	"region": "JP"
}```

You don't have to change any other values in there, just the region.
You can change the region to one of: EU, JP, KR, NA, RU, TW, TH.

