# IAM_Auth
A Free Radius


Combine 3 Repository and Extract it selecting all RAR File
juvin92j0n/IAM_Authentication-
juvin92j0n/IAM_Auth
juvin92j0n/jon


A Free Radius AUTH with webinterface


Free  IAM AUTH can authenticate users on systems such as 802.1x (WiFi), dialup, PPPoE, VPN's, VoIP, and many others.   IAM Auth admin is compiled for mainly PPPOE user manage,  IAM AuthAdmin is a project of mine and I make it Open source, with the intention of being a webinterface for Free IAM AUTH (mainly for user/group management).  IAM AuthAdmin is written in PHP and works by manipulating Free IAM AUTH' SQL database. Naturally, this requires that you use the rlm_sql module for authorization and/or accounting on Laravel Framework.
Free IAM AUTH' database consists of the following tables:
•	radcheck
•	radreply
•	radgroupcheck
•	radgroupreply
•	radusergroup
•	many more 
In rlm_sql, the tables mentioned above are analogous to the users file in rlm_files.
In addition, the rlm_sql schema includes some other tables:
•	nas
•	radacct
•	radpostauth
These tables are meant for client (nas) management, accounting and post-authentication logging respectively.  IAM AuthAdmin provides a frontend (in the case of accounting and post-auth, mostly statistics and reports) for these functions too. Of course, the again calls for the use of rlm_sql in those sections of Free IAM AUTH config. For more info, please see rlm_sql's documentation.
 IAM AuthAdmin doesn't augment or replace Free IAM AUTH' default SQL schema: it just needs access to the existing database and uses another database for  IAM AuthAdmin's own data storage needs. This is done not to pollute Free IAM AUTH' database with  IAM AuthAdmin's own stuff.
(Planned) Features
•	Add, remove and edit users and groups
•	Manage user-group relations
•	Manage every user's or group's check and reply attributes
•	Manage clients (nasses)
•	Show statistics and graphs about accounting and post-auth data
Development status
Currently,  IAM AuthAdmin is in a very early stage. Most features are not done yet, and it is thus not ready for use. It collected from many sources.
2015-09-02
Re 1 is released. The core framework is done. The only features that work are:
•	User management
•	Group management
•	Reply and check attributes
•	ISP all Billing control 
•	BD BTRC (Regulatory)  Report 
•	All reporting
•	Login Attemp
•	Each and everything
Used tools and libraries
 IAM AuthAdmin uses the following server-side tools, languages and libraries:
•	Primary language: PHP Laravel
•	Database access layer: PDO
•	Templating engine: Adminalt
In addition,  IAM AuthAdmin also uses the following front-end frameworks:
•	Javascript library: jQuery
•	Front-end framework: Bootstrap
•	Bootstrap theme: Bootswatch Flatly
•	Icon packs: Glyphicons and Font nice
•	Logo Static
Instructions
Download a stable release or clone the development branch (bleeding edge!). Put them somewhere where your webserver has access to them.
Now run composer install in the directory containing composer.json to let Composer download the dependencies for you. The directory structure should now look like this:
•	 IAM AuthAdmin
o	app
o	public_html
o	tmp
o	vendor
As you might have guessed, the public_html directory is going to be the docroot. All the other directories shouldn't be publicly available. You webserver should have read+execute access to all 4 subdirectories. In addition, it needs write access to the tmp directory.
Create a database and user for  IAM AuthAdmin and import the SQL file. Copy app/config.php.example to app/config.php and edit the file to reflect your database settings.
Databases
 IAM AuthAdmin needs access to 2 databases: Free IAM AUTH' database and  IAM AuthAdmin's own database. These two database don't necessarily have to reside on the same server, although the example config file assumes they do.
The schema for Free IAM AUTH' database can be found in raddb/mods-config/sql/main/*/schema.sql.  IAM AuthAdmin's schema is  IAM Authadmin.sql and should be in this directory.
 IAM AuthAdmin is made with MySQL in mind, but can probably work with other RDBMSs as well by editing app/include/db.php.
Requirements
Since the latest version uses scalar type hinting and return type hinting, it requires PHP 7. Older versions work on PHP 5.4. or letter  IAM AuthAdmin depends on Smarty, and dependencies are managed using Composer.
Debugging the Free  IAM Auth Server
Run the server in debugging mode, ( IAM Authd -X) and READ the output. We cannot emphasize this point strongly enough. The vast majority of problems can be solved by carefully reading the debugging output, which includes WARNINGs about common issues, and suggestions for how they may be fixed.
The debug output is explained in detail in the  IAM Authd-X page on the wiki.
Many questions are answered on the Wiki:
https://wiki.free IAM Auth.org
Read the configuration files. Many parts of the server are documented only with extensive comments in the configuration files.
Search the mailing lists. For example, using Google, searching "site:lists.free IAM Auth.org " will return results from the Free IAM AUTH mailing lists.
https://free IAM Auth.org/support/
Instructions for what to post on the mailing list are on the wiki. Please note that we DO recommend posting the output of IAM Authd -X. We do NOT recommend posting the configuration files.

License and Author

Copyright:: 2015 Juvin Jon Controlled Full Free for All anyone can use and Developed. 
