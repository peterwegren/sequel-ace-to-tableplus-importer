# Sequel Ace to Table Plus Importer

An unofficial way to migrate existing Sequel Ace connections to TablePlus.

## _Although a backup is created, this script is intended for use on fresh installations of TablePlus and will overwrite any existing connections._

### Prerequisites

- [TablePlus](https://tableplus.io/)
- [Sequel Ace](https://sequel-ace.com/)
- [Node](https://nodejs.org/) (_Make sure you are on the lastest version_)
- NPM or Yarn

Tested and working with node v21.7.2

### Installation

Please note that this script **_will not_** migrate any passwords. You will need to manually add passwords in TablePlus once the import is complete.

1. Clone the repository to your system or download the code:

```bash
git clone git@github.com:peterwegren/sequel-ace-to-tableplus-importer.git
```

2. Navigate into the freshly cloned project and use a package manager of your choosing to install required dependencies:

```bash
cd sequel-ace-to-tableplus-importer
npm install
```

3. Export favorites from Sequel Ace:

    1. Open Sequel Ace.
    2. Select all 'Favorites' that you want to migrate from the left sidebar, right click, and select '_Export Selected..._'.
    3. Ensure the file name is '_SequelAceFavorites.plist_' and save to your 'Downloads' directory.
        - The full path of the location to save this file should be: '_~/Users/\[username]/Downloads/SequelAceFavorites.plist_'.
        - This file may be named differently and/or stored in another file location — just be sure to update the `sequelAceFavorites` variable (located on line 9 in '_src/importer.js_') with the path to your file.
    4. Save.
    5. Quit Sequel Ace.

4. Quit both Sequel Ace and TablePlus.

5. Run the script:

```bash
./tp-importer
```

### _\*\*\*This script does not migrate passwords.\*\*\*_

To access to your passwords, use your keychain and search for the host name.

## Credit

- Forked from: [ashkellerman](https://github.com/ashkellerman/sequel-pro-to-tableplus-importer)

## Built With

- [Commander.js](https://github.com/tj/commander.js/) - node.js command-line interfaces.
- [Inquirer](https://github.com/SBoudrias/Inquirer.js/) - A collection of common interactive command line user interfaces.
