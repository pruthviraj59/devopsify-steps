# devopsify-steps
**steps to implement while deploying the code to the cluster**

- Dont directly start with containerizing the app/code, 1st you need to understand the project and check the code locally before containerizing it
1. clone the code from github
2. build the application (as the app is written in go lang, you can use go build -o main (this can be any name) .)  If you dont have go lang, need to install and add it to the path
3. you will get a binery(executable package) called name. you can execute that binery by ./name in terminal.
4. check the website using http://localhost:8080/courses.
5. Create a docker file using vs code (multistage build)
6. after creating the image, build the image using docker build -t pruthvi59/go-web-app:v1 .
7. docker run -p 8080:8080 to create the container
8. the container will be created, to checkit go to browser and seach for http//localhost:8080/courses
9. always check the bineries
10. Your container is Linux (ubuntu,debian,distroless) → it can only run Linux binaries.
You built a Windows binary → mismatch → container crashes.
✅ Multi-stage Dockerfile fixes it by building Linux binaries inside Docker itself.
11. to run the container continuosly, use -d (detached mode)
12. you can also use docker-compose (using docker-compose.yml file)
13. 🔹 Why this is better
You don’t need to type long docker run commands.
Restart policy (unless-stopped) is built in.
You can easily scale services later (databases, caches, multiple containers).
Great step towards production setups (Compose → Swarm → Kubernetes).
14.then push the image to dockerhub (docker push imagename)
15. now create a deployment.yaml file using vs code
