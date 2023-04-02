---
id: garrys-mod
title: 🔫 Garry's Mod
---

Cosmo supports Garry's Mod for the automated store. You can use it by installing the official Garry's Mod addon for Cosmo.

## Installing the integration
* [Download the integration](https://github.com/tbdscripts/cosmo-gmod/archive/refs/heads/master.zip)
* Extract the .zip file
* Place the addon folder in your server's `addons` folder
* Head into `lua/cosmo` and edit the `sh_config.lua` file
* Update `Cosmo.Config.InstanceUrl` to match your website's domain
* Close `sh_config.lua` and open `sv_config.lua`
* Update `Cosmo.Config.ServerToken` to match your server token
* Once you have done this we reccomend installing a HTTP module. You can follow the guide [**here**](#installing-a-http-module) for help

:::info
Your server token can be found in the **Management Panel** under **Components -> Server**.
Click on the **Edit** button of the corresponding server and click **Regenerate Token**
:::
* Update any other configuration values if you wish
* Restart your server

## Installing a HTTP module
It is reccomended to use a HTTP module such as CHTTP or Reqwest when using Cosmo.

:::info
If your server host does not allow uploading custom modules check if it in their mod manager. If not contact them for help.
:::
* Download one of the modules from below, We reccomend using Reqwest.
    * **Reqwest**: [Download](https://github.com/WilliamVenner/gmsv_reqwest/releases/tag/v3.0.2)
    * **CHTTP**: [Download](https://github.com/timschumi/gmod-chttp/releases/tag/v1.8.1)
* Place the downloaded module into the `garrysmod/lua/bin` folder on your server. If the `bin` folder does not exist, create it.


If you are unsure what file to download, run this in your server console:
```
lua_run print((system.IsWindows()and"Windows"or system.IsLinux()and"Linux"or"Unsupported").." "..(jit.arch=="x64"and"x86-64"or"x86"))
```




## Supported Action Types
* Console Command
* Usergroup
* Custom Lua
* DarkRP Money
* DarkRP Levels
* (Permanent) Weapons
* Pointshop 1 points
* Pointshop 2 standard and premium points

## Turning on debug mode
If staff requested you to turn on debug mode for support, please follow these steps.

* Go into `lua/cosmo` and edit the `sh_config.lua` file
* Change `Cosmo.Config.LogLevel` to `Cosmo.Config.LogLevel = Cosmo.Log.LEVEL_DEBUG`
* Restart your server
