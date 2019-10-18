---

copyright:
  years: 2019
lastupdated: "2019-10-15"

keywords: dns-svcs, DNS Services, Private DNS

subcollection: dns-svcs

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:external: target="_blank" .external}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:download: .download}


# Managing DNS records
{:#managing-dns-records}

{{site.data.keyword.cloud}} DNS Services is in Experimental Release. At this time the service is available to whitelisted customers only.
{: important}

You can manage DNS records in a variety of ways, such as adding, updating, and deleting.

## Adding DNS records
{:#adding-dns-records}

  1. From the DNS zones table, click the zone name you want to add record(s) to. You will see more details on the selected zone. 
  2. Click the `Add Record` button to display a side panel for creating a record.

You can use the **Type** dropdown to select the type of record you want to create. Each DNS record type has a Name and Time-To-Live (TTL) associated with it. 

Whatever you enter into the Name field has a domain name appended to it unless the domain name is manually added into the field already (for example, if `www` or `www.example.com` is typed into the field, the API will handle both as `www.example.com`). If the exact domain name is typed into the name field, then it won't be appended on itself (for example, `example.com` will be handled as `example.com`). However, the list of DNS records only show the names without the domain name added on. As a result, `www.example.com` displays as `www` and `example.com` as `example.com`. 

The TTL always has a default value of `1 min`, but it can be changed.
{: note}

### A Type record

To add this record type, valid values must exist in the **Name** and **IPv4 Address** fields. A **TTL** also can be specified from the dropdown menu, with a default value of `1 min`.

    Required Fields: Name, IPv4 Address
    Optional Field: TTL (Default value is 1 min)

### AAAA Type record

To add this record type, valid values must exist in the **Name** and **IPv6 Address** fields. A **TTL** also can be specified from the dropdown menu, with the default value of `1 min`.

    Required Fields: Name, IPv6 Address
    Optional Field: TTL (Default value is 1 min)

### CNAME Type record

To add this record type, a valid value must exist in the **Name** field and a fully qualified domain name must be in the **Target** (FQDN) field. A **TTL** also can be specified from the dropdown menu, with the default value of `1 min`.

    Required Fields: Name, Target (for CNAME)
    Optional Field: TTL (Default value is 1 min)

### MX Type record

To add this record type, a valid value must exist in the **Name** field, a fully qualified domain name must be in the **Mail Server** (FQDN)field, and a valid number must exist in the **Priority** field. A **TTL** also can be specified from the dropdown menu, with the default value of `1 min`.

    Required Fields: Name, Mail Server
    Optional Fields: TTL (Default value is 1 min), Priority (Default value is 1)

### PTR Type record

To add this record type, an existing A or AAAA records must be created beforehand that are not already associated with another PTR record. A dropdown allows you to select an existing record, and doing so is mandatory. A **TTL** can also be specified from the dropdown menu, with the default value of `1 min`.

    Required Fields: Select existing record
    Optional Fields: TTL (Default value is 1 min)

### SRV Type record

To add this record type, valid values must exist in the **Name**, **Service Name** and **Target** fields. Use the dropdown menu to select a **protocol**, which defaults to the UDP protocol. Additionally, you can specify **Priority**, **Weight** and **Port**. These three fields default to a value of `1`. A **TTL** can also be specified from the dropdown menu, with the default value of `1 min`.

    Required Fields: Name, Service Name, Target
    Optional Fields: TTL (Default value is Automatic), Protocol (Default value is UDP),
                     Priority (Default value is 1), Weight (Default value is 1), Port (Default value is 1)

### TXT Type record

To add this record type, valid values must exist in the **Name** and **Content** fields. A **TTL** can also be specified from the dropdown menu, with the default value of `1 min`.

    Required Fields: Name, Content
    Optional Field: TTL (Default value is 1 min)

## Updating DNS records
{:#updating-dns-records}

In each record row, click the **Edit** icon to open a side panel where you can update the record.

## Deleting DNS records
{:#deleting-dns-records}

In each record row, click the **Delete** icon to open a dialog box where you can confirm the delete process.
