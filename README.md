# java-container

## Project setup

* Docker for Windows (Shared C drive)
* Git Bash (Use Windows' default console window)
* Eclipse Che

### Clone the project your workspace...
```
mkdir /c/myworkspace
cd /c/myworkspace
git clone https://github.com/ivvarga/java-container.git
```

### Start Eclipse Che + workspace.
```
docker run -it --rm -v //var/run/docker.sock:/var/run/docker.sock -v ///c/myworkspace/java-container/.che/cli:/data -v ///c/myworkspace/java-container:/chedir eclipse/che:5.13.0 dir up
```
*Open the IDE:* http://localhost:8080/dashboard/#/ide/che/java-container

### Close the project creating a snapshot of the workspace...
```
docker run -it --rm -v //var/run/docker.sock:/var/run/docker.sock -v ///c/myworkspace/java-container/.che/cli:/data -v ///c/myworkspace/java-container:/chedir eclipse/che:5.13.0 dir down
```
