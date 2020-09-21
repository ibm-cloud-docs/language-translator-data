---

copyright:
  years: 2019, 2020
lastupdated: "2020-09-20"

keywords: identify language,identifiable languages

subcollection: language-translator-data

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:deprecated: .deprecated}
{:important: .important}
{:note: .note}
{:tip: .tip}
{:preview: .preview}
{:beta: .beta}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}

# Identifiable languages
{: #identifiable-languages}

The following languages can be identified by the service with the **Identify language** API method.

You can also use the **List identifiable languages** method to get the identifiable languages programmatically:

```sh
curl -X GET \
--header "Authorization: Bearer {token}" \
"{url}/v3/identifiable_languages?version=2018-05-01"
```
{: pre}

| Name                                 | Language code | Name                                 | Language code |
|--------------------------------------|---------------|--------------------------------------|---------------|
| Afrikaans                            | `af`          | Kirghiz                              | `ky`          |
| Albanian                             | `sq`          | Korean                               | `ko`          |
| Arabic                               | `ar`          | Kurdish                              | `ku`          |
| Armenian                             | `hy`          | Lao                                  | `lo`          |
| Azerbaijani                          | `az`          | Latvian                              | `lv`          |
| Bashkir                              | `ba`          | Lithuanian                           | `lt`          |
| Basque                               | `eu`          | Malay                                | `ms`          |
| Belarusian                           | `be`          | Malayalam                            | `ml`          |
| Bengali                              | `bn`          | Maltese                              | `mt`          |
| Bulgarian                            | `bg`          | Marathi                              | `mr`          |
| Burmese                              | `my`          | Mongolian                            | `mn`          |
| Catalan                              | `ca`          | Nepali                               | `ne`          |
| Central Khmer                        | `km`          | Norwegian Bokmal                     | `nb`          |
| Chinese (Simplified)                 | `zh`          | Norwegian Nynorsk                    | `nn`          |
| Chinese (Traditional)                | `zh-TW`       | Punjabi                              | `pa`          |
| Chuvash                              | `cv`          | Punjabi<br/>(Shahmukhi script, Pakistan) | `pa-PK`       |
| Croatian                             | `hr`          | Persian                              | `fa`          |
| Czech                                | `cs`          | Polish                               | `pl`          |
| Danish                               | `da`          | Portuguese                           | `pt`          |
| Dutch                                | `nl`          | Pushto                               | `ps`          |
| English                              | `en`          | Romanian                             | `ro`          |
| Esperanto                            | `eo`          | Russian                              | `ru`          |
| Estonian                             | `et`          | Serbian                              | `sr`          |
| Finnish                              | `fi`          | Sinhala                              | `si`          |
| French                               | `fr`          | Slovakian                            | `sk`          |
| Georgian                             | `ka`          | Slovenian                            | `sl`          |
| German                               | `de`          | Somali                               | `so`          |
| Greek                                | `el`          | Spanish                              | `es`          |
| Gujarati                             | `gu`          | Swedish                              | `sv`          |
| Haitian                              | `ht`          | Tagalog                              | `tl`          |
| Hebrew                               | `he`          | Tamil                                | `ta`          |
| Hindi                                | `hi`          | Telugu                               | `te`          |
| Hungarian                            | `hu`          | Thai                                 | `th`          |
| Icelandic                            | `is`          | Turkish                              | `tr`          |
| Irish                                | `ga`          | Ukrainian                            | `uk`          |
| Italian                              | `it`          | Urdu                                 | `ur`          |
| Japanese                             | `ja`          | Vietnamese                           | `vi`          |
| Kazakh                               | `kk`          | &nbsp; | &nbsp; |
{: caption="Table 1. Identifiable languages"}
