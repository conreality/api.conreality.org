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

.. code-block:: lua

   abort {mission}

disable
^^^^^^^

Disables a device.

In a natural-language interface, suggested aliases for this command include:
`stop`.

.. code-block:: lua

   disable {device=led01}

enable
^^^^^^

Enables a device.

In a natural-language interface, suggested aliases for this command include:
`start`.

.. code-block:: lua

   enable {device=led01}

fire
^^^^

.. code-block:: lua

   fire {device=laser, seconds=3.0}

hold
^^^^

.. code-block:: lua

   hold {}

join
^^^^

.. code-block:: lua

   join {swarm=perimeter}

leave
^^^^^

.. code-block:: lua

   leave {swarm=perimeter}

pan
^^^

Rotates the FOV in the horizontal plane.

.. code-block:: lua

   pan {direction=left, degrees=90.0}

pan to
^^^^^^

Rotates the FOV in the horizontal plane.

.. code-block:: lua

   pan_to {degrees=270.0}

ping
^^^^

.. code-block:: lua

   ping {ipv4='8.8.8.8'}

resume
^^^^^^

.. code-block:: lua

   resume {}

tilt
^^^^

Rotates the FOV in the vertical plane.

.. code-block:: lua

   tilt {direction=up, degrees=45.0}

tilt_to
^^^^^^^

Rotates the FOV in the vertical plane.

.. code-block:: lua

   tilt_to {degrees=45.}

toggle
^^^^^^

Toggles a device.

.. code-block:: lua

   toggle {device=laser}

track
^^^^^

.. code-block:: lua

   track {object=objects[42]}
