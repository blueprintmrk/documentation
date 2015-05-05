---
title: Cloning an Existing Site from a Dashboard Backup
description: Make a copy of your existing code, files, and database.
category:
  - developing
keywords: clone, restore backup, clone existing pantheon site, clone from pantheon backup, clone pantheon site, copy pantheon site
---
All Pantheon sites consist of three parts:

* **Code**: The code that makes up your site. This is contained within your Pantheon Git repository.
* **Files**: Images, user uploads, and other files that are not stored in version control, located in /sites/default/files (Drupal) or /wherever/wp-uploads/go (WordPress).
* **Database**: The MySQL database utilized by your code to store content, settings, etc.

## Copy Your Code/Files/Database

1. From your site Dashboard, go to the live environment and click **Backups**.
2. Select the backup you want to clone from, and download each of the backup files (Code, Database, Files) by clicking the **download** icon.

## Import Your Code/Files/Database

1. Go to the Account page on [https://dashboard.pantheon.io/](https://dashboard.pantheon.io/)
2. Click **Create A New Site**.
3. Name your new site.
4. Select **Import site** from the "Choose your Start State" options.
5. Choose the **Click here to provide separate code, files, and database archives** link.
6. In each of the fields, change the option from URL to File, then select the archives you previously downloaded.
7. Click **Import Site**.
8. The import process will create and deploy a new site based on the uploaded files. If there are issues,  see  [Importing an Existing Site](/docs/articles/drupal/importing-an-existing-drupal-site-to-pantheon) for possible solutions, or open a support ticket from your dashboard. Be sure to include any error messages or relevant information.


## Additional Considerations
Retaining Git history, importing large file structures or databases:
The methods in this article will work well for small to medium sized sites, but will not import the Git repository commit history or logs. Also, Pantheon's import process cannot handle exceptionally large file structures or databases. For any of these scenarios, please see [Importing a Large Site](/docs/articles/sites/create/importing-a-large-site).
