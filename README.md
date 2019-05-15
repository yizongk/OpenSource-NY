# What is OpenSource NY?
  OpenSourceNY App(OSNY) is a tool that tracks contributions made by a participant, and then rank the participants using a leaderboard-esque ranking system. Specifically, it is a tool designed to track participation in [Open Source NYC](https://www.meetup.com/Open-Source-NYC/)'s open source contribution challenge held over the summer in which participants are tasked to contribute, such as opening a pull request or issue, to open source projects in any way.

  In other terms, the tool should let participants register to join the challenge or send an email of interest, record activity metrics, and rank participants using a leaderboard.


  For any users that opts in, given a GitHub repo and GitHub username, the software will keep track of stats for that users in relation to the GitHub repo.

# Features (including stats that we will keep track of)
  - Listing Pull Requests from a specified Github Repo.
  - WIP

# Dependency
* npm 3.5.2 (All the other sub dependencies are in various package.json files, doing an 'npm install' on that directory will install the dependencies)

  For Ubuntu 18.04.2 LTS bionic:
```shell
sudo apt-get update --yes
sudo apt-get install npm --yes
sudo apt-get install postgresql postgresql-contrib
```


# How to run

  1. In one terminal, run this to get the server running (only need to do npm install on your first time, to install all the node_modules):
  ```bash
  cd src/myapp/server
  npm install   
  npm start
  ```
  2. In a second terminal, run this to get the front end running (only need to do npm install on your first time, to install all the node_modules):
  ```bash
  cd src/myapp/client
  npm install
  npm start
  ```

  3. Now go to your browser and open http://localhost:3000/
    Voila!

  *NOTE*: When npm start on REACT, you maybe run into this error:
  ```
  fs.js:1384
    throw error;
  ``` 
  To fix:  [Reference](https://github.com/facebook/jest/issues/3254)

  * add 'fs.inotify.max_user_watches=20000' without the single quotes into your /etc/sysctl.conf on the very last line. Change the number to however much you want. The error aboves results from the number being too small, so change it to a big enough number. How big? I don't know, depends on how much files you have in your REACT App.
  * After you edit that file, run the following to load in the [sysctl](https://linux.die.net/man/8/sysctl) setting from /etc/sysctl.conf
  ```shell
  sudo sysctl -p
  ``` 

# How to contribute
  PLEASE FORK, and follow a proper git work flow
  when you have a feature done, do a PR
  PLEASE DO NOT MAKE DIRECT EDITS TO THIS REPO

  If you see any bugs, on documentations, codes, etc please open an issue describing the bug. Thanks!

  Refer to [CONTRIBUTING.md](./CONTRIBUTING.md)


# For start(this section is for initial development of this project, will be removed from this README.md once we have a base to build on top of)
  Here are the 4 features that we would like to have as a base to work off on:

  * User opt in feature
    - Sign up form on the front end
    - connect to back end and fill in to data base
      - GitHub username
  * Base on a project-repo and GitHub username, will keep track of stats
    - Numbers of PR
    - Numbers of merged PR
  * Responsive Website
    - For Mobile
    - For Desktop
  * Data visualization of the stats that we will keep track of
  
<h2>OpenSourceNY App</h2>

  Made for [OSI (Open Source Initiative)](https://opensource.org/) and [Open Source NYC](https://www.meetup.com/Open-Source-NYC/). Idea was originally by Professor Jessie Contour of Hunter College, contour.j@gmail.com.

