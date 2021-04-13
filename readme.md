# Recommendations - What should you know before?
1. You should be familar with git commands
2. You should use git commits for your steps
  - => Use granular (baby) steps for the exercise
3. You should be familar with docker commands
  - => At least you should know how to interprete the docker docs (https://docs.docker.com/) :) 
4. You should have done the following exercises with git:
  - => https://learngitbranching.js.org/?locale=de_DE


# How can you achieve the requirements?
Easy way to learn git without breaking your project:
  - => https://learngitbranching.js.org/?locale=de_DE
Docker docs:
  - => https://docs.docker.com/

# How to do use this repository?
1. Use git clone
2. Copy the jar file from source
3. Create a docker file
  - Select a valid, official base image
  - Prepare your ports
  - Prepare your application folder
  - Define your build image
  - Prepare your steps for the build (copy, modify, etc.)
  - Define your final image
  - Copy the final build to the final image using base and final image
  - Decide your execution point (CMD vs. ENTRYPOINT)

4. Build the docker image (incl. tag): docker build . -t "[your-personal-tag-name]"
5. Start the docker container: docker run --restart always -p 5000:80 -p 5001:443 <your-personal-tag-name>
  - ==> (-p=Ports, --restart always=Troubleshooting, self-healing)
  - ==> -p [port-on-host:port-IN-container], [your port on host machine]:[your above defined exposed port in the container]
6. Open a second cmd/powershell: docker logs --follow --details [your-personal-tag-name]
  - ==> You see the logs from the current started container
7. Enter the URL "http://localhost:[your port on host machine]/" in your browser
  - ==> Use Firefox for none SSL connection
  - ==> Chrome is using HTTPS/SSL connections by default
