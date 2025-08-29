# devopsify-steps
**steps to implement while deploying the code to the cluster**

- Dont directly start with containerizing the app/code, 1st you need to understand the project and check the code locally before containerizing it
1. clone the code from github
2. build the application (as the app is written in go lang, you can use go build -o main (this can be any name) .)  If you dont have go lang, need to install and add it to the path
3. you will get a binery(executable package) called name. you can execute that binery by ./name in terminal.
4. check the website using http://localhost:8080/courses.
5. Create a docker file using vs code
