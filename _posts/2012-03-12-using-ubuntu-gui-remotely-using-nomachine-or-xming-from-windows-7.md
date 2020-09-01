---
layout: post
title: Using Ubuntu GUI remotely using NoMachine or Xming from Windows 7   
categories: [Linux, Ubuntu]
---

Solution 1: NoMachine

Steps:
* Download NoMachine Linux server from here 
[http://www.nomachine.com/select-package.php?os=linux&id=1](http://www.nomachine.com/select-package.php?os=linux&id=1)
* Follow installation instructions given here 
[http://www.nomachine.com/documents/server/install.php](http://www.nomachine.com/documents/server/install.php)
* Download NoMachine windows client from here 
[http://www.nomachine.com/download-package.php?Prod_Id=3655](http://www.nomachine.com/download-package.php?Prod_Id=3655)
* Follow installation instructions given here 
[http://www.nomachine.com/documents/client/install.php](http://www.nomachine.com/documents/client/install.php)

Solution 2: 
[Xming](http://sourceforge.net/projects/xming/)

Steps:
* Install PuTTY
[http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html)
* Follow steps in this site to install Xming and to set it up to make it work together with PuTTY
[http://rcc.its.psu.edu/user_guides/remote_display/xming/](http://rcc.its.psu.edu/user_guides/remote_display/xming/)
* Install additional fonts package for Xming
[http://sourceforge.net/projects/xming/files/](http://sourceforge.net/projects/xming/files/)
* Follow steps given in below link to increase the font sizes displayed in GUI through Xming
[http://aufather.wordpress.com/2010/11/21/increasing-font-size-in-xming-server/](http://aufather.wordpress.com/2010/11/21/increasing-font-size-in-xming-server/)

	
**Problem:**
Graphical programs are very slow.

**Solution:**
 Enabling "SSH compression" might help if you use a low bandwidth connection. The option is under Connection > SSH in the left menu of PuTTY. (
[http://doc.es.aau.dk/it_services/software/windows/putty_and_xming/](http://doc.es.aau.dk/it_services/software/windows/putty_and_xming/))

### Conclusion:
I am using  NoMachine, as Xming(6.9.0.31) was slow even after using SSH compression. And the latest version of Xming(7.5.0.45), which possibly has fixes for slow GUI (
[http://www.straightrunning.com/XmingNotes/](http://www.straightrunning.com/XmingNotes/)) was not  available for free.