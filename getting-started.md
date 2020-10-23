---

copyright:
  years: 2019, 2020
lastupdated: "2020-10-23"

keywords: language translator data,getting started,translate,identify language,translate document,translation

subcollection: language-translator-data

content-type: tutorial
completion-time: 10m

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
{:step: data-tutorial-type='step'}

# Getting started with {{site.data.keyword.languagetranslatorshort}}
{: #gettingstarted}
{: toc-content-type="tutorial"}
{: toc-completion-time="10m"}

{{site.data.keyword.languagetranslatorfull}} for {{site.data.keyword.icp4dfull_notm}} allows you to translate text programmatically from one language into another language.
{:shortdesc}

This tutorial walks you through the commands to translate text from English to Spanish, and to identify the language of a text sample.

## Before you begin
{: #prerequisites}

1.  Provision the instance of the {{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}}. For more information about provisioning, see [Installing](/docs/language-translator-data?topic=language-translator-data-install).
1.  From the {{site.data.keyword.icp4dfull_notm}} web client menu, choose **My Instances**.
1.  Click the {{site.data.keyword.nlushort}} instance to open the overview page. Copy the `{token}` and `{url}` credential values.

This tutorial uses an API key to authenticate. In production, use an IAM token. For more information see [Authenticating to Watson services](/docs/watson?topic=watson-iam).
{: tip}

### Using the curl examples
{: #getting-started-curl}

This tutorial uses the `curl` command to call methods of the service's HTTP interface. Make sure that you have the `curl` command installed on your system.

1.  To test whether `curl` is installed, run the following command on the command line. If the output lists the `curl` version that supports Secure Sockets Layer (SSL), you are set for the tutorial.

    ```bash
    curl -V
    ```
    {: pre}

1.  If necessary, install the version of `curl` with SSL enabled for your operating system from [curl.haxx.se](https://curl.haxx.se/){: external}.

Omit the braces (`{ }`) from the examples. They indicate variable values.
{: tip}

## Translate text
{: #translate-text}
{: step}

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

## Identify language
{: #identify-language}
{: step}

Use the following example to identify the language of the text. <span class="hide-dashboard">Replace `{token}` and `{url}` with your service credentials.</span>

```bash
curl -X POST \
--header "Authorization: Bearer {token}" \
--header "Content-Type: text/plain" \
--data "Language Translator translates text from one language to another" \
"{url}/v3/identify?version=2018-05-01"
```
{: pre}

## Translate a document (Beta)
{: #translate-a-document}
{: step}

{{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} allows you to translate documents, such as markup files that use XML or HTML, or Microsoft Office and Open Office files, while retaining the original formatting. For a tutorial, see [Translating documents (Beta)](/docs/language-translator-data?topic=language-translator-data-document-translator-tutorial).

## Next steps
{: #next-steps}

- View the [API & SDK reference](https://{DomainName}/apidocs/language-translator-data){: external}
- View language support information:
    - [Translation models](/docs/language-translator-data?topic=language-translator-data-translation-models)
    - [Identifiable languages](/docs/language-translator-data?topic=language-translator-data-identifiable-languages)
