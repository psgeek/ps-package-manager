# Design For Phase 1
* Phase 1 will pull projects from GitHub.  
  - It will not use GitHub Cloning or allow two-directional code migration.
  - The core migration is simply a download of the App Designer file project (one directory, with an INI and XML file).
  - A zip version of the App Designer project may be utilized.  TBD.
* Phase 2 will use GitHub Cloning to take full advantage of GitHub's versioning.  
  - Project files may need to be converted from App Designer objects to a text based directory structure, where code can be seen easily in a directory hierarchy, and thus cloned/synced to/from GitHub.
  - Once a project is ready for a public release, the text-based directory will be imported into App Designer, and an official App Designer project will be exported using the standard methods (Copy to File).
### Quick Definitions
* The term *App Designer* represents PeopleTools' *Application Designer*.
* The term *project* might represent an App Designer *project*, or a GitHub *Repository*.
* The term *PackMan* is short for this repository: *PeopleSoft Package Manager*.
* The term *host system* represents the *PeopleSoft development environment* that PackMan is running in.
### Actions
* Load the list of available GitHut App Designer projects, when the PackMan page first loads.
* Allow a compare for any project listed on the PackMan page.
* Allow a project to be installed.
### Tasks
Some of these tasks will be combined together to form a single action (for the list above).  **Group** represents the priority/order needed for the project, though different people can work ahead on Group 2 or 3.  Once Group 1 is complete, we'll have a working proof of concept.
* [ ] Download the Project files from GitHub to a folder on the host system's server. **Group 1**
  - :+1: First test is successful.  Was able to use Windows Command Prompt to download, using curl.
  - Next: Need to code into App Engine, and test on Windows and Linux.
  - May run into issue with PUM not being able to pull from Internet.
```
Examples using curl to retrieve GitHub files, without cloning.
curl https://github.com/psgeek/ps-process-monitor-2/archive/master.zip --location --insecure --show-error --silent --output sample.zip
curl https://github.com/psgeek/ps-process-monitor-2/raw/master/Z_PSGEEK_PROCESS_MONITOR_2.7.1.zip --location --insecure --show-error --silent --output sample.zip
```
* [ ] Allow import of project into host system. **Group 1**
  - Should be able to leverage psidex work already done with SQL Alters.
* [ ] Allow SQL Build/Alters/Create Views to be done on the installed project. **Group 1**
  - :+1: First test is successful.  Was able to run a SQL Build on a project, in Linux, using PSIDEX.
  - For now, we'll use a customized version of the SQL Build config file, called pspm.cfg.
* [ ] Get List of all active/approved GitHub App Designer projects, for possible download. **Group 2**
* [ ] Allow an App Designer compare to be done against the host system. **Group 2**
* [ ] Determine if the GitHub list of projects are already installed in the host system. **Group 3**
* [ ] List any pending updates for prior installed GitHub projects. **Group 3**
* [ ] Allow user to specify different Build options. **Group 3**
* [ ] Create SVG icon for Portal Structure and Content Fluid Icon. **Group 3**
