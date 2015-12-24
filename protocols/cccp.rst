Consensus Command and Control Protocol (CCCP)
*********************************************

The **Consensus Command and Control Protocol** (CCCP) is the native command
protocol for Conreality nodes.

Overview
========

CCCP is an asynchronous application protocol built on the transport-layer
User Datagram Protocol (UDP) running on IPv4 and IPv6 networks.

The use of UDP enables flexible asymmetric network topologies, where
requests and responses may potentially travel by wholly different routes.

Port Number
===========

The UDP protocol port is 1984.

Message Format
==============

Messages are snippets of Lua code.

Commands
========

* **Device Control**: enable, disable, toggle
* **Motion Control**: hold, pan, tilt
* **Motion Planning**:
* **Object Tracking**: track
* **Swarm Membership**: join, leave

Command Reference
=================

abort
^^^^^

disable
^^^^^^^

Disables a device.

In a natural-language interface, suggested aliases for this command include:
`stop`.

enable
^^^^^^

Enables a device.

In a natural-language interface, suggested aliases for this command include:
`start`.

fire
^^^^

hold
^^^^

join
^^^^

leave
^^^^^

pan
^^^

Rotates the FOV in the horizontal plane.

ping
^^^^

resume
^^^^^^

tilt
^^^^

Rotates the FOV in the vertical plane.

toggle
^^^^^^

Toggles a device.

track
^^^^^
