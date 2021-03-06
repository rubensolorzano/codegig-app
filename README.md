﻿# codegig-app
 CodeGig is a web application where you can search, list and add IT gigs. 
 It uses Sequelize for ORM, MariaDB an Express. The GUI is made with vanilla.js.
 
## Usage

To use this web application at localhost you need to install MariaDB and create a database. 
Inside that database you need to create a table named gigs, with the following query:

```
CREATE TABLE `gigs` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`title` VARCHAR(200) NOT NULL,
	`technologies` VARCHAR(200) NOT NULL,
	`budget` VARCHAR(20) NOT NULL,
	`description` TEXT NOT NULL,
	`contact_email` VARCHAR(50) NOT NULL,
	`createdAt` DATE NOT NULL,
	`updatedAt` DATE NOT NULL,
	PRIMARY KEY (`id`)
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=13
;

```

Now, inside configs folder, open database.js and change it to your database data as shown below:

```
module.exports = new sequelize("YOURDBNAME", "YOUR-DB-SERVER-USERNAME", "YOUR-DB-SERVER-PASSWORD", {
  host: "YOUR-HOST",
  port: YOUR-PORT,
  dialect: "mariadb"
});
```

Now you can just navigate on terminal to the codegig folder and run:

```
npm run start
```

You're ready to go!

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Authors
Ruben Acevedo

