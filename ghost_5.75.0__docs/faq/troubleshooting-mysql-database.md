Resolving a misconfigured MySQL database with Ghost - Ghost Developers
Common searches

* [how to set up my custom domain](/help/using-custom-domains/)
* [how to install ghost](/docs/install/)
* [login not working, how to reset password](/help/how-do-i-reset-my-password/)
* [cloudflare setup and config](/help/cloudflare-domain-setup/)
* [how to make a ghost theme](/docs/themes/)
[Developer docs](/docs/)

Quick-search for anything⌘F[5.116.1](https://github.com/tryghost/ghost/)

If your MySQL database is not correctly configured for Ghost, then you may run into some issues.

The solutions given are for self-hosted Ghost developers who are using the supported install method with `ghost-cli`. If you’re having problems with an unsupported custom install, check out the [forum](https://forum.ghost.org/).

### Error `ECONNREFUSED`

If you’re seeing an `ECONNREFUSED` error, which refers to port `3306`, Ghost wasn’t able to connect to your MySQL server and you need to check if your server is running via the command line.

To fix this issue:

1. Ensure the server is running with `sudo service mysql start`
2. Test that the server is now running by typing `mysql` in the command line and checking the response
3. If this error occurred after using `ghost install`, once resolved, re-run the setup phase using `ghost setup`

### Error `ER_BAD_FIELD_ERROR`

This may be caused by `ANSI_QUOTES` [sql mode](https://dev.mysql.com/doc/refman/8.0/en/sql-mode.html) or by [combination modes](https://dev.mysql.com/doc/refman/8.0/en/sql-mode.html#sqlmode_ansi) such as `ANSI` that include `ANSI_QUOTES`. To check your sql mode, run `SELECT @@sql_mode` in mysql.

To fix this issue:

1. Find and open your `my.cnf` file ([see below](#finding-your-mycnf-file))
2. Remove `ANSI_QUOTES` or `ANSI` from the `sql_mode` line

### Error `ER_FK_COLUMN_CANNOT_CHANGE`

This may be caused by missing the `STRICT_TRANS_TABLES` [sql mode](https://dev.mysql.com/doc/refman/8.0/en/sql-mode.html).

To fix this issue:

1. Find and open your `my.cnf` file ([see below](#finding-your-mycnf-file))
2. Add `STRICT_TRANS_TABLES` to the `sql_mode` line

### Error `ER_TOO_BIG_ROWSIZE`

The `row_format` of a table determines how it is stored, and this introduces limits on the size of the data. Older versions of MySQL and MariaDB used a different default `row_format` of `COMPACT` or `REDUNDANT`, which have stricter row size limits. The default on the latest version is `DYNAMIC`, which is what we support.

> In MariaDB 10.1 and before, and in MySQL 5.6 and before, the COMPACT row format was the default row format.
> - <https://mariadb.com/kb/en/troubleshooting-row-size-too-large-errors-with-innodb/>

To confirm if your database is affected:

1. Run `show table status;` whilst attached to the database in MySQL
2. If `Row_format` says `COMPACT` or `REDUNDANT`, this table needs updating to `DYNAMIC`.

To fix this issue MySQL should be updated to the latest version and all tables used by Ghost should be converted to the `DYNAMIC` format:

1. Ensure you have a recent backup of your database
2. Update MySQL to the latest supported version (so the default is `DYNAMIC` moving forwards)
3. For each table, run `ALTER TABLE <table> ROW_FORMAT=DYNAMIC;`
4. `show table status;` should report all tables are `DYNAMIC` and the problem should be solved

### Error `ER_CANT_CREATE_TABLE` with *“Foreign key constraint is incorrectly formed”* or `ER_FK_INCOMPATIBLE_COLUMNS`

MySQL is unable to create tables with foreign keys referencing tables using a different collation. This usually occurs after upgrading to MySQL 8 from an earlier version:

> The default collation for utf8mb4 differs between MySQL 5.7 and 8.0 (`utf8mb4_general_ci` for 5.7, `utf8mb4_0900_ai_ci` for 8.0).
> - <https://dev.mysql.com/doc/refman/8.0/en/charset-connection.html>

To fix this issue, ensure that all tables use the same collation as the default connection collation. You can find this by checking the value for `show variables like '%collation_connection%';`.

#### Finding your my.cnf file

* Run `mysql --help` and look for the line “Default options are read from the following files in the given order:”
* Below that line will be a list of locations to check
* You can also try using find: `sudo find / -name my.cnf` although the file can be called either `my.cnf` or `.my.cnf`
* If you can’t find a my.cnf file, create one at the first location in the list provided by `mysql --help`.
* The default sql\_mode line in MySQL 8 looks like: `sql_mode=ONLY_FULL_GROUP_BY,STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION`
##### On this page

Launch your site
----------------

Last week, 5,069 brand new  
publications got started with Ghost.

Today, it's your turn.

[Start a free trial now →](https://account.ghost.org/signup/)Product

* [Creator platform](/)
* [Theme marketplace](/marketplace/)
* [Integrations](/integrations/)
* [Experts](/experts/)
* [Ghost for news](/news/)
Developers

* [How to install Ghost](/docs/install/)
* [Core concepts](/docs/)
* [Ghost hosting](/pricing/)
* [API documentation](/docs/content-api/)
* [Security overview](/docs/security/)
* [Source code](https://github.com/TryGhost/Ghost)
Resources

* [Ghost tutorials](/tutorials/)
* [Resources](/resources/)
* [Node.js CMS guide](https://nodecms.guide)
* [Open Subscription Platforms](https://opensubscriptionplatforms.com)
Comparisons

* [Ghost vs Substack](/vs/substack/)
* [Ghost vs WordPress](/vs/wordpress/)
* [Ghost vs Medium](/vs/medium/)
* [Ghost vs Memberful](/vs/memberful/)
* [Ghost vs Patreon](/vs/patreon/)
* [Ghost alternatives →](/alternatives/)
Support

* [Help center](/help/)
* [Community forum](https://forum.ghost.org/)
* [Status  
  Triangle
  
  
  
   99.9%](https://status.ghost.org/)
[![Non-Profit Foundation](/images/logos/indie.svg)](/about/)
[![Open Source](/images/logos/opensource.svg)](https://github.com/tryghost)
[![Carbon Neutral](/images/logos/carbonneutral.svg)](https://climate.stripe.com/6MNofu)

