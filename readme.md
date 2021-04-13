# How to do use this repository?
1. Use git clone
2. Copy the jar file from source
3. Create a docker file
3.1 Select a valid, official base image
3.2 Prepare your ports
3.3 Prepare your application folder
3.4 Define your build image
3.5 Prepare your steps for the build (copy, modify, etc.)
3.7 Define your final image
3.8 Copy the final build to the final image using base and final image
3.9 Decide your execution point (CMD vs. ENTRYPOINT)

4. Build the docker image (incl. tag): docker build . -t "<your-personal-tag-name>"
5. Start the docker container: docker run --restart always -p 5000:80 -p 5001:443 <your-personal-tag-name>
=> (-p=Ports, --restart always=Troubleshooting, self-healing)
=> -p <port-on-host:port-IN-container>, <your port on host machine>:<your above defined exposed port in the container>
6. Open a second cmd/powershell: docker logs --follow --details <your-personal-tag-name>
=> You see the logs from the current started container
7. Enter the URL "http://localhost:<your port on host machine>/" in your browser
=> Use Firefox for none SSL connection, use Chrome for HTTPS/SSL connection
