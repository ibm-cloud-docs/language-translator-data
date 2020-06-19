---

copyright:
  years: 2015, 2020
lastupdated: "2020-06-19"

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:tip: .tip}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}

# Translation models
{: #translation-models}

{{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} can translate the following languages. Click a language in the list below to view a list of compatible translation models.

All languages listed here might not be available. Ask an administrator which languages are installed with {{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}}.

You can also use the [List models](https://cloud.ibm.com/apidocs/language-translator-data#list-models){: external} API method to view the translation models that are available. You can filter results by language with the `source` and `target` parameters. The following example lists models that can translate English to Spanish.

```sh
curl --header "Authorization: Bearer {token}" "{url}/v3/models?source=en&target=es&version=2018-05-01"
```
{: pre}

For more information, see the [API reference](https://cloud.ibm.com/apidocs/language-translator-data#list-models){: external}.

- [Arabic](#arabic)
- [Bengali](#bengali)
- [Bulgarian](#bulgarian)
- [Catalan](#catalan) (only to and from Spanish)
- [Chinese (Simplified)](#chinese-simplified)
- [Chinese (Traditional)](#chinese-traditional)
- [Croatian](#croatian)
- [Czech](#czech)
- [Danish](#danish)
- [Dutch](#dutch)
- [English](#english)
- [Estonian](#estonian)
- [Finnish](#finnish)
- [French](#french)
- [German](#german)
- [Greek](#greek)
- [Gujarati](#gujarati)
- [Hebrew](#hebrew)
- [Hindi](#hindi)
- [Hungarian](#hungarian)
- [Irish](#irish)
- [Indonesian](#indonesian)
- [Italian](#italian)
- [Japanese](#japanese)
- [Korean](#korean)
- [Latvian](#latvian)
- [Lithuanian](#lithuanian)
- [Malayalam](#malayalam)
- [Malay](#malay)
- [Maltese](#maltese)
- [Nepali](#nepali)
- [Norwegian Bokmål](#norwegian-bokmal)
- [Polish](#polish)
- [Portuguese](#portuguese)
- [Romanian](#romanian)
- [Russian](#russian)
- [Slovak](#slovak)
- [Slovenian](#slovenian)
- [Sinhala](#sinhala)
- [Spanish](#spanish)
- [Swedish](#swedish)
- [Tamil](#tamil)
- [Telugu](#telugu)
- [Thai](#thai)
- [Turkish](#turkish)
- [Urdu](#urdu)
- [Vietnamese](#vietnamese)

## Arabic
{: #arabic}

The following models can translate Arabic text.

| Model ID | Source        | Target         | Domain  |
|----------|---------------|----------------|---------|
| `ar-en`  | Arabic (`ar`) | English (`en`) | general |

## Bengali
{: #bengali}

The following models can translate Bengali text.

| Model ID | Source         | Target         | Domain  |
|----------|----------------|----------------|---------|
| `bn-en`  | Bengali (`bn`) | English (`en`) | general |

## Bulgarian
{: #bulgarian}

The following models can translate Bulgarian text.

| Model ID | Source        | Target         | Domain  |
|----------|---------------|----------------|---------|
| `ar-en`  | Arabic (`ar`) | English (`en`) | general |

## Catalan
{: #catalan}

The following models can translate Catalan text.

| Model ID | Source         | Target         | Domain  |
|----------|----------------|----------------|---------|
| `ca-es`  | Catalan (`ca`) | Spanish (`es`) | general |

## Chinese (Simplified)
{: #chinese-simplified}

The following models can translate Chinese (Simplified) text.

| Model ID | Source                    | Target         | Domain  |
|----------|---------------------------|----------------|---------|
| `zh-en`  | Simplified Chinese (`zh`) | English (`en`) | general |

## Chinese (Traditional)
{: #chinese-traditional}

The following models can translate Chinese (Traditional) text.

| Model ID   | Source                       | Target         | Domain  |
|------------|------------------------------|----------------|---------|
| `zh-TW-en` | Simplified Chinese (`zh-TW`) | English (`en`) | general |

## Croatian
{: #croatian}

The following models can translate Croatian text.

| Model ID | Source          | Target         | Domain  |
|----------|-----------------|----------------|---------|
| `hr-en`  | Croatian (`hr`) | English (`en`) | general |

## Czech
{: #czech}

The following models can translate Czech text.

| Model ID | Source       | Target         | Domain  |
|----------|--------------|----------------|---------|
| `cs-en`  | Czech (`cs`) | English (`en`) | general |

## Danish
{: #danish}

The following models can translate Danish text.

| Model ID | Source        | Target         | Domain  |
|----------|---------------|----------------|---------|
| `da-en`  | Danish (`da`) | English (`en`) | general |

## Dutch
{: #dutch}

The following models can translate Dutch text.

| Model ID | Source       | Target         | Domain  |
|----------|--------------|----------------|---------|
| `nl-en`  | Dutch (`nl`) | English (`en`) | general |

## English
{: #english}

The following models can translate English text.

| Model ID   | Source         | Target                        | Domain  |
|------------|----------------|-------------------------------|---------|
| `en-ar`    | English (`en`) | Arabic (`ar`)                 | general |
| `en-bg`    | English (`en`) | Bulgarian (`bg`)              | general |
| `en-bn`    | English (`en`) | Bengali (`bn`)                | general |
| `en-cs`    | English (`en`) | Czech (`cs`)                  | general |
| `en-da`    | English (`en`) | Danish (`da`)                 | general |
| `en-de`    | English (`en`) | German (`de`)                 | general |
| `en-el`    | English (`en`) | Greek (`el`)                  | general |
| `en-es`    | English (`en`) | Spanish (`es`)                | general |
| `en-et`    | English (`en`) | Estonian (`et`)               | general |
| `en-fi`    | English (`en`) | Finnish (`fi`)                | general |
| `en-fr`    | English (`en`) | French (`fr`)                 | general |
| `en-ga`    | English (`en`) | Irish (`ga`)                  | general |
| `en-gu`    | English (`en`) | Gujarati (`gu`)               | general |
| `en-he`    | English (`en`) | Hebrew (`he`)                 | general |
| `en-hi`    | English (`en`) | Hindi (`hi`)                  | general |
| `en-hr`    | English (`en`) | Croatian (`hr`)               | general |
| `en-hu`    | English (`en`) | Hungarian (`hu`)              | general |
| `en-id`    | English (`en`) | Indonesian (`id`)             | general |
| `en-it`    | English (`en`) | Italian (`it`)                | general |
| `en-ja`    | English (`en`) | Japanese (`ja`)               | general |
| `en-ko`    | English (`en`) | Korean (`ko`)                 | general |
| `en-lt`    | English (`en`) | Lithuanian (`lt`)             | general |
| `en-lv`    | English (`en`) | Latvian (`lv`)                | general |
| `en-ml`    | English (`en`) | Malayalam (`ml`)              | general |
| `en-ms`    | English (`en`) | Malay (`ms`)                  | general |
| `en-mt`    | English (`en`) | Maltese (`mt`)                | general |
| `en-ne`    | English (`en`) | Nepali (`ne`)                 | general |
| `en-nb`    | English (`en`) | Norwegian Bokmal (`nb`)       | general |
| `en-nl`    | English (`en`) | Dutch (`nl`)                  | general |
| `en-pl`    | English (`en`) | Polish (`pl`)                 | general |
| `en-pt`    | English (`en`) | Portuguese (`pt`)             | general |
| `en-ro`    | English (`en`) | Romanian (`ro`)               | general |
| `en-ru`    | English (`en`) | Russian (`ru`)                | general |
| `en-si`    | English (`en`) | Sinhala (`si`)                | general |
| `en-sk`    | English (`en`) | Slovak (`sk`)                 | general |
| `en-sl`    | English (`en`) | Slovenian (`sl`)              | general |
| `en-sv`    | English (`en`) | Swedish (`sv`)                | general |
| `en-ta`    | English (`en`) | Tamil (`ta`)                  | general |
| `en-te`    | English (`en`) | Telugu (`te`)                 | general |
| `en-th`    | English (`en`) | Thai (`th`)                   | general |
| `en-tr`    | English (`en`) | Turkish (`tr`)                | general |
| `en-ur`    | English (`en`) | Urdu (`ur`)                   | general |
| `en-vi`    | English (`en`) | Vietnamese (`vi`)             | general |
| `en-zh`    | English (`en`) | Simplified Chinese (`zh`)     | general |
| `en-zh-TW` | English (`en`) | Traditional Chinese (`zh-TW`) | general |

## Estonian
{: #estonian}

The following models can translate Estonian text.

| Model ID | Source          | Target         | Domain  |
|----------|-----------------|----------------|---------|
| `et-en`  | Estonian (`et`) | English (`en`) | general |

## Finnish
{: #finnish}

The following models can translate Finnish text.

| Model ID | Source         | Target         | Domain  |
|----------|----------------|----------------|---------|
| `fi-en`  | Finnish (`fi`) | English (`en`) | general |

## French
{: #french}

The following models can translate French text.

| Model ID | Source        | Target         | Domain  |
|----------|---------------|----------------|---------|
| `fr-en`  | French (`fr`) | English (`en`) | general |

## German
{: #german}

The following models can translate German text.

| Model ID | Source        | Target         | Domain  |
|----------|---------------|----------------|---------|
| `de-en`  | German (`de`) | English (`en`) | general |
| `de-fr`  | German (`de`) | French (`fr`)  | general |
| `de-it`  | German (`de`) | Italian (`it`) | general |

## Greek
{: #greek}

The following models can translate Greek text.

| Model ID | Source       | Target         | Domain  |
|----------|--------------|----------------|---------|
| `el-en`  | Greek (`el`) | English (`en`) | general |

## Gujarati
{: #gujarati}

The following models can translate Gujarati text.

| Model ID | Source          | Target         | Domain  |
|----------|-----------------|----------------|---------|
| `gu-en`  | Gujarati (`gu`) | English (`en`) | general |

## Hebrew
{: #hebrew}

The following models can translate Hebrew text.

| Model ID | Source        | Target         | Domain  |
|----------|---------------|----------------|---------|
| `he-en`  | Hebrew (`he`) | English (`en`) | general |

## Hindi
{: #hindi}

The following models can translate Hindi text.

| Model ID | Source       | Target         | Domain  |
|----------|--------------|----------------|---------|
| `hi-en`  | Hindi (`hi`) | English (`en`) | general |

## Hungarian
{: #hungarian}

The following models can translate Hungarian text.

| Model ID | Source           | Target         | Domain  |
|----------|------------------|----------------|---------|
| `hu-en`  | Hungarian (`hu`) | English (`en`) | general |

## Indonesian
{: #indonesian}

The following models can translate Indonesian text.

| Model ID | Source            | Target         | Domain  |
|----------|-------------------|----------------|---------|
| `id-en`  | Indonesian (`id`) | English (`en`) | general |

## Irish
{: #irish}

The following models can translate Irish text.

| Model ID | Source       | Target         | Domain  |
|----------|--------------|----------------|---------|
| `ga-en`  | Irish (`ga`) | English (`en`) | general |

[PostgreSQL]
(https://www.postgresql.org/)

[PostgreSQL](https://www.postgresql.org/)

## Italian
{: #italian}

The following models can translate Italian text.

| Model ID | Source         | Target         | Domain  |
|----------|----------------|----------------|---------|
| `it-de`  | Italian (`it`) | German (`de`)  | general |
| `it-en`  | Italian (`it`) | English (`en`) | general |

## Japanese
{: #japanese}

The following models can translate Japanese text.

| Model ID | Source          | Target         | Domain  |
|----------|-----------------|----------------|---------|
| `ja-en`  | Japanese (`ja`) | English (`en`) | general |

## Korean
{: #korean}

The following models can translate Korean text.

| Model ID | Source        | Target         | Domain  |
|----------|---------------|----------------|---------|
| `ko-en`  | Korean (`ko`) | English (`en`) | general |

## Latvian
{: #latvian}

The following models can translate Latvian text.

| Model ID | Source         | Target         | Domain  |
|----------|----------------|----------------|---------|
| `lv-en`  | Latvian (`lv`) | English (`en`) | general |

## Lithuanian
{: #lithuanian}

The following models can translate Lithuanian text.

| Model ID | Source            | Target         | Domain  |
|----------|-------------------|----------------|---------|
| `lt-en`  | Lithuanian (`lt`) | English (`en`) | general |

## Malay
{: #malay}

The following models can translate Malay text.

| Model ID | Source       | Target         | Domain  |
|----------|--------------|----------------|---------|
| `ms-en`  | Malay (`ms`) | English (`en`) | general |

## Malayalam
{: #malayalam}

The following models can translate Malayalam text.

| Model ID | Source           | Target         | Domain  |
|----------|------------------|----------------|---------|
| `ml-en`  | Malayalam (`ml`) | English (`en`) | general |

## Maltese
{: #maltese}

The following models can translate Maltese text.

| Model ID | Source         | Target         | Domain  |
|----------|----------------|----------------|---------|
| `mt-en`  | Maltese (`mt`) | English (`en`) | general |

## Nepali
{: #nepali}

The following models can translate Nepali text.

| Model ID | Source        | Target         | Domain  |
|----------|---------------|----------------|---------|
| `ne-en`  | Nepali (`ne`) | English (`en`) | general |

## Norwegian Bokmål
{: #norwegian-bokmal}

The following models can translate Norwegian Bokmål text.

| Model ID | Source                  | Target         | Domain  |
|----------|-------------------------|----------------|---------|
| `nb-en`  | Norwegian Bokmal (`nb`) | English (`en`) | general |

## Polish
{: #polish}

The following models can translate Polish text.

| Model ID | Source        | Target         | Domain  |
|----------|---------------|----------------|---------|
| `pl-en`  | Polish (`pl`) | English (`en`) | general |

## Portuguese
{: #portuguese}

The following models can translate Portuguese text.

| Model ID | Source            | Target         | Domain  |
|----------|-------------------|----------------|---------|
| `pt-en`  | Portuguese (`pt`) | English (`en`) | general |

## Romanian
{: #romanian}

The following models can translate Romanian text.

| Model ID | Source            | Target         | Domain  |
|----------|-------------------|----------------|---------|
| `ro-en`  | Romanian (`ro`) | English (`en`) | general |

## Russian
{: #russian}

The following models can translate Russian text.

| Model ID | Source         | Target         | Domain  |
|----------|----------------|----------------|---------|
| `ru-en`  | Russian (`ru`) | English (`en`) | general |

## Sinhala
{: #sinhala}

The following models can translate Sinhala text.

| Model ID | Source         | Target         | Domain  |
|----------|----------------|----------------|---------|
| `si-en`  | Sinhala (`si`) | English (`en`) | general |

### Slovak
{: #slovak}

The following models can translate Slovak text.

| Model ID | Source        | Target         | Domain  |
|----------|---------------|----------------|---------|
| `sk-en`  | Slovak (`sk`) | English (`en`) | general |

## Slovenian
{: #slovenian}

The following models can translate Slovenian text.

| Model ID | Source           | Target         | Domain  |
|----------|------------------|----------------|---------|
| `sl-en`  | Slovenian (`sl`) | English (`en`) | general |

## Spanish
{: #spanish}

The following models can translate Spanish text.

| Model ID | Source         | Target         | Domain  |
|----------|----------------|----------------|---------|
| `es-ca`  | Spanish (`es`) | Catalan (`ca`) | general |
| `es-en`  | Spanish (`es`) | English (`en`) | general |
| `es-fr`  | Spanish (`es`) | French (`fr`)  | general |

## Swedish
{: #swedish}

The following models can translate Swedish text.

| Model ID | Source         | Target         | Domain  |
|----------|----------------|----------------|---------|
| `sv-en`  | Swedish (`sv`) | English (`en`) | general |

## Tamil
{: #tamil}

The following models can translate Tamil text.

| Model ID | Source       | Target         | Domain  |
|----------|--------------|----------------|---------|
| `ta-en`  | Tamil (`ta`) | English (`en`) | general |

## Telugu
{: #telugu}

The following models can translate Telugu text.

| Model ID | Source        | Target         | Domain  |
|----------|---------------|----------------|---------|
| `te-en`  | Telugu (`te`) | English (`en`) | general |

## Thai
{: #thai}

The following models can translate Thai text.

| Model ID | Source      | Target         | Domain  |
|----------|-------------|----------------|---------|
| `th-en`  | Thai (`th`) | English (`en`) | general |

## Turkish
{: #turkish}

The following models can translate Turkish text.

| Model ID | Source         | Target         | Domain  |
|----------|----------------|----------------|---------|
| `tr-en`  | Turkish (`tr`) | English (`en`) | general |

## Urdu
{: #urdu}

The following models can translate Urdu text.

| Model ID | Source      | Target         | Domain  |
|----------|-------------|----------------|---------|
| `ur-en`  | Urdu (`ur`) | English (`en`) | general |

## Vietnamese
{: #vietnamese}

The following models can translate Vietnamese text.

| Model ID | Source            | Target         | Domain  |
|----------|-------------------|----------------|---------|
| `vi-en`  | Vietnamese (`vi`) | English (`en`) | general |
