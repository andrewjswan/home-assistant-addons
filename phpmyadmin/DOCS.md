# phpMyAdmin Add-on

phpMyAdmin is a database administration tool for MariaDB & MySQL. Frequently
used operations (managing databases, tables, columns, relations, indexes,
users, permissions, etc) can be performed via the user interface,
while you still have the ability to directly execute any SQL statement.

## Installation

Add the repository URL under **Supervisor → Add-on Store** in your Home Assistant front-end:

    https://github.com/andrewjswan/phpmyadmin-addon/

1. Click the "Install" button to install the add-on.
1. Start the "phpMyAdmin" add-on.
1. Enjoy the add-on!

## Configuration

**Note**: _Remember to restart the add-on when the configuration is changed._

Example add-on configuration:

```yaml
log_level: info
```

**Note**: _This is just an example, don't copy and paste it! Create your own!_

### Option: `host`

IP Address or Hostname of the SQL server. If not specified, the local MariaDB add-on is used.

### Option: `port`

SQL server port, default 3306.

### Option: `username`

The Username for authorization in the SQL server.

### Option: `password`

The Password for authorization in the SQL server.

### Option: `upload_limit`

By default, the size limit for uploads (for operations such as imports) is set to
64MB. This can be increased with this option, for example, `100` would be 100MB.

### Option: `log_level`

The `log_level` option controls the level of log output by the addon and can
be changed to be more or less verbose, which might be useful when you are
dealing with an unknown issue. Possible values are:

- `trace`: Show every detail, like all called internal functions.
- `debug`: Shows detailed debug information.
- `info`: Normal (usually) interesting events.
- `warning`: Exceptional occurrences that are not errors.
- `error`: Runtime errors that do not require immediate action.
- `fatal`: Something went terribly wrong. Add-on becomes unusable.

Please note that each level automatically includes log messages from a
more severe level, e.g., `debug` also shows `info` messages. By default,
the `log_level` is set to `info`, which is the recommended setting unless
you are troubleshooting.

## Support

Got questions?

You could also [open an issue here][issue] GitHub.

## Authors & contributors

The original setup of this repository is by [Andrew J.Swan][andrewjswan].

Addon based on offical [Home Assistant Community Add-on: phpMyAdmin][phpmyadmin] by [Franck Nijhof][frenck].

## License

MIT License

Copyright (c) 2024 Andrew J.Swan

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[addon-badge]: https://my.home-assistant.io/badges/supervisor_addon.svg
[addon]: https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_phpmyadmin&repository_url=https%3A%2F%2Fgithub.com%2Fandrewjswan%2Faddon-phpadmin
[andrewjswan]: https://github.com/andrewjswan
[issue]: https://github.com/andrewjswan/phpmyadmin-addon/issues
[frenck]: https://github.com/frenck
[phpmyadmin]: https://github.com/hassio-addons/addon-phpmyadmin