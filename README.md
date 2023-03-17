# Description
Libraries used by modules can generate crucial information for troubleshooting (or even their normal functioning).
This module can redirect logs from certain libraries (based on classpath) to Mendix lognodes.

It leverages the Log4j framework and includes a slf4j to log4j adapter.
 
# Typical usage scenario
- Developing or troubleshooting a module or connector which uses a library which logs information through one of the mentioned frameworks. 
- Capture inner working of a library in your application's log to ensure its working.
 
# Features and limitations
Redirect logging messages from one of the following frameworks to a Mendix lognode:
- Log4j
- Slf4j
- apache-common
 
# Dependencies
This module will typically be a dependency of other modules.

# Installation
## Fresh installation
Download the module from the App Store

## Upgrade notice
Before downloading a new version of the module from the App Store, remove all the jar files having a corresponding `LibraryLogging.RequiredLib` in their filename.
These are typically files starting with:
- `log4-api`
- `log4j-core`
- `log4j-jcl`
- `log4j-slf4j`
- `slf4j-api`

# Configuration
Attach the AfterStartup microflow from the _USE_ME folder to your startup flow.

# For module developers
Use the action AddLibraryLogListener redirect all log messages from a certain classpath to a Mendix log node.
Use the action SetRootLevel to log everything to a Mendix lognode (recommended for developing purposes only)
 
# Known bugs
Let me know and I'll add them to the list.