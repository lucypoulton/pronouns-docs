## Installation

Installing the plugin is super simple:

- Download the plugin from <https://lucypoulton.net/pronouns> - take care to choose 
  the correct file for your server platform.
- Place the downloaded plugin into your server's plugins folder.
- (Bukkit-based servers only) Optionally install PlaceholderAPI.
- Restart your server.

You're done! The plugin has a sane default configuration and will work "out of the box", 
but there are some settings you may want to change. See the next page for more info.

## ProNouns Cloud

[ProNouns Cloud](https://pn.lucypoulton.net) is a service that defines commonly used neopronouns so people don't need to
type out the entire thing every time. By default, recent versions of ProNouns (2.0.0+) will automatically and anonymously
send pronoun sets that aren't in the list back to the server, subject to manual moderation on my end. If you don't wish 
to participate in this, you can opt out from the config:

```yaml
# ProNouns Cloud-related settings
cloud:
  # Should the plugin regularly download the list of pronouns from the server and make them available to players?
  sync: true
  # Should the plugin anonymously submit unrecognised sets back to the server?
  upload: true
```

When `sync: true`, the list will be regularly downloaded from the server, and placed into a file called `pronouns.json`
at the root of the plugin's config directory. It can also be manually updated by using the command `/pn cloud sync` or by
downloading the file from <https://pn.lucypoulton.net>.

## Using MySQL

ProNouns supports MySQL to synchronise pronouns across multiple servers. 
You'll need to create a user and database for it (note this step may vary depending on your hosting provider, 
contact them if in doubt):

```sql
CREATE DATABASE pronouns;
CREATE USER pronouns@localhost IDENTIFIED BY 'a long, secure password';
GRANT ALL PRIVILEGES ON pronouns.* TO pronouns@localhost;
FLUSH PRIVILEGES;
```

Then in the ProNouns config, add your user, database and password:
```yaml
connection: 'mysql' # remember to set this!
mysql:
  host: '127.0.0.1'
  port: 3306
  database: 'pronouns'
  username: 'pronouns'
  password: 'your password here'
```

## Moderation and admin commands

To allow a player to act as a moderator, grant the permission `pronouns.admin`. This will do the following:

- Grants access to admin commands (`setother`, `clearother`, `reload`, `cloud`)
- Player is notified when a player without the bypass permission tries to use a set blocked by the filter
- Player is notified when an update becomes available

It's recommended to also grant `pronouns.bypass` to allow these players to bypass the filter in case of a false positive.