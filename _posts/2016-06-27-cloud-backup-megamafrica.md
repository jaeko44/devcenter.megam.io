---
title: Backup your data in a Cloud Storage - MegamAfrica
layout: post
og_image_url: "https://devcenter.megam.io/res/gotalk-intro.png"
description: Backup your data in a Cloud Storage - MegamAfrica
---

### Introduction
You want to backup your data in cloud and access it on need.
Cloudberry backup desktop client can be used to backups files and folders on your Windows machine to our cloud storage - Atharva MegamAfrica.

#### Introducing Atharva Storage - MegamAfrica

**Atharva Storage** - MegamAfrica is a "Cloud object storage, low latency and (S3 - AWS Signature v2) compatible API  built on top of ceph - jewel.".

Upon successful signin to https://console.megamafrica.com, look for the icon
![](http://devcenter.megam.io/content/images/2016/06/storage-1.jpg)
 at the top right hand corner named `Storage`
![](http://devcenter.megam.io/content/images/2016/06/atharva-1.jpg)

This tutorial will guide you in setting up a **Cloudberry backup tool for windows client on your windows 7+/10 workstation** and connecting it to manage your atharva storage account in MegamAfrica.
<a href="https://console.megamafrica.com" target="_blank">
<img src="https://s3-ap-southeast-1.amazonaws.com/megampub/images/megamafrica/DEPLOY-TO-MEGAM-AFRICA-BIG1.png" alt="wordpres button" /></a>

### Prerequisites

* You are running Windows 7 or later version. This was tested on Windows 10.

* You have to create a valid credential for accessing https://console.megamafrica.com. [How to create an account with MegamAfrica](http://devcenter.megam.io/2016/05/27/how-to-launch-ubuntu/).

* You have to create an atharva storage account with MegamAfrica. [How to create an atharva account with MegamAfrica](http://devcenter.megam.io/2016/06/17/getting-started-atharva-storage-in-megamafrica/).

### Connecting Cloudberry Backup Desktop client with Atharva (Ceph object storage) MegamAfrica

This initial section contains everything you need to setup cloudberry backup tool for windows native client on your server.

##### Step-1 Download Cloudberry Backup Desktop client for windows

* Go to this link. <a href="http://www.cloudberrylab.com/download-thanks.aspx?prod=cbbackup" target="_blank">Cloudberry backup</a>.

* Click `Download` button to start your download.

* Right-click the download file and install it in your windows system.

###### Step-2 Create the storage setting with MegamAfrica

* Once you successfully install CloudBerry, start up the application to display the`Welcome` screen.

* click the`Setup Backup Plan` button in the middle of the page

* CloudBerry has many options for backup targets. In this tutorial we’re focusing on `Amazon’s s3 compatible` cloud storage offerings.

* On the `S3 Compatible Storage` tab specify Servie point as `88.198.139.81`.

* Enter the other details.

    	Display Name : Type a name for the account
		Access key
		Secret key
* You can see your `Access-key` and `Secret-key` from your `profile page` in MegamAfrica. (https://console.megamafrica.com)
![](http://devcenter.megam.io/content/images/2016/06/cloudberry-aws-s3-account-info.png)

* Click the "Advance Settings" and uncheck `Use SSL` link. Now you can see your bucket in `Bucket name` box. choose one of the bucket  you want to backup.

* Next you’ll want to select your `backup mode` as Simple.

* On the next page you’ll want to select your `Backup Source`. Select your folder to connect with MegamAfrica storage
![](http://devcenter.megam.io/content/images/2016/06/cloudberry-backup-wizard-backup-source.png)

* Once you see that your `Backup Plan` is successfully created, press "Finish" leaving the "Run backup now" box checked, to test your newly configured backup.

* From the Welcome screen you’ll be able to see that your backup is currently running, and some live summary information about the backup job.

##### Upload a file from cloudberry backup tool to MegamAfrica

* Copy the one or multiple files to upload/copy an upload folder if you want to upload a whole folder.

* Paste into `Backup source` folder. The upload process will begin.

* Let us verify if the files is uploaded

Logon https://console.megamafrica.com goto `storage` place. You can see your bucket, and the uploaded files are displayed.

### Conclusion

These are the very simple steps to create a sync tool for an upload files using Windows native client using cloudberry backup to Atharva - MegamAfrica.

This is a good head-start for using Cloudberry  & our Athava ceph based object storage in MegamAfrica.

### Start uploading to our storage - MegamAfrica

<a href="https://console.megamafrica.com" target="_blank">
<img src="https://s3-ap-southeast-1.amazonaws.com/megampub/images/megamafrica/DEPLOY-TO-MEGAM-AFRICA-BIG1.png" alt="wordpres button" /></a>
