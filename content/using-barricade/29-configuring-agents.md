+++
title = "Configuring Agents"
description = "How to configure a Barricade Agent"
weight = "29"

tags = ["agent", "configuration"]
section = "using-barricade"
categories = ["using-barricade"]
type = "page"
slug = "configuring-agents"

[menu.main]
    url = "configuring-agents"
    parent = "using-barricade"

+++

By default, Agents are optimized to handle heavy traffic without impacting on the performance of your server - but you can always change the configuration to suit your needs.

## Configuration File

Config settings can be found and modified in this file on your server: 

`/etc/barricade/barricade.cfg`

Once updated, a restart is **required** for any changes to take effect:

`sudo restart barricade`

## Configuration Options:

### tag

_Tag_ is an arbitrary config value which can be used to identify and organize your Agents - particularly useful for [Filtering Agents](#tagging-filtering). The default value is `production`.

`tag=production`

You can e.g. to denote _development, staging, production environments, "commit" versions_, etc.

`tag=staging,development,beta`

### high_water_mark

This is the maximum number of packets per second that the agent will send to Barricade. Default value is 10,000 packets per second.

`high_water_mark=10000`

After this, the Agent will begin dropping older packets to prioritize the newest information, and emit a warning to this effect in the logs (/var/log/barricade.log on most systems, in journalctl for systemd based systems).

## Barricade.cfg Troubleshooting

**Some options do not appear in my barricade.cfg file.**  
Your Agent may not be up to date - ensure you have [updated to the latest version](#updating-agents).  

**I'm not sure how to access the file on a server.**  
You'll need connect to the server via SSH to run the command - see [our guide](../getting-started/#running-commands) here.