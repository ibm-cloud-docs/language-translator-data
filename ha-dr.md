---

copyright:
  years: 2019, 2020
lastupdated: "2020-06-19"

subcollection: language-translator-data

---

{:external: target="_blank" .external}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}

# High availability and disaster recovery
{: #ha-dr}

{{site.data.keyword.languagetranslatorfull}} for {{site.data.keyword.icp4dfull_notm}} is highly available within multiple {{site.data.keyword.cloud_notm}} locations (for example, Dallas and Washington, DC). However, recovering from potential disasters that affect an entire location requires planning and preparation.
{: shortdesc}

You are responsible for understanding your configuration, customization, and usage of the service. You are also responsible for being ready to re-create an instance of the service in a new location and to restore your data in any location. See [How do I ensure zero downtime?](/docs/overview?topic=overview-zero-downtime#zero-downtime){: external} for more information.

## High availability
{: #high-availability}

{{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} supports high availability with no single point of failure. The service achieves high availability automatically and transparently by using the multi-zone region (MZR) feature provided by {{site.data.keyword.cloud_notm}}.

{{site.data.keyword.cloud_notm}} enables multiple zones that do not share a single point of failure within a single location. It also provides automatic load balancing across the zones within a region.

## Disaster recovery
{: #disaster-recovery}

In the event of a catastrophic failure in a region, complete the following steps.

- Create a new {{site.data.keyword.languagetranslatorshort}} for {{site.data.keyword.icp4dfull_notm}} service instance.
- Adjust your application software to use the new service instance URL and credentials.
