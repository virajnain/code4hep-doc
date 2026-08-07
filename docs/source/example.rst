Getting started with code4hep
=============================


Initial setup
~~~~~~~~~~~~~~~~~~~~

Once you are logged onto the cluster, clone the c4h-dist repository:

.. code-block:: bash

   git clone https://github.com/c4h-dist.git

Next, build the container using podman:

.. code-block:: bash

   cd c4h-dist
   podman build --format docker -t code4hep-build -f Dockerfile . 

Once the container is built, run it using podman:

Replace ``<container_name>`` with a name of your choice.

.. code-block:: bash

   podman run -it <container-name>

Once you are inside the container, activate the spack environment:

.. code-block:: bash

    source /opt/spack/share/spack/setup-env.sh
    spack env activate code4hep_env

Now code4hep is ready for use!

General tips
~~~~~~~~~~~~~~~~~~~~
To leave the container simply use the command ``exit``

To reenter the container run:

.. code-block:: bash

    podman start -ai <container_name>