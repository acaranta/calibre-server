calibre-server (docker)
=====================

Docker container with calibre server installed from git source 

Getting the image
-----------------
You can pull it from ``https://index.docker.io/u/acaranta/calibre-server/`` or clone this repo and build it.

Using your library
------------------
This container exposes the volume **/calibre-lib** and the port **8080**
By default the server is expecting user=calibre, password=calibre


To allow calibre to run **your library** you have to **mount it as a volume** with ``-v /your/library/location:/calibre-lib``


Runnining the container
------------------------

    docker run -p 80:8080 -v <your-lib-dir>:/calibre-lib --name calibre-server acaranta/calibre-server

You can pass different user/password to calibre-server:

    docker run -p 80:8080 -e USER=<user> -e PASS=<pass> -v <your-lib-dir>:/calibre-lib --name calibre-server acaranta/calibre-server

