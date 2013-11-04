Installing StriderCD
====================

Dependencies
------------

Strider requires Node 0.10.x or higher and a MongoDB database. You can get node.js for your platform at http://nodejs.org. You can get
MongoDB for your platform at http://mongodb.org.

We assume you have a MongoDB server running locally on your machine in the interests of simplicity. Of course, you can use a remote or cloud-hosted MongoDB just as easily.


Latest Stable Version
---------------------

The latest version of Strider in NPM is always a stable version. Once you have Node.JS on your system, you can install the 
most recent stable version of Strider system-wide with the following command::

    npm install -g strider

Now you should have a ``strider`` executable in your ``$PATH``. 


Latest Development Version 
--------------------------

The very latest version of Strider is available on Github. While we strive to
keep Strider as stable as possible, this should be considered development or
pre-release code.

First clone the repository from Github::

    git clone https://github.com/Strider-CD/strider.git

Next go into the ``strider`` directory and install strider system-wide::

    cd strider
    npm install -g

Now you should have a ``strider`` executable in your ``$PATH``.

Adding Users
------------

Strider isn't much use without any user accounts. You will want to create at least one admin user to manage your instance::

  strider addUser

This command will walk you through creating a new user. If you already know an email and password, you can also pass them directly. For example to create a new user with email ``foo@example.com`` and password ``supersecret`` with admin privileges::

  strider addUser -l foo@example.com -p supersecret -a


Cloud-hosted or Remote MongoDB
------------------------------

If you don't want to run a local MongoDB, you can also use a cloud-hosted
database, such as a free one provided by MongoLab. Using a cloud-hosted
database for Strider can be advantageous because you can easily outsource
backups, upgrades and other operations tasks which aren't generally fun.

Additionally, a cloud-hosted MongoDB database should be available from anywhere.

Of course, you might already have your own MongoDB set up in your environment, but just not on your local machine.

Strider can be configured to use a remote MongoDB database with the ``DB_URI`` environment variable. For example::

    DB_URI=mongodb://username:supersecret@mongodb.example.com/strider npm start


