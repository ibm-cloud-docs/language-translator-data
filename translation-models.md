---

copyright:
  years: 2015, 2020
lastupdated: "2020-10-30"

keywords: installed languages,language paks,direct translations,pivot language

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

# Supported languages for translation
{: #translation-models}

With {{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}}, source and target languages are installed and enabled. {{site.data.keyword.languagetranslatorshort}} can translate between those source and target languages either directly or through English when no direct model is available.
{: shortdesc}

For example, if the German to English translation model is enabled (`de-en`), you can translate by specifying the source and target languages. Likewise, if the English to Korean translation model is also enabled (`en-ko`), you can also translate from German to Korean. Although no direct model exists between German and Korean, you can specify the source language (`de`) and target language (`ko`). {{site.data.keyword.languagetranslatorshort}} first translates from German to English, and then translates from English to Korean.

To find out which languages are installed and which models are enabled, ask an administrator. You can also use the [List models](https://{DomainName}/apidocs/language-translator-data#listmodels){: external} method to identify the enabled translation models.

## Listing supported languages for translation
{: #list-languages}

You can use the [List supported languages](https://{DomainName}/apidocs/language-translator#listlanguages){: external} method to retrieve the list of supported languages for translation. The following example calls the method:

```sh
curl -X GET \
--header "Authorization: Bearer {token}" \
"{url}/v3/languages?version=2018-05-01"
```
{: pre}

The method returns a complete list of all supported languages, sorted by `language` code (for example, `af`, `ar`). In addition to basic information about each language, the response indicates whether the language is `supported_as_source` for translation and `supported_as_target` for translation. It also lists whether the language is `identifiable`.

```json
"languages": [
  {
    "language": "af",
    "language_name": "Afrikaans",
    "native_language_name": "Afrikaans",
    "country_code": "ZA",
    "words_separated": true,
    "direction": "left_to_right",
    "supported_as_source": false,
    "supported_as_target": false,
    "identifiable": true
  },
  {
    "language": "ar",
    "language_name": "Arabic",
    "native_language_name": "العربية",
    "country_code": "AR",
    "words_separated": true,
    "direction": "right_to_left",
    "supported_as_source": true,
    "supported_as_target": true,
    "identifiable": true
  },
  . . .
]
```
{: codeblock}

The list of support languages can be long, reporting more than 75 languages.

## List of supported languages
{: #list-languages-supported}

The following table list the translatable languages. The service can translate from the following languages to any other language in the list (with the exception of Basque and Catalan).

| Language              | Language code | Language              | Language code |
|-----------------------|---------------|-----------------------|---------------|
| Arabic                | `ar`          | Korean                | `ko`          |
| Basque **[1]**        | `eu`          | Latvian               | `lv`          |
| Bengali               | `bn`          | Lithuanian            | `li`          |
| Bosnian               | `bs`          | Malay                 | `ms`          |
| Bulgarian             | `bg`          | Malayalam             | `ml`          |
| Catalan **[1]**       | `ca`          | Maltese               | `mt`          |
| Chinese (Simplified)  | `zh`          | Nepali                | `ne`          |
| Chinese (Traditional) | `zh-TW`       | Montenegrin           | `cnr`         |
| Croatian              | `hr`          | Norwegian Bokmål      | `nb`          |
| Czech                 | `cs`          | Polish                | `pl`          |
| Danish                | `da`          | Portuguese            | `pt`          |
| Dutch                 | `nl`          | Romanian              | `ro`          |
| English               | `en`          | Russian               | `ru`          |
| Estonian              | `et`          | Serbian **[2]**       | `sr`          |
| Finnish               | `fi`          | Sinhala               | `si`          |
| French                | `fr`          | Slovak                | `sk`          |
| French (Canadian)     | `fr-CA`       | Slovenian             | `sl`          |
| German                | `de`          | Spanish               | `es`          |
| Greek                 | `el`          | Swedish               | `sv`          |
| Gujarati              | `gu`          | Tamil                 | `ta`          |
| Hebrew                | `he`          | Telugu                | `te`          |
| Hindi                 | `hi`          | Thai                  | `th`          |
| Hungarian             | `hu`          | Turkish               | `tr`          |
| Irish                 | `ga`          | Ukrainian             | `uk`          |
| Indonesian            | `id`          | Urdu                  | `ur`          |
| Italian               | `it`          | Vietnamese            | `vi`          |
| Japanese              | `ja`          | Welsh                 | `cy`          |
{: caption="Table 1. Translatable languages"}

Notes:

1.  Basque and Catalan are supported only for translation to and from Spanish.
3.  Serbian translation support is based on the Cyrillic alphabet. (Bosnian, Croatian, and Montenegrin translation support is based on the Latin alphabet.)
