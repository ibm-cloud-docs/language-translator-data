---

copyright:
  years: 2019, 2020
lastupdated: "2020-08-24"

subcollection: language-translator-data

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:deprecated: .deprecated}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:ruby: .ph data-hd-programlang='ruby'}
{:swift: .ph data-hd-programlang='swift'}
{:apikey: data-credential-placeholder='apikey'}
{:url: data-credential-placeholder='url'}
{:hide-dashboard: .hide-dashboard}

# Getting started with {{site.data.keyword.languagetranslatorshort}}
{: #gettingstarted}

{{site.data.keyword.languagetranslatorfull}} for {{site.data.keyword.icp4dfull_notm}} allows you to translate text programmatically from one language into another language.
{:shortdesc}

This tutorial walks you through the commands to translate text from English to Spanish, and to identify the language of a text sample.

## Before you begin
{: #prerequisites}

1.  Provision the instance of the {{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}}. For more information about provisioning, see [Installing](/docs/language-translator-data?topic=language-translator-data-install).
1.  From the {{site.data.keyword.icp4dfull_notm}} web client menu, choose **My Instances**.
1.  Click the {{site.data.keyword.nlushort}} instance to open the overview page. Copy the `{token}` and `{url}` credential values.
1.  Make sure that you have the `curl` command.
    - Test whether `curl` is installed. Run the following command on the command line. If the output lists the `curl` version with SSL support, you are set for the tutorial.

        ```bash
        curl -V
        ```
        {: pre}
    - If necessary, install a version with SSL enabled from [curl.haxx.se](https://curl.haxx.se/){: external}.
1.  To disable certificate verification by `curl`, include the `-k` (or `--insecure`) option with the command. You need to disable SSL verification if you use a self-signed certificate.

    Enabling SSL verification is highly recommended. Disable SSL only if necessary, and take steps to enable SSL as soon as possible.
    {: note}

This tutorial shows you how to use the {{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} API from a command-line interface. For more information about client libraries for various programming languages, see [Watson SDKs](/docs/natural-language-understanding-data?topic=watson-using-sdks#using-sdks).
{:tip}

## Step 1: Translate text
{: #translate-text}

Use the following example to translate two phrases, "Hello, world." and "How are you?", from English to Spanish. <span class="hide-dashboard">Replace `{token}` and `{url}` with your service credentials.</span> In the command, `model_id` identifies the installed model to be used for translation, in this case `en-es`.

```bash
curl -X POST \
--header "Authorization: Bearer {token}" \
--header "Content-Type: application/json" \
--data '{"text": ["Hello, world.", "How are you?"], "model_id":"en-es"}' \
"{url}/v3/translate?version=2018-05-01"
```
{: pre}

The `/v3/translate` method accepts a maximum of 50 KB of input text encoded in UTF-8 format for translation.
{: note}

## Step 2: Identify language
{: #identify-language}

Use the following example to identify the language of the text. <span class="hide-dashboard">Replace `{token}` and `{url}` with your service credentials.</span>

```bash
curl -X POST \
--header "Authorization: Bearer {token}" \
--header "Content-Type: text/plain" \
--data "Language Translator translates text from one language to another" \
"{url}/v3/identify?version=2018-05-01"
```
{: pre}

## Step 3: Translate a document (Beta)
{: #translate-a-document}

{{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} allows you to translate documents, such as markup files that use XML or HTML, or Microsoft Office and Open Office files, while retaining the original formatting. For a tutorial, see [Translating documents (Beta)](/docs/language-translator-data?topic=language-translator-data-document-translator-tutorial).

## Next steps
{: #next-steps}

- View the [API reference](https://{DomainName}/apidocs/language-translator-data){: external}
- View language support information:
    - [Translation models](/docs/language-translator-data?topic=language-translator-data-translation-models)
    - [Identifiable languages](/docs/language-translator-data?topic=language-translator-data-identifiable-languages)
