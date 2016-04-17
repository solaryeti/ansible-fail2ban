# Ansible - Fail2ban
## Description

Ansible role for installing intrusion protection with [fail2ban](fail2ban.org).

The role currently supports using fail2ban to protect apache, postfix, dovecot, and squid.

## Compatability

This role has been developed for use with *openSUSE* and has been tested against ansible 1.9.x.

## Variables

```yaml
---
# Apache protection
include_apache: false
apache_logpath: /var/log/apache*/*error_log

# Postfix, Dovecot protection
include_mailserver: false
mail_logpath: /var/log/mail

# Squid protection
include_squid: false
squid_logpath: /var/log/squid/access.log

# General fail2ban settings
default_bantime: 86400
fail2ban_email: user@example.com     # Used for notifications
```

For full details see `defaults/main.yml`.

## Contributors

Feel free to contribute by sending pull requests.

## License

This role is licensed under a BSD-style license. See LICENCE for details.
