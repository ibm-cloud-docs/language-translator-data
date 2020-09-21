---

copyright:
  years: 2015, 2020
lastupdated: "2020-07-29"

subcollection: language-translator-data

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:tip: .tip}
{:note: .note}
{:pre: .pre}
{:beta: .beta}
{:codeblock: .codeblock}
{:screen: .screen}
{:curl: .ph data-hd-programlang='curl'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# Translating documents (Beta)
{: #document-translator-tutorial}

You can use {{site.data.keyword.languagetranslatorfull}} for {{site.data.keyword.icp4dfull}} to translate files from one language to another while preserving the original document format. The service supports translation of a dozen different file formats, including Microsoft Office and Open Office formats.
{:shortdesc}

Document translation is currently a Beta feature.
{: beta}

## Before you begin
{: #translate-prerequisites}

Make sure that you have the following information and meet the following requirements:

-   You need your {{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} service credentials (`token` and `url`). For more information, see [Getting started with {{site.data.keyword.languagetranslatorshort}}](/docs/language-translator-data?topic=language-translator-data-gettingstarted).
-   The document that you want to translate must not exceed the size limit of 20 MB.
-   The document must be in one of the [Supported file formats (Beta)](#supported-file-formats) or [Supported file formats (Experimental)](#supported-file-formats-experimental).
-   The source and target languages must be among the [Supported translation models](/docs/language-translator-data?topic=language-translator-data-translation-models).

This tutorial walks you through translating documents from the command line with `curl`. You can also use the {{site.data.keyword.watson}} SDKs to translate documents with a number of programming languages. For more information, see the methods in the [API reference](https://{DomainName}/apidocs/language-translator-data){: external}.

## Step 1: Submit a document to translate
{: #submit-document-to-translate}

The following example request submits the file **curriculum.html** to the service and translates it from English to French. Replace `{token}` and `{url}` with your service credentials, and replace `curriculum.html` with a relative path to your file. The `source` and `target` parameters specify the languages for the translation.

```bash
curl -X POST \
--header "Authorization: Bearer {token}" \
--form "file=@curriculum.html" \
--form "source=en" \
--form "target=fr" \
"{url}/v3/documents?version=2018-05-01"
```
{: pre}

Microsoft Windows users, replace the backslash (`\`) at the end of each line with a caret (`^`). Make sure there are no trailing spaces after the caret.
{: tip}

A successful translation request returns a document ID in the response. In the following example, the ID is `bae02796-0d28-435c-9115-888359fdde62`. The `status` of `processing` indicates that the service is translating the document.

```json
{
  "document_id": "bae02796-0d28-435c-9115-888359fdde62",
  "filename": "curriculum.html",
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

After you have submitted a document for translation, you can check the translation status to find out when the translated document is available to download. The following example request checks the translation status of the document with ID `bae02796-0d28-435c-9115-888359fdde62`. When the `status` in the response is `available`, the translated document is ready to download.

```bash
curl -X GET \
--header "Authorization: Bearer {token}" \
"{url}/v3/documents/bae02796-0d28-435c-9115-888359fdde62?version=2018-05-01"
```
{: pre}

```json
{
  "document_id": "bae02796-0d28-435c-9115-888359fdde62",
  "filename": "curriculum.html",
  "model_id": "en-fr",
  "source": "en",
  "target": "fr",
  "status": "available",
  "created": "2018-10-11T03:31:25",
  "completed": "2018-10-11T03:31:38"
}
```
{: codeblock}

## Step 3: Download the translated document
{: #download-translated-document}

The following example request saves the translated document with ID `bae02796-0d28-435c-9115-888359fdde62` to a file named `curriculum-fr.html`.

```bash
curl -X GET \
--header "Authorization: Bearer {token}" \
--output "curriculum-fr.html" \
"{url}/v3/documents/bae02796-0d28-435c-9115-888359fdde62/translated_document?version=2018-05-01"
```
{: pre}

## Step 4: Translate a previously submitted document
{: #translate-document-by-reference}

The following example request translates the original English file **curriculum.html**, which has document ID `bae02796-0d28-435c-9115-888359fdde62`, to Portuguese.

```bash
curl -X POST \
--header "Authorization: Bearer {token}" \
--form "document_id=bae02796-0d28-435c-9115-888359fdde62" \
--form "source=en" \
--form "target=pt" \
"{url}/v3/documents?version=2018-05-01"
```
{: pre}

```json
{
  "document_id": "a0ge2746-ad38-7d5c-7025-4cd3g9f451ab"
}
```
{: codeblock}

The response contains a new document ID. Repeat step two with the new document ID to check the status of the translation. When the status becomes `available`, use the new document ID to download the translated file as shown in step three.

## Step 5: Delete documents
{: #delete-documents}

To delete documents that you no longer need, use the **Delete document** method. In this tutorial, the English file **curriculum.html** was involved with two translations, so two requests are required to delete all copies of the original document.

Delete the original submission of **curriculum.html** and the French translation by using the document ID for that translation, `bae02796-0d28-435c-9115-888359fdde621`:

```bash
curl -X DELETE \
--header "Authorization: Bearer {token}" \
"{url}/v3/documents/bae02796-0d28-435c-9115-888359fdde62?version=2018-05-01"
```
{: pre}

Delete the duplicate of the original **curriculum.html** file and the Portuguese translation by the using the document ID for that translation, `a0ge2746-ad38-7d5c-7025-4cd3g9f451ab`:

```bash
curl -X DELETE \
--header "Authorization: Bearer {token}" \
"{url}/v3/documents/a0ge2746-ad38-7d5c-7025-4cd3g9f451ab?version=2018-05-01"
```
{: pre}

## Supported file formats (Beta)
{: #supported-file-formats}

Translation of the following file formats is Beta functionality:

-   Microsoft Office
    -   Word: `.doc`, `.docx`
    -   PowerPoint: `.ppt`, `.pptx`
    -   Excel: `.xls`, `.xlsx`
    -   Rich Text Format: `.rtf`
-   Open Office
    -   Writer: `.odt`
    -   Impress: `.odp`
    -   Calc: `.ods`
-   Other formats
    -   HTML: `.htm`, `.html`
    -   XML: `.xml`
    -   JSON: `.json` (values with type `string` or `string array` are translated)
    -   Text: `.txt`

## Supported file formats (Experimental)
{: #supported-file-formats-experimental}

Translation of the following file format is Experimental functionality:

- PDF: `.pdf`

The quality of PDF translation is still largely an Alpha release. The translation works best for single-column PDF documents that do not include many tables or images. Quality is expected to evolve and improve with future releases.
