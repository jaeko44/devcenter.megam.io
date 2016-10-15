---
title: How to launch Java - spring-webflow in MegamAfrica
layout: post
og_image_url: "https://devcenter.megam.io/res/gotalk-intro.png"
description: How to launch Java - spring-webflow in MegamAfrica
---

### **Introduction**
Spring Web Flow facilitates building the j2EE based web applications that require guided navigation -- e.g. a shopping cart, flight check-in, a loan application, and many others. In contrast to stateless, free-form navigation such use cases have a clear start and end point, one or more screens to go through in a specific order, and a set of changes that are not finalized to the end.

This tutorial will guide you in launching a J2EE web application (spring-webflow) in MegamAfrica.

<a href="https://console.megamafrica.com" target="_blank">
<img src="https://s3-ap-southeast-1.amazonaws.com/megampub/images/megamafrica/DEPLOY-TO-MEGAM-AFRICA-BIG1.png" alt="wordpres button" /></a>


###**Prerequisites**

* You are running Ubuntu 14.04 or Linux workstation.

* Git installed on your server, which you can do by following the [How To Install Git with Apt.](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-14-04)

* You have an account on GitHub, which is a Git repository host.

* You have to create a valid credential for accessing https://console.megamafrica.com. [How to create an account with MegamAfrica](http://devcenter.megam.io/2016/05/27/how-to-launch-ubuntu/)

You have to install openssh-server for ssh access.

	sudo apt-get install openssh-server
Check SSH working properly

	ps aux | grep sshd
In this tutorial you will see the steps to launch the J2EE using Spring-webflow application.

###Step-1 Fork spring web-flow

* To fork spring web-flow  https://github.com/verticeapps/java_springwebflow.git

* You will be see the fork option in the top right corner of the git hub page.click the fork option.

* The spring web-flow repository is forked into your git repository.

###Step-2 Launch the app
1. Go to MegamAfrica Dashboard

2. Click Marketplace on the top bar.Marketplace contains all the linux distros, applications, services and microservices which megamafrica supports.

3. Click Java Icon.A window will pop up for your git repository selection.

4. Pick a repository by choosing your repository.

  Let us use Github: < mygithub >/java_springwebflow.git

5. You can create new sshkey or use an existing sshkey or upload your own sshkeys too.

6. To launch J2EE App.Click Create.

* Voila ! Your App is up to date.

* Now that you have launched your app, you might want to launch a service (database) and bind it

*Rember that when you select memory its upto `2GB`

####Buildpack for Java

Java's default build pack get's going by kicking of maven. We plan to support `ant`, `gradle` in the future

	#!/bin/bash
	#Java builder WAR

	#megam_java_builder/build tomcat

	megam_home="/var/lib/megam/gulp"
	local_repo="/home/megam/tomcat/webapps"
	remote_repo="https://github.com/vinomca-megam/spring-webflow-samples.git"

	filename=$(basename "$remote_repo")
	extension="${filename##*.}"
	filename="${filename%.*}"

      rm $local_repo/*.war
      cd $megam_home
      rm -r $filename
      git clone $remote_repo
      cd $filename
      mvn clean
      mvn install -Dmaven.test.skip=true -U

	stop java
	start java

###**Step-3 Open Your Web browser**
  You can access your web page using `http://IP_ADDRESS:8080`

You will show the below UI
![](http://devcenter.megam.io/content/images/2016/05/1-1.png)

Select the Manager App.It asks User Name and Password
`Username and password is "megam"`

Then the below UI will be open

Here you will click the webflow show case link.

![](http://devcenter.megam.io/content/images/2016/05/2.png)

![](http://devcenter.megam.io/content/images/2016/05/3-1.png)



###Conclusion

These are the very simple steps to launch a J2EE web app (spring-webflow) using github repository.

###Deploy Java app now
<a href="https://console.megamafrica.com" target="_blank">
<img src="https://s3-ap-southeast-1.amazonaws.com/megampub/images/megamafrica/DEPLOY-TO-MEGAM-AFRICA-BIG1.png" alt="wordpres button" /></a>
