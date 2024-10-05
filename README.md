# Stellaris Avali Commons Library

![Steam Views][badge-steam-views]
![Steam Downloads][badge-steam-downloads]
![Steam Subscriptions][badge-steam-subscriptions]
![Steam Addon Size][badge-steam-filesize]
![License][badge-license]

_Across the stars. Together in feather and ice._

This is a utility mod for Stellaris mods that adds common bases for the Avali species, such as
- Graphical cultures
- Name lists
- Portrait categories
- Species classes
- Species names
- Localizations

## Contributing
See something amiss? Pull Requests and issues are welcome.  

## Usage

[![Download][badge-download]][steam-workshop-url]

### For Players

This is a utility mod, so in most cases you should only install this if another mod depends on it.  
However, this mod still adds name lists and a few other things that could be useful to make custom empires or have in a game, so it wouldn't hurt to use.

The latest version of this mod can be found on the [Steam Workshop][steam-workshop-url].  
If you require an earlier version, check the [git tags][github-tags] page or the [Releases][github-releases] page.  
To then download, simply click the `Source code (zip)` or `Source code (tar.gz)` links on the page of the version you want.

You can either do a full manual install if you know how or use the included `manual-mod-install.cmd` script, simply double click it, it will create a link to this directory and a copy of the .mod file to the Stellaris mods directory.

### For Modders

**FIRST AND FOREMOST: Make sure to name your files uniquely!  
Do not reuse filenames unless you know what you are doing, especially not from third party mods, else you may break things!**  
This also applies for keys or definition names in the files themselves.  
An easy way to do so is by using a personal prefix that is unique to you and your mod.  

Please note that some library-specific definitions in this mod simply use `AVALI`. This is intentional.  
If your mod uses this prefix, please either change it or raise an issue about name collision and the reasoning.  

_The goal here is to unify the inter-mod definitions and compatibility for the feathery critters and make things easier for everyone._  

### MOD PREFIX: `avali-commons_`

Examples:
- `avali-commons_avali`
- `avali-commons_l_english.yml`

### Cheat Sheet For Definitions

| Type | Definition | Description |
|------|------------|-------------|
| Graphical Culture | `avalian_01` | Controls ship color and lighting, as well as city backgrounds |
| Name Lists | `AVALI1` | Namelists for ships, fleets, armies, planets and characters |
| Portrait Categories | `avalian` |  |
| Species Classes | `AVALI` | |
| Species Names | `AVALI` | Definition for compound of Name, Plural, Adjective, Homeplanet, Homesystem and Namelist |

### I want to add a new portrait! How?

1. Make sure to create one or more new portrait set(s), depending on your needs.
2. Add or copy the portrait category from this mod to your own, and add your own portraits under the `sets` key.
	
	Example:
	<!-- It aint TOML but the highlighting works.. even if its borderline useless -->
	```toml
	avalian = {
		name = AVALI

		sets = {
			"YOUR PORTRAIT SET NAME HERE"
			"and any other you might have"
		}
	}
	```

## Localizations:

Language | Translated (estimate)
---|---:
Brazilian Portuguese | 0%
English | 95%
French | 0%
German | 0%
Japanese | 0%
Korean | 0%
Polish | 0%
Russian | 0%
Simplified Chinese | 0%
Spanish | 0%

## Credits

- [Major Missile][credit-url-major_missile] - compiled initial namelists for ASAE
- Avali race, lore and concept ©️ RyuujinZERO, licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License][license-cc-by-sa-4.0]

## License

Licensed under the MIT License.  

<!-- URL references -->

[badge-download]: https://img.shields.io/badge/Get%20it%20now-on%20Steam-blue.svg?style=for-the-badge&color=00aeef
[badge-license]: https://img.shields.io/github/license/atakiya/stellaris-avali-commons-library.svg?style=flat-square
[badge-steam-filesize]: https://img.shields.io/steam/size/3340739706.svg?label=addon%20size&style=flat-square
[badge-steam-subscriptions]: https://img.shields.io/steam/subscriptions/3340739706.svg?style=flat-square
[badge-steam-downloads]: https://img.shields.io/steam/downloads/3340739706.svg?style=flat-square
[badge-steam-views]: https://img.shields.io/steam/views/3340739706.svg?style=flat-square

[credit-url-major_missile]: https://steamcommunity.com/id/missilesandafterburners

[license-cc-by-nc-nd-4.0]: https://creativecommons.org/licenses/by-nc-nd/4.0/
[license-cc-by-sa-4.0]: https://creativecommons.org/licenses/by-sa/4.0/

[github-releases]: https://github.com/atakiya/stellaris-avali-commons-library/releases
[github-tags]: https://github.com/atakiya/stellaris-avali-commons-library/tags

[steam-workshop-url]: https://steamcommunity.com/sharedfiles/filedetails/?id=3340739706
