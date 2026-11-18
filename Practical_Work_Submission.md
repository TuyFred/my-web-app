# DevOps Practical Work Submission

## Practical Work #2: Git repository

The Node.js application is stored in this folder and tracked with Git. The
`.gitignore` file excludes `node_modules`, environment files, and npm logs.
The repository is initialized locally, committed, renamed to `main`, and is
ready to be connected to a GitHub repository.

Expected local verification:

```powershell
git status
git log --oneline
node index.js
```

The application is available at `http://localhost:3000`.

## Practical Work #3, Activity 1: Branch and merge

The feature branch is named `feature/add-route`. It adds the `/about` route
without changing the main branch until the feature is reviewed and merged.
The merge is performed with:

```powershell
git checkout main
git merge --no-ff feature/add-route -m "Merge /about route feature"
```

## Practical Work #3, Activity 2: Pull request

Create a pull request with:

- **Title:** Add /about route to web application
- **Base branch:** `main`
- **Compare branch:** `feature/add-route`
- **Description:** Added a new `/about` route that returns `About Page`.

Suggested review comment: “Please use consistent indentation in the route
handlers.” After checking the formatting, push any correction, approve the
pull request, and merge it. Copy the merged pull-request URL and capture the
merged status for submission.

### 50-100 word documentation

I created the `feature/add-route` branch to add an `/about` endpoint without
changing the stable `main` branch. The route was tested locally and committed
with a descriptive message. During review, I checked the route formatting and
confirmed that the response is returned correctly. The feature branch was then
reviewed, approved, and merged into `main`. This workflow demonstrates
isolated development, peer review, traceable commits, and safe integration of
web-application changes.

## Practical Work #3, Activity 3: Docker

The `Dockerfile` uses the official Node.js 18 Alpine image, installs the
dependencies, copies the application, exposes port 3000, and starts the server.
After installing Docker Desktop, run the Docker commands in `README.md`.
Verify the response with `curl http://localhost:3000` and capture the output
together with `docker ps`.

## Submission checklist

- [ ] GitHub repository URL
- [ ] `git log --oneline` screenshot
- [ ] Feature branch screenshot
- [ ] Pull-request URL and merged-status screenshot
- [ ] `docker images` screenshot
- [ ] `docker ps` screenshot
- [ ] Browser or `curl` response screenshot
