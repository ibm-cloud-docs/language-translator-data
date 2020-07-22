---

copyright:
  years: 2015, 2020
lastupdated: "2020-07-22"

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

For example, if the German to English translation model is enabled (`de-en`), you can translate by specifying the source and target languages. Likewise, if the English to Korean translation model is also enabled (`en-ko`), you can also translate from German to Korean. Although no direct model exists between German and Korean, you can specify the source language (`de`) and target language (`ko`). {{site.data.keyword.languagetranslatorshort}} first translates from German to English, and then translates from English to Korean.

To find out which languages are installed and which models are enabled, ask an administrator. You can also use the [List models](https://cloud.ibm.com/apidocs/language-translator-data#list-models){: external} API method to identify the enabled translation models.

{{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} can translate the following languages.

| Language              | Language code |
|-----------------------|---------------|
| Arabic                | `ar`          |
| Bengali               | `bn`          |
| Bulgarian             | `bg`          |
| Catalan\*             | `ca`          |
| Chinese (Simplified)  | `zh`          |
| Chinese (Traditional) | `zh-TW`       |
| Croatian              | `hr`          |
| Czech                 | `cs`          |
| Danish                | `da`          |
| Dutch                 | `nl`          |
| English               | `en`          |
| Estonian              | `et`          |
| Finnish               | `fi`          |
| French                | `fr`          |
| German                | `de`          |
| Greek                 | `el`          |
| Gujarati              | `gu`          |
| Hebrew                | `he`          |
| Hindi                 | `hi`          |
| Hungarian             | `hu`          |
| Irish                 | `ga`          |
| Indonesian            | `id`          |
| Italian               | `it`          |
| Japanese              | `ja`          |
| Korean                | `ko`          |
| Latvian               | `lv`          |
| Lithuanian            | `li`          |
| Malay                 | `ms`          |
| Malayalam             | `ml`          |
| Maltese               | `mt`          |
| Nepali                | `ne`          |
| Norwegian Bokmål      | `nb`          |
| Polish                | `pl`          |
| Portuguese            | `pt`          |
| Romanian              | `ro`          |
| Russian               | `ru`          |
| Sinhala               | `si`          |
| Slovak                | `sk`          |
| Slovenian             | `sl`          |
| Spanish               | `es`          |
| Swedish               | `sv`          |
| Tamil                 | `ta`          |
| Telugu                | `te`          |
| Thai                  | `th`          |
| Turkish               | `tr`          |
| Urdu                  | `ur`          |
| Vietnamese            | `vi`          |
