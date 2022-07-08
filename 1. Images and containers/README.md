# Problem

Dockerize BOTH apps - the Python and the Node app.

**1 - Create appropriate images for both apps (two separate images!). HINT: Have a brief look at the app code to configure your images correctly!**

Inside the respective project's folder, execute the command:

``docker build .``

**2 - Launch a container for each created image, making sure, that the app inside the container works correctly and is usable.**

NODE APP: ``docker run --rm -d -p 3000:3000 [image_id]``

PYTHON APP: ``docker run --rm -it [image_id]``

**3 - Re-create both containers and assign names to both containers.Use these names to stop and restart both containers.**

NODE APP: [ADD ANSWER HERE]

PYTHON APP: [ADD ANSWER HERE]

**4 - Clean up (remove) all stopped (and running) containers, clean up all created images.**

The --rm flag can be used to remove a container once it is stopped. Otherwise each container must be removed using ``docker rm [container_name] [container_name2]`` and so on.

**5 - Re-build the images - this time with names and tags assigned to them.**

NODE APP: [ADD ANSWER HERE]

PYTHON APP: [ADD ANSWER HERE]

**6 - Run new containers based on the re-built images, ensuring that the containers are removed automatically when stopped.**

As stated on the question 4, the ``--rm`` flag can be used to remove a container once it is stopped.