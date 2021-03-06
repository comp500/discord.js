.. include:: ./vars.rst

Role
====

Represents data for a Server Role.

--------

Attributes
----------

position
~~~~~~~~

`Number`, position of the role when viewing the roles of a server.

name
~~~~

`String`, name of the role.

managed
~~~~~~~

`Boolean`, whether Discord has created the role itself. Currently only used for Twitch integration.

id
~~

`String`, ID of the role.

hoist
~~~~~

`Boolean`, whether the role should be displayed as a separate category in the users section.

color
~~~~~

`Number`, a base 10 colour. Use ``role.colorAsHex()`` to get a hex colour instead.

server
~~~~~~

The Server_ the role belongs to.

client
~~~~~~

The Client_ that cached the role.

createdAt
~~~~~~~~~

A `Date` referring to when the role was created.

Functions
---------

serialise()
~~~~~~~~~~~

**Aliases:** `serialize`

Makes an object with the permission names found in `Permission Constants`_ and a boolean value for them.

hasPermission(permission)
~~~~~~~~~~~~~~~~~~~~~~~~~

Sees whether the role has the permission given.

- **permission** - See `Permission Constants`_ for valid permission names.

colorAsHex()
~~~~~~~~~~~~

Returns the role's colour as hex, e.g. ``#FF0000``.

mention()
~~~~~~~~~

Returns a valid string that can be sent in a message to mention the role. By default, ``role.toString()`` does this so by adding a role object to a string, e.g. ``role + ""``, their mention code will be retrieved. If the role isn't mentionable, its name gets returned.