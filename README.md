Modified Defuse.ca's Pastebin
=============================


- Restored original code from defuse.ca (https://github.com/defuse/pastebin)
- Recreated MySQL DB
- Added config.php for rapid deployment

Database Table
--------------
desc pastes;
+---------+-------------+------+-----+---------+-------+
| Field   | Type        | Null | Key | Default | Extra |
+---------+-------------+------+-----+---------+-------+
| token   | varchar(70) | YES  |     | NULL    |       |
| data    | text        | YES  |     | NULL    |       |
| time    | int(11)     | YES  |     | NULL    |       |
| jscrypt | text        | YES  |     | NULL    |       |
+---------+-------------+------+-----+---------+-------+

Setup
-----
mysql -p
> CREATE DATABASE pastebin;
> CREATE TABLE pastes (token VARCHAR(70), data TEXT, time INTEGER, jscrypt TEXT);

TODO:
-----
- Pretty up the UI. pastebin.html hasn't really been touched
- Burn after reading?
