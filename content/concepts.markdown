Concepts
==========

Container
-------------
Isolated Subsystem running on a shared host
Multiple containers can be linked.

Image
-----------
Template for Containers

Layer
-----------

Build Cache
------------
Cache will be used, iff
1) it is not invalidated
2) command equals one of current images child's commands
3) except: ADD/COPY will look at changed file hashes
4) it is not manually disabled by: ``` --no-cache=true ```

Repository
-------------


Registry
--------------
A host that serves **repositories**

Networking
---------------
Control inter-container communication
https://docs.docker.com/engine/userguide/networking/
https://docs.docker.com/engine/userguide/networking/work-with-networks/

Compose
---------------
Tool to orchestrate multiple containers.
https://docs.docker.com/compose/overview/
