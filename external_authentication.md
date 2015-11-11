# User authentication

Xen Orchestra support various type of user authentication, internal or even external thanks to the usage of [Passport library](http://passportjs.org/).

## Built-in

This method is the default one. Creating a user is very simple:

1. Go into the Settings view, select "Users"
2. You can create a *user* or an *admin*, with his password (or generate one)

By default, a *user* won't have any permission. At the opposite, an *admin* will have every rights.

## LDAP

XO currently support connection to LDAP directories, like *Open LDAP* or *Active Directory*.

To configure your LDAP, go need to go in the plugin section in "Settings":

![LDAP plugin setting]()

If you don't find the LDAP plugin in the list, be sure to have it displayed in your Xen Orchestra configuration (in `/etc/xo-server/config.yaml`):

```
plugins:

  auth-ldap:
```

If it's not the case, don't forget to restart the service after your modification, with `systemctl restart xo-server.service`.