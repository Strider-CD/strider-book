Introduction
============

What Is Strider
---------------

Strider is an Open Source Continuous Integration and Deployment platform
written in JavaScript/Node.JS and using MongoDB for persistance.  It is
released under the BSD license. While similar conceptually to systems such as
Travis and Jenkins, Strider is designed to be easy to setup, use, and
customize.


What Is Continuous Integration
------------------------------

Continuous Integration (a.k.a. CI) is a software engineering process.  It can be
defined as running an automated test suite on every commit to a software project
and notifying on success and failure. 

CI is useful because it greatly increases the feedback developers receive on
each commit, and the health and well-being of the software overall. It is
amazing how many bugs can be found which otherwise would remain covered due to
particulars of development environments.

What Is Continnuous Deployment
------------------------------

At a high level, Continuous Deployment
(a.k.a. CD) extends Continuous Integration to include automated deployment 


Strider Philosophy
------------------

We believe that Continuous Integration and Continuous Deployment processes
improve the quality and reliability of software. Furthermore, these processes 

Features
--------

Strider has the following major features:

- Stylish dashboard displaying the current and recent test and deploy status of
  each project.

- Development teams via "collaborators". Give other users read-only access or
  full admin rights.

- Public projects. Let the world at large see your project status dashboard!
  Public projects may be browsed by anonymous users, but not triggered nor
  configured. Great for Open Source projects. See Strider's public CI dashbaord
  at https://public-ci.stridercd.com.

- Github, Github Enterprise, BitBucket, GitLab and more. Intuitively add
  projects for CI and CD with only a few clicks.

- Branches. Each VCS branch may be configured independently, including with
  different deployment configuration. Use this to create powerful workflows.
  For example, "master" branch may only deploy to production with a manual
  trigger while "testing" branches deploy to QA automatically on each
  successful test run.

- Pull Requests. GitHub pull requests can be automatically tested when they are
  opened, with test result status sent back to GitHub to mark the PR. For
  security reasons, this is only enabled for specific users which you
  whitelist.

- Script each phase of each project from the web or config file. Custom prepare, test and deploy scripts
  easily enable integration with your specific language, environment and existing automation.

- Out-of-box support for Node.JS and Python projects. Other languages / environments can be supported with thirdparty plugins
  or custom scripts.

- Sauce Labs integration. Easily configure Sauce credentials and select os/browser combinations via Strider's web UI. Strider will
  even manage the Sauce Connect proxy for you.


