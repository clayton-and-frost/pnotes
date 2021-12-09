
***

```
-- Display list of tables in the currently selected database.
SHOW TABLES;
```

***

```
-- View the table details: field names and types, etc.
DESCRIBE books;
```

***

```
-- Create two related tables.
CREATE TABLE authors (
	id INTEGER UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY, 
	name VARCHAR(100))
DEFAULT CHARACTER SET utf8 ENGINE=InnoDB;

CREATE TABLE books (
	id INTEGER UNSIGNED NOT NULL AUTO_INCREMENT,
	author_id INTEGER UNSIGNED NOT NULL,
	description TEXT,
	price FLOAT NOT NULL,
    published DATE NOT NULL,
	PRIMARY KEY(id),
	FOREIGN KEY(author_id) REFERENCES authors(id))
DEFAULT CHARACTER SET utf8 ENGINE=InnoDB;
```

***

```
-- Delete the table.
DROP TABLE books;
```

***
