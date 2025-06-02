---
layout: post
title:  "Naming VMware Snapshots"
categories: vmware naming
---
I love using VMware snapshots before I do an upgrade or make a significant change.  However naming snapshots can be difficult, especially with the time travel aspect of it.  If you have a snapshot named just "Java v8" does that mean you took a snapshot before installing Java 8 or that you took a snapshot after installing Java 8 and want to keep it clean to go back to?

Since I mainly use VMware snapshots as a quick fallback, for upgrades or changes, I name all my snapshots starting with "Before".  

* Before Upgrade to Server 2012
* Before Java Upgrade
* Before VMware tools upgrade

Finally, because the thick client doesn't show me the date the snapshot was created, I prepend the date to every snapshot.  The previous list becomes:

* 2017-10-09 Before Upgrade to Server 2012 
* 2016-12-15 Before Java Upgrade 
* 2017-10-02 Before VMware tools upgrade 

