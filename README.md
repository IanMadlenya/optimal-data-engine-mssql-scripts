﻿# Optimal Data Engine (ODE) Scripts#
Copyright 2015 OptimalBI - Licensed under the GNU GENERAL PUBLIC LICENSE Version 3.0 (GPL-3.0)

## What Optimal Data Engine Scripts does: ##
This project contains a collection of scripts, which you are free to use, at your own risk, to make working with ODE Configuration easier and more standard.

## Requirements (All users): ##
It is assumed that you have an ODE installation as these scripts all relate to ODE configuration.
ODE itself can be downloaded from the related project - "optimal-data-engine-mssql", which has it's own installation instructions. 

## Branches: ##
Currently, ODE Scripts has two Branches available:
* master and
* develop

Master contains code which is known to be running in a production environment.

Develop contains the latest, locally tested version of the codebase.

## Download and build instructions: ##
If you wish to develop the code base further, we recommend that you use the Visual Studio solution which is provided.

The Project contains a number of discrete scripts, which you can copy off the GitHub website, or from the project zip.

### Pre-requisites ###

* Download a copy of the zip and extract to a temporary folder

### Scripted Install ###

* Open SQL Server Management studio and load *ode_to_mssql_scripts_Create.sql* from the extracted zip file. You will find it in the *ReleaseScript* folder.
* Within SQL Server Management Studio > Click Query Menu > SQLCMD Mode 
* Within the script optionally change the ConfigDatabase to your ODE_Config database name, DatabaseName and DefaultFilePrefix to the preferred ODE scripts database name; default is *ode_to_mssql_scripts*. *ODE_Admin* is recommended. 
* Click Execute from the toolbar. This should run successfully with a result of 'Update complete' on the Message panel

### Ad Hoc Usage ###

Scripts could be used on Ad Hoc basis without new database installation. Refer to folders *Configuration* and *Management* for Ad Hoc scripts.
 
## Current functionality: ##
Details of the current ODE functionality can be found here http://www.ode.ninja/category/features/
These scripts are linked on a number of pages in http://www.ode.ninja/ , where there usage is dicussed in more detail.

## Notes ##
* Untested on SQL Server editions prior to 2014. Installation script is compiled for SQL Server 2016.
* Stored procedures have hidden settings for columnstore indexes and table compression flags. You may need to edit stored procedures in case these features are not available in your instance of SQL Server.
* This product is still in Beta and should not be deployed to a production environment without thorough testing by you to ensure no adverse effects on your environment

## Feedback, suggestions, bugs, contributions: ##
Please submit these to GitHub issue tracking or join us in developing by forking the project and then making a pull request!

## Find out more: ##
Visit http://www.ode.ninja/ - this is where we keep our guides and share our knowledge. To find out more about OptimalBI and the work we do visit http://www.optimalbi.com or check out our blogs at http://optimalbi.com/blog/tag/data-vault/ for all the latest on our Data Vault journey. If you want to get in touch, you can email us at hey@optimalbi.com

## Change log: ##
```
Build 004.001.001 on 20170301
		* Scripts are upgraded to run on ODE version 4.1
		* Some scripts are transformed to stored procedures to be stored in ODE admin database (not in core config)
20160819 
        * Initial Build.
```
