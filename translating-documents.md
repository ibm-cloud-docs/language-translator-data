---

copyright:
  years: 2015, 2020
lastupdated: "2020-06-19"

---
<!-- Attribute definitions -->
{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:tip: .tip}
{:note: .note}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:curl: .ph data-hd-programlang='curl'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}
{:download: .download}

# Translating documents (Beta)
{: #document-translator-tutorial}

Translate files from one language to another while preserving the original format. More than 12 different file formats can be translated, including MS Office, Open Office, and PDF.
{:shortdesc}

## Before you begin
{: #translate-prerequisites}

- [Get started](/docs/language-translator-data?topic=language-translator-data-gettingstarted) with {{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}}. You need your {{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} service credentials (`token` and `url`).
- Make sure the document you want to translate meets the following requirements:
    - Maximum file size: **20 MB**
    - [Supported file formats](#supported-file-formats)
    - [Supported translation models](/docs/language-translator-data?topic=language-translator-data-translation-models)

This tutorial walks you through translating documents from a command line with curl. To view document translation examples in different programming languages, follow the links to the methods in the [API reference](https://{DomainName}/apidocs/language-translator-data) for each step.
{: note}

## Step 1: Submit a document to translate
{: #submit-document-to-translate}

The following [Translate document](https://{DomainName}/apidocs/language-translator-data#translate-document){: external} request submits an example file *curriculum.pdf* to the service and translates it from English to French. Replace `{apikey}` and `{url}` with your service credentials, and replace `curriculum.pdf` with a relative path to your file.

Example request:
```bash
curl -X POST \
"{url}/v3/documents?version=2018-05-01" \
--header "Authorization: Bearer {token}" \
--form "file=@curriculum.pdf" \
--form "source=en" \
--form "target=fr"
```
{: pre}

A successful request returns a `document_id` in the response.


Example response:
```json
{
  "document_id": "bae02796-0d28-435c-9115-888359fdde62",
  "filename": "curriculum.pdf",
  "model_id": "en-fr",
  "source": "en",
  "target": "fr",
  "status": "processing",
  "created": "2018-10-11T03:31:25"
}
```
{: codeblock}

## Step 2: Check the translation status
{: #check-translation-status}

After you have submitted a document for translation, you can use the [Get document status](https://{DomainName}/apidocs/language-translator-data#get-document-status){: external} method to find out when the translated document is available to download. The following example request checks the translation status of the document with document ID  `bae02796-0d28-435c-9115-888359fdde62`.

Example request:
```bash
curl -X GET \
"{url}/v3/documents/bae02796-0d28-435c-9115-888359fdde62?version=2018-05-01" \
--header "Authorization: Bearer {token}"
```
{: pre}

Example response:
```json
{
  "document_id": "bae02796-0d28-435c-9115-888359fdde62",
  "filename": "curriculum.pdf",
  "model_id": "en-fr",
  "source": "en",
  "target": "fr",
  "status": "available",
  "created": "2018-10-11T03:31:25",
  "completed": "2018-10-11T03:31:38"
}
```
{: codeblock}

When the `status` in the response is `available`, the translated document is ready to download.

## Step 3: Download the translated document
{: #download-translated-document}

The following [Get translated document](https://{DomainName}/apidocs/language-translator-data#get-translated-document){: external} request saves the translated document with document ID `bae02796-0d28-435c-9115-888359fdde62` to the file *curriculum-fr.pdf*.

Example request:
```bash
curl -X GET \
"{url}/v3/documents/bae02796-0d28-435c-9115-888359fdde62/translated_document?version=2018-05-01" \
--header "Authorization: Bearer {token}" \
--output "curriculum-fr.pdf"

```
{: pre}

## Step 4: Translate a previously submitted document
{: #translate-document-by-reference}

The following [Translate document](https://{DomainName}/apidocs/language-translator#translate-document){: external} request references the original English *curriculum.pdf* file with the `document_id` `bae02796-0d28-435c-9115-888359fdde62` and translates it to Portuguese.

Example request:
```bash
curl -X POST \
"{url}/v3/documents?version=2018-05-01" \
--header "Authorization: Bearer {token}" \
--form "document_id=bae02796-0d28-435c-9115-888359fdde62" \
--form "source=en" \
--form "target=pt"
```
{: pre}

Example response:
```json
{
  "document_id": "a0ge2746-ad38-7d5c-7025-4cd3g9f451ab"
}
```
{: codeblock}

The response contains a new `document_id`. Repeat steps two and three with your new `document_id` to check the status of the translation, and to download the translated file once it is available.

## Step 5: Delete documents
{: #delete-documents}

To delete documents manually, use the [Delete document](https://{DomainName}/apidocs/language-translator#delete-document){: external} method. In this tutorial, the English *curriculum.pdf* file was involved with two translations, so two requests are required to delete all copies of the original document.

Delete the original submission of *curriculum.pdf* and the French translation:
```bash
curl -X DELETE \
"{url}/v3/documents/bae02796-0d28-435c-9115-888359fdde62?version=2018-05-01" \
--header "Authorization: Bearer {token}"
```
{: pre}

Delete the duplicate of the original *curriculum.pdf* file and the Portuguese translation:
```bash
curl -X DELETE \
"{url}/v3/documents/a0ge2746-ad38-7d5c-7025-4cd3g9f451ab?version=2018-05-01" \
--header "Authorization: Bearer {token}"
```
{: pre}

## Supported file formats
{: #supported-file-formats}

- Microsoft Office
    - Word: `.doc`, `.docx`
    - PowerPoint: `.ppt`, `.pptx`
    - Excel: `.xls`, `.xlsx`
    - Rich Text Format: `.rtf`
- Open Office
    - Writer: `.odt`
    - Impress: `.odp`
    - Calc: `.ods`
- Other formats
    - PDF: `.pdf`
    - HTML: `.htm`, `.html`
    - XML: `.xml`
    - JSON: `.json` (values with type `string` or `string array` are translated)
    - Text: `.txt`
