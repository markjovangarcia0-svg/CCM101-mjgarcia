# Mission 4 Reflection

During this laboratory activity, I learned that containers can make application deployment much simpler compared with setting up a complete virtual machine. A virtual machine needs its own operating system, so starting one involves loading many system components before the application is ready. With Docker, the Nginx image was already packaged and I only needed a few commands to create and start the container. This made the setup process much quicker for the web server used in the activity.

The port mapping `-p 8080:80` connects two different ports. Port 80 is where the Nginx service listens inside the container, while port 8080 is the port exposed on the host. This allowed me to send a request to `localhost:8080` and receive the Nginx response from inside the container.

I also learned that stopping and removing a container are different actions. The `docker stop` command changes the running container into a stopped state, while `docker rm` removes that container. Information that exists only in the container's writable layer should not be treated as permanent storage because removing the container can delete that data.

Containerization can also support cooperation between developers and operations teams. Developers can package an application into a consistent environment, while operations teams can deploy the same image without manually installing every application dependency. This can make the movement from development to deployment more consistent.

My GitHub portfolio is becoming more useful as I add practical activities instead of only theoretical notes. This laboratory gave me another experience to document because I had to perform actual Docker commands and record the results. I also became more familiar with using Markdown to organize technical information in a way that can be viewed clearly on GitHub.
