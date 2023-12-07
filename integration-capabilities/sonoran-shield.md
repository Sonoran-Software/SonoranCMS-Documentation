---
description: Manage your Sonoran Server's network protection, right from the CMS!
---

# Sonoran Shield

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Sonoran CMS x Sonoran Servers - Shield</p></figcaption></figure>

## Linking your Sonoran Server

Once you have purchased a [VPS or Dedicated server from Sonoran Servers](https://sonoranservers.com/):

In the `Admin` panel, navigate to `Integrations` > `Sonoran Shield` > `Link Your Server`

Enter in your Sonoran Servers login credentials.

## Configuring your Shield

It is **recommended** to do the following in order to stop network attacks with Sonoran Shield:

1. Block all unused ports using a "block-all" rule
2. Allow traffic to used ports, allowing all traffic to ports used by your users and whitelisting specific IPs for management ports (such as Remote Desktop or SSH ports)
3. Apply Application Filtering rules to all ports that are open based on their specific application

The following linked guides walk you through how to complete each of the above steps:

* [Block unused ports and open required ones](https://info.sonoranservers.com/tutorials/sonoran-shield/firewall-rules)
* [Apply application-specific filters](https://info.sonoranservers.com/tutorials/sonoran-shield/application-filters)
* [View your attack history](https://info.sonoranservers.com/tutorials/sonoran-shield/attack-history)

## Sonoran Shield Permissions

CMS allows you to grant shield access to other administrators.

In the [rank manager](../tutorials/user-management/creating-departments.md), their role will need the `Modify Sonoran Shield` permission under the `System` tab.

<figure><img src="../.gitbook/assets/image (6) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>
