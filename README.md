# hello-world

Scala, Play Framework, Docker 

## Run server locally
```bash
sbt run
```

"Hello World" website will be available at http://localhost:9000


## Push new version to Docker Registry
- Check build.sbt:

```bash
name := "hello-world"

dockerRepository := Some("giltouroboros") // replace with your Docker repository name

maintainer in Docker := "Ouroboros <ouroboros@gilt.com>" // update your details

```
 - Commit and tag in git
```bash
git commit -a -m "Change 'Hello message'"

git tag vX.X.X
 ```
- Build Docker image and push to Docker registry

```bash
sbt docker:publish
```
