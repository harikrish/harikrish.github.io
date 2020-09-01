---
layout: post
title:  "How to delete a Git branch both locally and remotely?"
date:   2017-05-18 16:36:00 -0700
categories: [Programming, Git]
---

To delete the local branch use:
{% highlight shell %}
$ git branch -d branch_name
{% endhighlight %}

To delete the remote branch use:
{% highlight shell %}
$ git push origin --delete <branch_name>
{% endhighlight %}

References
- http://stackoverflow.com/questions/2003505/how-to-delete-a-git-branch-both-locally-and-remotely