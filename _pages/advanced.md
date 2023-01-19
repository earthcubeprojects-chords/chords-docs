---
layout: single
title: Advanced
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
permalink: /advanced/
toc: true
toc_sticky: true
toc_label: "Table of Contents"
toc_icon: "cog"
---

## chords_control

When you {% highlight sh %} curl -O -k https://raw.githubusercontent.com/earthcubeprojects-chords/chords/development/chords_control {% endhighlight %} a file named "chords_control" is created in your folder "chords". This file sets up and maintains your portal. ``chords_control`` is the CHORDS management script. Used to manage the CHORDS portal configuration, running/stopping the portal, and updating the portal software.

 
There are several main ways to use chords_control

``python3 chords_control --config``
- Lets you configure your CHORDS portal.
  - Set internal system passwords. These are only accessed from the system console.
  - Configure the email account that is used for CHORDS password reset emails and Grafana alert emails.
  - Configure the CHORDS port numbers.
  - Enable and configure HTTPS (for only the portal, not for Grafana)

``python3 chords_control --update``
- Updates your portal's software

``python3 chords_control --run``
- Starts your CHORDS portal

``python3 chords_control --stop``
- Stops your CHORDS portal

``python3 chords_control --status``
- Lets you check your portal's current status

Use ``python3 chords_control --help`` to get a help menu.

## Email support

CHORDS will use email to send password reset messages and Grafana alerts messages. However, an existing email account on an SMTP server must be configured to
serve as a relay.

It is highly recommended that you create an email account specifically for this purpose,
so that you don't pollute a personal account with CHORDS administrative traffic.

### Using Gmail as a relay

Google gmail is a good choice for this function. However, gmail servers do not allow
arbitrary applications to log in with the user's regular credentials. But CHORDS will be 
able to log in using an 'application password'.

Once you have created the gmail account, open the account settings and:
  - select the Security tab. 
  - find the section that says “Signing in to Google”.
  - enable ‘2-step verification’ (you will need to add a 2FA recipient).
  - Go into App passwords, and create a new App password. Be sure to save it immediately, because they will never make it visible again.

Configure CHORDS:
  - Run ``python3 chords_control --config``.
    - Set CHORDS_EMAIL_ADDRESS to the gmail address.
    - Set CHORDS_EMAIL_PASSWORD to the App password.
  - restart CHORDS: ``python3 chords_control --restart``.

Log into the CHORDS website as admin@chordsrt.com, go to the Configure page, 
and press the 'test email' button..
You should also see the forwarded (relayed) messages in the gmail account inbox.

## Portal Backup and Restoration

``python3 chords_control --backup``
- Creates a backup .tar file of your portal

``python3 chords_control --restore (backup_file.tar)``
- Restores your CHORDS portal to the backup version

{% include video id="Tr1kRlVfFrQ" provider="youtube" %}

## Docker

Docker is used as a tool to make it easier to create, deploy and run CHORDS by using containers. Containers let us package CHORDS with all the parts it needs, like libraries and other dependencies, and ship it out in one nice simple package. For more information on Docker check out their [website](https://docs.docker.com/get-started/){:target="_blank"}.

### Docker logs

``docker exec -it chords_app tail -f log/production.rb`` command shows information logged by a running chords container.

### Removing old docker images

To remove a specific Image
``docker images -a`` Lists ID’s of images 
``docker rmi Image Image`` Place image ID after “docker rmi” to remove it specifically

 ``docker system prune`` Lets you clean up resources (images, containers, volumes, and networks) that are not associated with the container.


``docker system prune -a`` Lets you remove stopped containers as well as the resources listed above. (Use with CAUTION)

``docker exec -it (containername) /bin/bash``

### Save disk space

``docker system df`` Shows docker disk usage
``docker system events`` Gets real time events from the server
``docker system info`` Displays system-wide information
``docker system prune`` Removes unused data