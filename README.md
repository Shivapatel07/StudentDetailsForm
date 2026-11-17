# Question 10 – Student Details Form

## Run without Docker
Open `index.html` in a browser.

## Docker
```bash
docker build -t student-form .
docker run -d -p 8080:80 --name student-form-container student-form
```
Open `http://localhost:8080`.

## Jenkins
Create a Pipeline or Freestyle job connected to this GitHub repository. For a Pipeline job, select **Pipeline script from SCM**, choose Git, enter the repository URL, and set Script Path to `Jenkinsfile`. Ensure the Jenkins agent has Docker installed and permission to run it.

## GitHub
```bash
git init
git add .
git commit -m "Add student details form"
git branch -M main
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git push -u origin main
```
