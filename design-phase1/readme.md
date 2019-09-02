# Design For Phase 1
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
Some of these tasks will be combined together to form a single action (for the list above).  **Group** represents the priority/order needed for the project, though different people can work ahead on Group 2 or 3.
* [ ] Get List of all active/approved GitHub App Designer projects, for possible download. **Group 2**
* [ ] Determine if the GitHub list of projects are already installed in the host system. **Group 3**
* [ ] List any pending updates for prior installed GitHub projects. **Group 3**
* [ ] Download the Project files  from GitHub to folder on the host system's server. **Group 1**
* [ ] Allow an App Designer compare to be done against the host system. **Group 2**
* [ ] Allow import of project into host system. **Group 1**
* [ ] Allow SQL Build/Alters/Create Views to be done on the installed project. **Group 1**
  - :+1: First test is successful.  Was able to run a SQL Build on a project, in Linux, using PSIDEX.
* [ ] Allow user to specify different Build options. **Group 3**
* [ ] Create SVG icon for Portal Structure and Content Fluid Icon. **Group 3**
