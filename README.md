<p align="center">
  <img src="assets/logo.svg" alt="Pak-Plaza" width="460">
</p>

<p align="center"><b>A store of paks for NextUI handhelds, with one shelf per device.</b></p>

<p align="center">
  <a href="https://retrotiv.github.io/Pak-Plaza/">Open the store</a> ·
  <a href="CREDITS.md">Credits</a>
</p>

<p align="center">
  <a href="https://ko-fi.com/retrotiv"><img src="https://img.shields.io/badge/%E2%98%95%20Support%20on-Ko--fi-ff5e5b?logo=ko-fi&logoColor=white" alt="Support retrotiv on Ko-fi"></a>
</p>

## What this is

Pak-Plaza gathers the paks (the little apps and tools that extend NextUI) into one place and
sorts them by device, laid out like a small eShop. You pick your handheld, then browse two
shelves: the community paks from the **Pak Store**, and the **exclusives** made for
Pak-Plaza that you will not find anywhere else.

It opens dark with an amber accent. There is a light theme in the preferences if you prefer
it, and it remembers your choice on that device.

## Two shelves

* **Pak Store.** The community paks from the NextUI Pak Store, built for your device. On the
  RG353V these are the versions adapted here (part of the
  [AnberNext](https://github.com/retrotiv/AnberNext) project); on the TrimUI Brick they are
  the upstream builds. Every card names the original author and links to the source.
* **Exclusives.** Paks made for Pak-Plaza, like the AnberNext over-the-air updater. These are
  ours and live only here.

## Devices

The store starts with the **Anbernic RG353V** and the **TrimUI Brick**, with room for more.
Switching device at the top shows only what runs on it.

## How the catalog works

The storefront is a single page on GitHub Pages that reads [`paks.json`](paks.json). To add
or change a pak you edit that file, no code involved:

```jsonc
{
  "name": "Game Manager",
  "store": "pakstore",
  "category": "Scrapers",
  "desc": "Rename, archive and delete ROMs, and download box art.",
  "author": "UncleJunVIP",
  "source": "https://github.com/UncleJunVIP/nextui-game-manager",
  "availability": { "rg353v": "adapted", "brick": "original" }
}
```

`store` is `pakstore` or `alternative`. `availability` maps a device id to `adapted` (a build
made here) or `original` (the upstream build). Add a device to the `devices` list and it shows
up as a switch on its own.

## Credit where it is due

These paks are the community's work. Pak-Plaza is a shelf, not an author. Every card credits
the person or project that made the pak and links to its home. If you made one of these and
want it added, linked differently, or taken down, open an issue and it gets handled. See
[CREDITS.md](CREDITS.md).
