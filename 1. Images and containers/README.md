# Problem

Dockerize BOTH apps - the Python and the Node app.

**1 - Create appropriate images for both apps (two separate images!). HINT: Have a brief look at the app code to configure your images correctly!**

Inside the respective project's folder, execute the command:

``docker build .``

**2 - Launch a container for each created image, making sure, that the app inside the container works correctly and is usable.**

NODE APP: ``docker run -d -p 3000:3000 [image_id or tag]``

PYTHON APP: ``docker run -it [image_id or tag]``

**3 - Re-create both containers and assign names to both containers.Use these names to stop and restart both containers.**

We use the ``--name`` tag to give a container a name.

NODE APP: ``docker run --name node_container -d -p 3000:3000 [image_id or tag]``

PYTHON APP: ``docker run -it --name python_container [image_id or tag]``

**4 - Clean up (remove) all stopped (and running) containers, clean up all created images.**

Cleaning up the containers: All the containers can be removed using the combination of two commands:

``docker stop $(docker ps -aq)``

``docker rm $(docker ps -aq)``

The ``docker ps -aq`` will return only the ids of all the containers. Otherwise you can specify which container you want to remove passing it's name to the ``docker rm`` command.

Cleaning up all the images: just run ``docker image prune -a``

**5 - Re-build the images - this time with names and tags assigned to them.**

We use the option ``-t`` to assing a name and a tag (optionally) to the new created image.

NODE APP: ``docker build -t node-app:lastest``

PYTHON APP: ``docker build -t python-app:lastest``

**6 - Run new containers based on the re-built images, ensuring that the containers are removed automatically when stopped.**

The ``--rm`` option can be used on the ``docker run`` command to remove a container once it is stopped.