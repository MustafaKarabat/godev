# Welcome to godev!

The aim of this project is to develop a premier Go language IDE hosted in a web interface. This was inspired by the way that the godoc tool uses a web UI instead of a traditional GUI.

There are certain advantages of a web UI in this case 


* Remote access through your web browser (no extra install required)
* OS independent GUI (Go has no standard cross-platform library)
* Hosted Go development environment

# The Plan

The initial sprint and prototype is complete. Future sprints will focus on improving breadth and depth of functionality.

Areas explored:

* Edit and Code Navigation
    + Use the Eclipse Orion project as a base
    + http://www.eclipse.org/orion
    + Syntax highlighting
    + File outline
    + Simple content assists
    + Markers for compile errors, todo comments, fixme comments
* Documentation
    + Go doc integration
* Build and Compile
    + Use the go build/go install commands to compile the code
    + Create console and markers for specific compile errors
* Run
    + Run and manage running Go process (output buffer, input, stop)

New areas to explore:

* Debug
    + Use the gdb/MI interface to present an interactive debugging web UI
    + [http://sourceware.org/gdb/onlinedocs/gdb/GDB_002fMI.html]([http://sourceware.org/gdb/onlinedocs/gdb/GDB_002fMI.html)
* Git Integration
    + Manage push/pull/commit/add
* RTC SCM Integration
    + Manage pending changes, check-ins, deliveries
* Go test
    + Run a package's go test suite and report back results in a table/tree
* Contextual content assist
    + Content assists based on the return value of a function call
    + Content assists based on the other functions in the current file and local GOPATH packages 

# Screenshots

![Screenshot1](https://hub.jazz.net/ccm01/service/com.ibm.team.workitem.service.internal.rest.IAttachmentRestService/repo/csid/Attachment/godev-screenshot1.png?itemId=_MwuvANtwEeKv4ph699mytQ)
Save the go file to see markers for compile errors

![Screenshot2](https://hub.jazz.net/ccm01/service/com.ibm.team.workitem.service.internal.rest.IAttachmentRestService/repo/csid/Attachment/godev-screenshot2.png?itemId=_Mx07MNtwEeKv4ph699mytQ)
Run and Debug programs from the Debug page
	
![Screenshot3](https://hub.jazz.net/ccm01/service/com.ibm.team.workitem.service.internal.rest.IAttachmentRestService/repo/csid/Attachment/godev-screenshot3.png?itemId=_MzNbQNtwEeKv4ph699mytQ)
Get content assistance using Ctrl-Space

![Screenshot4](https://hub.jazz.net/ccm01/service/com.ibm.team.workitem.service.internal.rest.IAttachmentRestService/repo/csid/Attachment/godev-screenshot4.png?itemId=_Mznq8NtwEeKv4ph699mytQ)
Use the shell to run go build or go install

![Screenshot5](https://hub.jazz.net/ccm01/service/com.ibm.team.workitem.service.internal.rest.IAttachmentRestService/repo/csid/Attachment/godev-screenshot5.png?itemId=_M0X44NtwEeKv4ph699mytQ)
Bring up godocs using the GoDoc page

# Videos
[Youtube](http://www.youtube.com/watch?feature=player_embedded&v=UTfHDbUUECg)

# Getting Started

The godev tool requires the Go SDK, which is freely available for download on golang.org 

To begin working with Go you first need to set up your GOPATH. This is a directory where all of your source code and binaries live. Pick an empty directory somewhere on your system and set the GOPATH environment variable with the path to this directory. For more details you can read the "How to Write Go Code" guide on golang.org. 

Get the source code from the latest release by running go get: "go get github.com/sirnewton01/godev"

Compile and install godev in your GOPATH by running go install: "go install github.com/sirnewton01/godev"

Run godev from the GOPATH/bin directory: "$GOPATH/bin/godev -dev"

Open up your web browser and navigate to http://127.0.0.1:2022 Note that unless you launch the server with the "-http" parameter it will be accessible only through your local machine using the "127.0.0.1" address. You can begin a new godev project using the "New -> Folder" menu near the top of the screen.

If you have ideas for enhancements or find defects please Raise a Task on JazzHub (account required): [https://hub.jazz.net/ccm01/web/projects/sirnewton%20%7C%20godev#action=com.ibm.team.workitem.newWorkItem&type=task&ts=13725284879510](https://hub.jazz.net/ccm01/web/projects/sirnewton%20%7C%20godev#action=com.ibm.team.workitem.newWorkItem&type=task&ts=13725284879510)

Happy Go hacking! 
