# WP Sync DB

Copy your database from one WP install to another with a few clicks in your dashboard.

Especially handy for syncing a local development database with a live site.

<img src="https://raw.github.com/slang800/psychic-ninja/master/wp-migrate-db.png"/>

**TABLE OF CONTENTS**

1. [How it Works](#how-it-works)
1. [Features](#features)
1. [How to Use](#how-to-use)
1. [Help Videos](#help-videos)

## How it works

WP Sync DB exports your database as a MySQL data dump (much like phpMyAdmin), does a find and replace on URLs and file paths, then allows you to save it to your computer, or send it directly to another WordPress instance. It is perfect for developers who develop locally and need to move their WordPress site to a staging or production server.

## Features

- **Selective Sync**

  WP Sync DB lets you choose which DB tables are migrated. Have a huge analytics table you'd rather not send? Simply deselect it and it won't be synced.

- **Pull: Replace a Local DB with a Remote DB**

  If you have a test site setup locally but you need the latest data from the production server, just install WP Sync DB on both sites and you can pull the live database down, replacing your local database in just a few clicks.

- **Push: Replace a Remote DB with a Local DB**

  If you're developing a new feature for a site that's already live, you likely need to tweak your settings locally before deploying. Once you've perfected your configuration on your development machine, it's easy to send the settings to your production server. Just push to the server, replacing your remote database with your local one.

- **Database Export & Backup**

  Not only can WP Sync DB pull and push your DB: it can export your DB to an SQL file that you can save and backup wherever you want. No need to ssh into your machine or open up phpMyAdmin.

- **Encrypted Transfers**

  All data is sent over SSL to prevent your database from being read during the transfer. WP Sync DB also uses HMAC encryption to sign and verify every request. This ensures that all requests are coming from an authorized server and haven't been tampered with en route.

- **Automatic Find & Replace**

  When migrating a WordPress site, URLs in the content, widgets, menus, etc need to be updated to the new site's URL. Doing this manually is annoying, time consuming, and very error-prone. WP Sync DB does all of this for you.

- **Stress Tested on Massive Sites**

  Huge database? No prob. WP Sync DB has been tested with tables several GBs in size.

- **Detect Limitations Automatically**

  WP Sync DB checks both the remote and local servers to determine limitations and optimize for performance. For example, we detect the MySQL `max_allowed_packet_size` and adjust how much SQL we execute at a time.

- **Sync Media Libraries Between Installations**

  Using the optional [WP Sync Media](https://github.com/hrsetyono/wp-sync-media) addon, you can have media files synced between installs too.

## How to Use

The guide below assume you're using it to sync online db with local one.

1. Install this plugin on both your online and local installation.
1. In your online installation, go to Tools > Migrate DB > Settings tab. Tick all three options: "Accept pull", "Accept push", and "Enable SSL".
1. Copy the **Connection Info**.
1. In your local installation, go to Tools > Migrate DB > Migrate tab. Choose Pull or Push and paste in the Connection Info.

    **PULL** means downloading the online db and use it to overwrite your local db. **PUSH** is uploading your local db to overwrite online db.

1. Configure the Search & Replace. Usually you need to replace "https" to "http" or vice versa depending on your site's configuration.
1. Click "Migrate DB" and wait for it to finish.

## Help Videos

| Title | Description | Link |
| --- | --- | --- |
| Feature Walkthrough | A brief walkthrough of the WP Sync DB plugin showing all of the different options and explaining them. | [Youtube](https://www.youtube.com/watch?v=u7jFkwwfeJc) |
| Pulling Live Data Into Your Local Development Environment | This screencast demonstrates how you can pull data from a remote, live WordPress install and update the data in your local development environment. | [Youtube](http://www.youtube.com/watch?v=IFdHIpf6jjc) |
| Pushing Local Development Data to a Staging Environment | This screencast demonstrates how you can push a local WordPress database you've been using for development to a staging environment. | [Youtube](http://www.youtube.com/watch?v=FjTzNqAlQE0) |
| Media Files Addon Demo | A short demo of how the [Media Files addon](https://github.com/hrsetyono/wp-sync-media) allows you to sync up your WordPress Media Libraries. | [Youtube](http://www.youtube.com/watch?v=0aR8-jC2XXM) |