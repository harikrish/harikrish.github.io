---
layout: post
title: Connecting to Amazon EC2 Linux instance using PuTTY
categories: [SSH, Linux, Cloud]
---

EC2 private key file has extension .pem , which cannot be used by PuTTY. So we have to convert .pem to .ppk format which PuTTY accepts.  Listing the steps below to do it,

* Download PuTTYgen - 
[http://the.earth.li/~sgtatham/putty/latest/x86/puttygen.exe](http://the.earth.li/~sgtatham/putty/latest/x86/puttygen.exe)
	
* Launch PuTTYgen, Using the 'Import' command from the ‘Conversions’ menu, load the .pem file of EC2 and press  'Save Private Key button'. Ignore warning about leaving the passphrase blank.  The file will be saved with .ppk extension

* Now launch PuTTY, go to SSH panel, 'Private key file for authentication' load the .ppk file, and now you can use PuTTY to connect to the EC2 instance.

References:
- [http://clouddb.info/2009/05/17/a-quick-overview-of-putty-and-ssh-for-aws-newbies/](http://clouddb.info/2009/05/17/a-quick-overview-of-putty-and-ssh-for-aws-newbies/)
- [http://the.earth.li/~sgtatham/putty/0.62/htmldoc/Chapter8.html#puttygen-conversions](http://the.earth.li/~sgtatham/putty/0.62/htmldoc/Chapter8.html#puttygen-conversions)
- [http://the.earth.li/~sgtatham/putty/0.62/htmldoc/Chapter4.html#config-ssh](http://the.earth.li/~sgtatham/putty/0.62/htmldoc/Chapter4.html#config-ssh)
- [http://docs.amazonwebservices.com/AWSEC2/latest/GettingStartedGuide/LaunchInstance.html](http://docs.amazonwebservices.com/AWSEC2/latest/GettingStartedGuide/LaunchInstance.html)