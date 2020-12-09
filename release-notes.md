---

copyright:
  years: 2019, 2020
lastupdated: "2020-12-04"

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

The following versions of {{site.data.keyword.languagetranslatorfull}} for {{site.data.keyword.icp4dfull}} have been released. The information includes new features and changes for each version of the product and any known limitations.
{: shortdesc}

## Version 1.2 (9 December 2020)
{: #v12}

{{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} version 1.2 is now available. Installation and administration of the service include many changes. This version supports {{site.data.keyword.icp4dfull_notm}} versions 3.5 and 3.0.1, and Red Hat OpenShift versions 4.5 and 3.11. For more information about installing and managing the service, see [Installing {{site.data.keyword.watson}} {{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.cpd_short}}](/docs/language-translator-data?topic=language-translator-data-install).

The release includes the following functional changes and enhancements:

-   The service now offers the [List supported languages](https://{DomainName}/apidocs/language-translator-data#listlanguages){: external} (`GET /v3/languages`) method to retrieve the list of supported languages for translation. The method returns a complete list of all supported languages, sorted by `language` code (for example, `af`, `ar`). In addition to basic information about each language, the response indicates whether the language is `supported_as_source` for translation and `supported_as_target` for translation. It also lists whether the language is `identifiable`. For more information, see [Listing supported languages for translation](/docs/language-translator-data?topic=language-translator-data-translation-models#list-languages).
-   The following translation models are now available.

    <table style="width:75%">
      <caption>Table 1. New translation models</caption>
      <tr>
        <th style="text-align:left">Translation models</th>
        <th style="text-align:center">Identifiable</th>
      </tr>
      <tr>
        <td>Basque to Spanish (`eu-es`)<br/>Spanish to Basque (`es-eu`)</td>
        <td style="vertical-align:top; text-align:center">`eu` is identifiable</td>
      </tr>
      <tr>
        <td>Bosnian to English (`bs-en`)<br/>English to Bosnian (`en-bs`)</td>
        <td style="vertical-align:top; text-align:center">`bs` is not identifiable **[1]**</td>
      </tr>
      <tr>
        <td>Canadian French to English (`fr-CA-en`)<br/>English to Canadian French (`en-fr-CA`)</td>
        <td style="vertical-align:top; text-align:center">`fr-CA` is not identifiable **[2]**</td>
      </tr>
      <tr>
        <td>Montenegrin to English (`cnr-en`)<br/>English to Montenegrin (`en-cnr`)</td>
        <td style="vertical-align:top; text-align:center">`cnr` is not identifiable **[1]**</td>
      </tr>
      <tr>
        <td>Serbian to English (`sr-en`)<br/>English to Serbian (`en-sr`)</td>
        <td style="vertical-align:top; text-align:center">`sr` is identifiable **[3]**</td>
      </tr>
      <tr>
        <td>Ukrainian to English (`uk-en`)<br/>English to Ukrainian (`en-uk`)</td>
        <td style="vertical-align:top; text-align:center">`uk` is identifiable</td>
      </tr>
      <tr>
        <td>Welsh to English (`cy-en`)<br/>English to Welsh (`en-cy`)</td>
        <td style="vertical-align:top; text-align:center">`cy` is identifiable</td>
      </tr>
    </table>

    The following notes apply to the languages listed in the table:

    1.  Bosnian, Croatian, and Montenegrin translation support is based on the Latin alphabet. Only Croatian is identifiable. Bosnian and Montenegrin are not identifiable because they cannot be reliably distinguished from Croatian.
    1.  French content is identifiable, but Canadian French is not because it cannot be reliably distinguished from French.
    1.  Serbian translation support is based on the Cyrillic alphabet. Serbian is identifiable because it can be readily distinguished from Bosnian, Croatian, and Montenegrin.

    For more information, see [List of supported languages](/docs/language-translator-data?topic=language-translator-data-translation-models#list-languages-supported).
-   Beta support is available for translation of the following subtitle (caption) document formats:
    -   SubRip: `.srt`
    -   SubViewer: `.sbv`
    -   DirectVobSub or VSFilter: `.sub`
    -   MicroDVD: `.sub`
    -   WebVTT: `.vtt`

    These textual formats contain the transcript of a sound track or video source. For more information about the formats and the characteristics of subtitle translation, see [Subtitle formats (Beta)](/docs/language-translator?topic=language-translator-document-translator-tutorial#supported-file-formats-subtitles).
-   The English to Spanish (`en-es`) and Spanish to English (`es-en`) translation models are improved.
-   The English to Korean (`en-ko`) and Korean to English (`ko-en`) translation models are improved. The models are intended to preserve markup in the translation if present in the source.
-   Table handling for Microsoft PowerPoint is improved for document translation.

## Version 1.1.2 (19 June 2020)
{: #v112}

-   The service now offers expanded language support.
    -   The following translation models are now available:
        -   Bengali (`en-bn` and `bn-en`)
        -   Gujarati (`en-gu` and `gu-en`)
        -   Malayalam (`en-ml` and `ml-en`)
        -   Maltese (`en-mt` and `mt-en`)
        -   Nepali (`en-ne` and `ne-en`)
        -   Sinhala (`en-si` and `si-en`)
        -   Tamil (`en-ta` and `ta-en`)
        -   Telugu (`en-te` and `te-en`)

        For more information, see [List of supported languages](/docs/language-translator-data?topic=language-translator-data-translation-models#list-languages-supported).
    -   The Catalan (`ca`) and Simplified Chinese (`zh`) translation models are improved.
    -   The English to Hindi (`en-hi`) and Hindi to English (`hi-en`) translation models are improved.
-   Automatic source language detection is available when you translate plain text or documents. If you specify a target language without a source language or a translation model, the service attempts to identify the source language and continue with the translation. In the results, the service returns the identified language and a score that indicates its confidence in the identification.
-   Performance is improved for translating Microsoft Word, PowerPoint, and Excel documents.

## Version 1.1.1 (February 2020)
{: #1.1.1}

The service now offers the following translation models:

-   English to and from Latvian (`en-lv` and `lv-en`)
-   English to and from Urdu (`en-ur` and `ur-en`)
-   English to and from Vietnamese (`en-vi` and `vi-en`)

For more information, see [List of supported languages](/docs/language-translator-data?topic=language-translator-data-translation-models#list-languages-supported).

## Version 1.1.0 (November 2019)
{: #1.1.0}

{{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} is now available.
