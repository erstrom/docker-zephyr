=====================
Zephyr docker dev env
=====================

Installation
++++++++++++

See the official docker documentation for a general overview of docker
and how to install:

https://docs.docker.com/engine/installation/linux/

Build and launch docker image
+++++++++++++++++++++++++++++

Build the docker image, create a container and launch it:

.. code-block:: bash

	git clone https://github.com/erstrom/docker-zephyr.git
	cd docker-zephyr
	./docker-build.sh
	./docker-run.sh

``docker-build.h`` and ``docker-run.sh`` should only be run once unless several
containers are needed. In this case ``docker-run.sh`` must be modified with
different ``--name`` options for each container.

``docker-run.sh`` wraps ``docker run`` and adds a few options for convenience.

Since ``docker-run.sh`` adds the ``-i`` and ``-t`` options, the container will be
launched in interactive mode. In order to leave the interactive session and
stop the running container, type ``exit``

Launch an already created container
+++++++++++++++++++++++++++++++++++

``docker-start.sh`` is used to launch an already created container:

.. code-block:: bash

	cd docker-zephyr
	./docker-start.sh
