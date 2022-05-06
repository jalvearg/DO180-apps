
  
1. Setting up a Podman Host
  - Set up RHEL 8 host with a graphical user interface.
  - Install the appropriate tools to work with Podman, Buildah and Skopeo.
  - To test the setup, run the bitnami/nginx container.

2. Working with standard images
  - Use your developer.redhat.com credentials to login to the RedHat image registries.
  - User the appropriate command to inspect the mariadb image without downloading it.
  - Download the image without running it.
  - Run the image as a container.
  - After starting it, open an interactive shell on the container and find which operating system and kernel it uses.

3. Managing images
  - Start the bitnami/nginx image using the name mynginx.
  - Add the file /tmp/hello and ensure that changes th the image are saved.
  - Save the modified image to a tar archive.
  - Restore the backup that yu previously created.

4. Managing Containers
  - Use podman to start a mysql container.
  - Ensure that this container will store files that are written to /var/lib/mysql persistently to the host directory /srv/mysql.
  - Expose the default container port on port 30306 on the localhost.

5. Using Dockerfile
  - Create a Dockerfile that will start a network scan on the local network using the Linux command nmap -sn 172.17.0.0/24 
    (make sure the network IP address matches your current container network IP address).
  - Ensure that this container image is build on a minimal RHEL-based.
  - Also make sure that the container image provides the ip, ps and ping utilities for troubleshooting.

6. Using CRC
  - Install CRC
  - Start an nginx application that is based on the bitnami/nginx application.
  - Use the command line client to verify that the application is running.

7. Running Application in OpenShift
  - Create a YAML manifest file that allows you to run an application with the name newnginx, meeting the following requirements:
      - Use bitnami/nginx image.
      - Provide access to the application using a route.
  - Ensure that a YAML file is created, but no API resources are actually added to the cluster.

8. Decoupling Information
  - Run a Pod that offers mysql services, meeting the following requirements:
    - Use a mysql image.
    - Make sure that the /var/lib/mysql directoryin the container is mounted on a Persistent Volume Claim.
    - Provide variables that are required to start the application in an efficient way.

9. Using S2I
  - Using your own GitHub account, create a GitHub repo with the name task9.
  - In the repo, copy (not fork) the content of http://github.com/sandervanvugt/sinpleapp
  - Use Source2Image to run this application in OpenShift.

10. Troubleshooting
  - Run an application in OpenShift that meets the following requirements:
    - Use the busybox image.
    - Give it the name lab10busy.
  - Use the appropriate tools to analyze why the application is not starting.
  - Fix it in such way that the application can be started.
