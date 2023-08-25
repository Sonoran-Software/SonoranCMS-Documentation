# Getting Started

{% embed url="https://www.youtube.com/watch?v=eoI5ah6amf4" %}

## Setting up the Connection

To begin, head to the **Admin Panel -> Advanced -> TeamSpeak3 Integration**

Once in that section, enter the information corresponding to your TeamSpeak server:

* **IP/Hostname**: The IP (like 1.2.3.4) or the hostname (like google.com) that you use to connect to your TeamSpeak server
* **Query Port**: By default 10011 for most TeamSpeak servers (especially self-hosted ones). Check with your host provider to be sure
* **Server Port**: The port you use to connect to your TeamSpeak, which is by default 9987. (This will always be different from the Query Port)
* **ServerQuery Username/Password:** Check the section below for creating a serverquery login

<figure><img src="https://i.imgur.com/g3Bhbnd.png" alt=""><figcaption><p>Sonoran CMS - TeamSpeak Integration Settings</p></figcaption></figure>

Once you put all the TeamSpeak information into the inputs, click the **Save Integration Settings** button to save. If something is wrong, it'll display an error at the top of your screen that identifies the issue. If all correct, you should see:

<figure><img src="https://i.imgur.com/UOSLFV1.png" alt=""><figcaption><p>Sonoran CMS - Configuration Successful</p></figcaption></figure>

## Creating a Server Query Login

### The User Method

This method is the easiest for creating a server query login, but the permissions of the login are tied to the user creating it. In the event that the person who created the login loses their permissions, role syncing will not be possible

1. While connected to your TeamSpeak server, go to the **Top Toolbar -> Tools -> ServerQuery Login**

<figure><img src="https://i.imgur.com/1lZcMiC.png" alt="" width="563"><figcaption><p>TeamSpeak - ServerQuery Login</p></figcaption></figure>

2. Enter any preferred username into the "Name" field of the popup and click **OK**

<figure><img src="https://i.imgur.com/QbX35nM.png" alt=""><figcaption><p>TeamSpeak - ServerQuery Name</p></figcaption></figure>

3. In the new popup, the "Name" field is your username is the "Password" is your server query password. Note that you will lose the password if you close the popup without saving it.

<figure><img src="https://i.imgur.com/BbcDNFl.png" alt=""><figcaption><p>TeamSpeak - ServerQuery Password</p></figcaption></figure>

### The serveradmin Method (Self-Hosted Only)

This method only works if you self-host the TeamSpeak server, but it doesn't have the permission issues like the user method.

The `serveradmin` password is found:

1. In the original popup when you create your TeamSpeak, the same dialog that had your Server Admin permission key
2. Or by changing the serveradmin password manually ([use this guide](https://support.teamspeak.com/hc/en-us/articles/360002712878-How-do-I-change-my-ServerQuery-Admin-password-))

Now that you have the password, you can put that into CMS along with the username `serveradmin`&#x20;

## Setting up Role Sync

Now that you've got the connection, it's time to setup which CMS Ranks correspond to which TeamSpeak Groups!

{% content-ref url="adding-ranks.md" %}
[adding-ranks.md](adding-ranks.md)
{% endcontent-ref %}

