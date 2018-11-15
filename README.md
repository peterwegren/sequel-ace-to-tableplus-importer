# Sequel Pro to Table Plus Importer

An unofficial way to import existing Sequel Pro connections into TablePlus. 



## *Although a backup is created, this script is intended for use on fresh installations of TablePlus and will overwrite any existing connections.*

### Prerequisites
* [TablePlus](https://tableplus.io/)
* [Sequel Pro](https://www.sequelpro.com/)
* [Node](https://nodejs.org/) - Make sure you are on the lastest version
* NPM or Yarn

Tested and working with node v10.8.0

### Installing
Please note that this script will not bring over any passwords. You will need to add those directly in TablePlus once the import is complete.

Clone the project somewhere on your system:
```
git clone git@github.com:ashbakernz/sequel-pro-to-tableplus-importer.git
```

Navigate into the freshly cloned project and use a package manager of your choosing to install required dependencies:
```
cd sequel-pro-to-tableplus-importer
npm install
```

Be sure both Sequel Pro and TablePlus are closed and run the script:
```
./tp-importer
```
###  Note: It does not import over the passwords.
To get access to your passwords please use your keychain and search for the host name. 

## Credit
* [brandonjjon](https://github.com/brandonjjon/tp-importer) - This project is a fork from.

## Built With

* [Commander.js](https://github.com/tj/commander.js/) - node.js command-line interfaces
* [Inquirer](https://github.com/SBoudrias/Inquirer.js/) - A collection of common interactive command line user interfaces.
