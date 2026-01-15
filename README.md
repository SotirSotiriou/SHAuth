# SHAuth
Modrinth: https://modrinth.com/mod/shauth

# Usage
This mod provides **a more advanced way to protect your server**. It is used on cracked servers in order to prevent account stealing and player coordinate leakage.

# How it works
When a player tries to connect to a server, SHAuth contacts the server and **verifies** that the connecting player provides a valid key tied to their username. If the key is valid, the connection proceeds, otherwise the player is **kicked**.


![Kick Message](https://cdn.modrinth.com/data/cached_images/c3151f943dcad591d1d27ab08fea8094f7b6671f_0.webp)


# What it safeguards against
- In cracked servers (online-mode=false) anyone can pick any username and impersonate another player. SHAuth **prevents attackers from joining as someone else**.
- Most log-in systems require you to first connect to the server and then log-in. This process allows an attacker to access information like the player's cordinates, which can be frustrating in competitive servers. However, SHAuth **requires valid credentials** before granting access.


# How to use it
1. An operator first creates a key tied to your account by doing **/shauth authorize \<username>**.
2. The player enters the key in in the server's properties menu under the server address.


![Add Server Screen](https://cdn.modrinth.com/data/cached_images/5358d5e24c4e12c0d8562e80022e98085a4b15ca.png)


# Commands
- **/shauth authorize \<username>** - Assigns a key to a player and authorizes them.
- **/shauth unauthorize \<username>** - Revokes authorization for a player.
- **/shauth reset \<username>** - Resets the key associated with a player (useful if the key gets leaked).
- **/shauth list** - Displays authorized users.
