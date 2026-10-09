# countries

`countries.json` is a list of 250 countries and territories with their native name, flag emoji, country code, dial code and continent.

This is the file I use on my own projects, including [LetterMe](https://letterme.app) and [Sedcst](https://sedcst.com). The list has some political bias, so feel free to update it to match your own views. See [Coverage](#coverage) and [Naming](#naming) for which territories are and aren't included and how they're named.

| Field          | Example   | Description                  |
| -------------- | --------- | ---------------------------- |
| `name`         | `"Spain"` | Common English name          |
| `native_name`  | `"España"` | Name in the main local language |
| `flag`         | `"🇪🇸"`    | Flag emoji                   |
| `country_code` | `"ES"`    | ISO 3166-1 alpha-2 code      |
| `dial_code`    | `"+34"`   | International dialing prefix |
| `continent`    | `"EU"`    | Continent code (see below)   |

## Continent codes

| Code | Continent     |
| ---- | ------------- |
| `AF` | Africa        |
| `AN` | Antarctica    |
| `AS` | Asia          |
| `EU` | Europe        |
| `NA` | North America |
| `OC` | Oceania       |
| `SA` | South America |

Continent assignments follow [GeoNames](https://www.geonames.org/countries/).

## Coverage

The list contains every ISO 3166-1 entry (249) plus Kosovo.

### Disputed territories

These are included as separate entries:

| Name                        | Code | Note                                                        |
| --------------------------- | ---- | ----------------------------------------------------------- |
| Kosovo                      | `XK` | Not in ISO 3166-1; `XK` is a widely used user-assigned code |
| Palestine                   | `PS` |                                                             |
| Taiwan                      | `TW` |                                                             |
| Western Sahara              | `EH` |                                                             |
| Falkland Islands (Malvinas) | `FK` | Both names are given                                        |

Not listed separately: Northern Cyprus, Abkhazia, South Ossetia, Transnistria, Somaliland.

### China, Hong Kong, Macao and Taiwan

Hong Kong (`HK`), Macao (`MO`) and Taiwan (`TW`) are separate entries, each with its own dial code. `China` (`CN`) means mainland China only.

## Naming

Names are the common English short names, not official long names:

- `St.` for "Saint": `St. Lucia`, `St. Kitts & Nevis`
- `&` instead of "and": `Antigua & Barbuda`, `Bosnia & Herzegovina`
- The two Congos are named by capital: `Congo - Brazzaville` (`CG`), `Congo - Kinshasa` (`CD`)
- New names: `Czechia` (formerly Czech Republic), `Eswatini` (formerly Swaziland), `North Macedonia` (formerly Macedonia), `Myanmar` (formerly Burma), `Naoero` (formerly Nauru)
- Official names, not English translations: `Türkiye`, `Cabo Verde`, `Côte d'Ivoire`

Some entries use a different name from their ISO name:

| Name used             | ISO name                             | Code |
| --------------------- | ------------------------------------ | ---- |
| Chagos Archipelago    | British Indian Ocean Territory       | `IO` |
| Caribbean Netherlands | Bonaire, Sint Eustatius and Saba     | `BQ` |
| Vatican City          | Holy See                             | `VA` |
| Pitcairn Islands      | Pitcairn                             | `PN` |
| Micronesia            | Micronesia, Federated States of      | `FM` |
| US Outlying Islands   | United States Minor Outlying Islands | `UM` |

`native_name` is the country's name in its official or most widely spoken language, based on [Unicode CLDR](https://cldr.unicode.org). Countries with several official languages have just one native name, e.g. `België` for Belgium and `Schweiz` for Switzerland.

## Dial codes

Places that share the `+1` dial code with the US and Canada have their area code added to `dial_code`, e.g. `+1684` for American Samoa and `+1876` for Jamaica. Places with more than one area code list only one: the Dominican Republic is `+1849` (it also uses 809 and 829), Puerto Rico is `+1939` (also 787) and Jamaica is `+1876` (also 658).
