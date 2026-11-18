# Node Web App - DevOps Practical Work

This project demonstrates the Git, branching, pull-request, and Docker activities
from Practical Work #2 and Practical Work #3.

## Run locally

```powershell
npm install
npm start
```

Open `http://localhost:3000` to see `Hello, World!`, or
`http://localhost:3000/about` to see `About Page`.

## Git workflow

```powershell
git init
git add .
git commit -m "Initial commit: Add basic Node.js web app"
git branch -M main
git checkout -b feature/add-route
git add index.js
git commit -m "Add /about route to web application"
git checkout main
git merge --no-ff feature/add-route -m "Merge /about route feature"
```

To publish to GitHub, create an empty repository and run:

```powershell
git remote add origin https://github.com/YOUR_USERNAME/node-web-app.git
git push -u origin main
git push -u origin feature/add-route
```

Then create a pull request from `feature/add-route` into `main`.

## Docker workflow

```powershell
docker build -t node-web-app .
docker run -d --name node-web-app-container -p 3000:3000 node-web-app
curl http://localhost:3000
docker ps
docker stop node-web-app-container
docker rm node-web-app-container
```
