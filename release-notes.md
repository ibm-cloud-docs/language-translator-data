---

copyright:
  years: 2019, 2020
lastupdated: "2020-06-19"

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
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# Release notes
{: #release-notes}

The following new features and changes to the service are available.
{: shortdesc}

## Version 1.1.2 (19 June 2020)
{: #v112}

- **Expanded language support.**
    - Added [translation models](/docs/language-translator-data?topic=language-translator-data-translation-models) for English to and from the following languages:
        - Bengali (`en-bn` and `bn-en`)
        - Gujarati (`en-gu` and `gu-en`)
        - Malayalam (`en-ml` and `ml-en`)
        - Maltese (`en-mt` and `mt-en`)
        - Nepali (`en-ne` and `ne-en`)
        - Sinhala (`en-si` and `si-en`)
        - Tamil (`en-ta` and `ta-en`)
        - Telugu (`en-te` and `te-en`)
    - Improved results when translating to and from the following languages:
        - Catalan (`ca`)
        - Chinese (Simplified) (`zh`)
    - Improved translation quality for translation between English and Hindi.
- **Automatic language detection**
    - Added source language detection when you translate plain text or documents. If you specify a target language without a source language or translation model, the service attempts to identify the source language and continues with the translation. In the results, the service returns the identified language and a score that indicates the confidence in the identification.
- **Improved performance when translating documents**
    - Better performance for Word, PowerPoint, and Excel documents.

## Version 1.1.1 (February 2020)
{: #1.1.1}

Added the following [translation models](/docs/language-translator-data?topic=language-translator-data-translation-models):

- English to and from Latvian (`en-lv` and `lv-en`)
- English to and from Urdu (`en-ur` and `ur-en`)
- English to and from Vietnamese (`en-vi` and `vi-en`)

## Version 1.1.0 (November 2019)
{: #1.1.0}

{{site.data.keyword.languagetranslatorfull}} for {{site.data.keyword.icp4dfull_notm}} is now available.
