---

copyright:
  years: 2015, 2020
lastupdated: "2020-09-20"

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

To find out which languages are installed and which models are enabled, ask an administrator. You can also use the [List models](https://{DomainName}/apidocs/language-translator-data#listmodels){: external} method to identify the enabled translation models.

{{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} can translate the following languages.

| Language              | Language code | Language              | Language code |
|-----------------------|---------------|-----------------------|---------------|
| Arabic                | `ar`          | Korean                | `ko`          |
| Bengali               | `bn`          | Latvian               | `lv`          |
| Bulgarian             | `bg`          | Lithuanian            | `li`          |
| Catalan **[1]**       | `ca`          | Malay                 | `ms`          |
| Chinese (Simplified)  | `zh`          | Malayalam             | `ml`          |
| Chinese (Traditional) | `zh-TW`       | Maltese               | `mt`          |
| Croatian              | `hr`          | Nepali                | `ne`          |
| Czech                 | `cs`          | Norwegian Bokmål      | `nb`          |
| Danish                | `da`          | Polish                | `pl`          |
| Dutch                 | `nl`          | Portuguese            | `pt`          |
| English               | `en`          | Romanian              | `ro`          |
| Estonian              | `et`          | Russian               | `ru`          |
| Finnish               | `fi`          | Sinhala               | `si`          |
| French                | `fr`          | Slovak                | `sk`          |
| German                | `de`          | Slovenian             | `sl`          |
| Greek                 | `el`          | Spanish               | `es`          |
| Gujarati              | `gu`          | Swedish               | `sv`          |
| Hebrew                | `he`          | Tamil                 | `ta`          |
| Hindi                 | `hi`          | Telugu                | `te`          |
| Hungarian             | `hu`          | Thai                  | `th`          |
| Irish                 | `ga`          | Turkish               | `tr`          |
| Indonesian            | `id`          | Urdu                  | `ur`          |
| Italian               | `it`          | Vietnamese            | `vi`          |
| Japanese              | `ja`          | &nbsp; | &nbsp; |
{: caption="Table 1. Translatable languages"}

Notes:

1.  Catalan is supported only for translation to and from Spanish.
