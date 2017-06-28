# java-container

## Project setup

* Docker for Windows (Shared C drive)
* Git Bash (Use Windows' default console window)
* Eclipse Che

### Clone the project into your workspace...
```
$ mkdir /c/myworkspace
$ cd /c/myworkspace
$ git clone https://github.com/ivvarga/java-container.git
```

### Start Eclipse Che + workspace.
```
$ docker run -it --rm -v //var/run/docker.sock:/var/run/docker.sock -v ///c/myworkspace/java-container/.che/cli:/data -v ///c/myworkspace/java-container:/chedir eclipse/che:5.13.0 dir up
INFO: (che cli): 5.13.0 - using docker 17.06.0-ce-rc5 / docker4windows
INFO: (che dir): Starting Eclipse Che silently
INFO: (che dir): Eclipse Che will be available at http://localhost:8080 (it's running but configuration is still in progress)
INFO: (che dir): Workspace exists from a previous start
INFO: (che dir): Workspace booting...
INFO: (che dir): Using existing ssh key
INFO: (che dir): Workspace booted and ready for development
INFO: (che dir): Connect to http://localhost:8080/dashboard/#/ide/che/local
```
*Open the IDE:* http://localhost:8080/dashboard/#/ide/che/java-container

### Close the project creating a snapshot of the workspace...
```
$ docker run -it --rm -v //var/run/docker.sock:/var/run/docker.sock -v ///c/myworkspace/java-container/.che/cli:/data -v ///c/myworkspace/java-container:/chedir eclipse/che:5.13.0 dir down
INFO: (che cli): 5.13.0 - using docker 17.06.0-ce-rc5 / docker4windows
INFO: (che dir): Search for a running Eclipse Che...
INFO: (che dir): Found running Eclipse Che at http://localhost:8080
INFO: (che dir): Stopping Eclipse Che...
INFO: (che dir): Eclipse Che instance successfully stopped
```
