CakePHP 2.x.x Enum compatible files
===================================

The command "Console/cake schema generate/create" does not work with Enum type fields by default. You will always get NOTICE's while doing so, and won't be able to restore them. 

Even not be a huge fan of ENUM fields, sometimes you need to face them while working with really old projects. 

I did some changes (just a few lines in these two files), if you copy them to your project you will be able to use:

``Console/cake schema generate`` (to auto generate your database dump with ENUM fields)


And also:

``Console/cake schema create`` (to import/create them again)

Files edited:

``Model/Datasource/Database/Mysql.php`` (just added line 128)

``Model/CakeSchema.php`` (search for ENUM or matheuscmpm to see where I changed - just a couple lines too)

I added them into the project to be able to let my Cakephp directory clean.

Cheers.


Tested on Cakephp 2.8.9