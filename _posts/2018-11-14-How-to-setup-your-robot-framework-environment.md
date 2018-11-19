---
title: "How to setup your Robot Framework environment"
date:   2018-11-14 15:23:10 +0800
categories: "QAEngineers"
---

### Installing the following Prerequisites

- [Install SublimeText](https://www.sublimetext.com/3)
- [Install SourceTree](https://www.sourcetreeapp.com/)
- [Install GitBash](https://git-scm.com/downloads)
- [Install BeyondCompare](https://www.scootersoftware.com/download.php)
- [Install Python](https://www.python.org/downloads/windows/)

> Install Python 2.7.xx whichever is most recent, currently Python 2.7.15


![Image with caption](https://i.imgur.com/Pdy95h0.jpg "Image with caption")
_Select Install for All Users -> Next -> Add Python.ext to Path -> Next -> DONE_

- [Install Pip](https://bootstrap.pypa.io/get-pip.py)
{% highlight js %}
Save as Python file in Downloads
Open Windows Powershell
cd Downloads
python get-pip.py
{% endhighlight %}

- [Install Chromedriver](http://chromedriver.chromium.org/downloads)
{% highlight js %}
Click latest release version
Download Wndows Version zip
Move chromedriver file to C:\Python27\Scripts
{% endhighlight %}

- [IntelliJ IDEA : Community Edition](https://www.jetbrains.com/idea/download/#section=windows)
{% highlight js %}
Go To File -> Settings -> Plugins
Uninstall IntelliBot (if you dont have it, better)
Browse repositories -> Install the ff. plugins
Python Community Edition
Robot Framework Support
Robot Plugin
{% endhighlight %}

- [Install Robot Framework + Plugins](http://robotframework.org/)
{% highlight js %}
Open Windows Powershell
pip install robotframework
pybot --version
pip install robotframework-seleniumlibrary
pip install robotframework-selenium2library
pip install robotframework-databaselibrary
pip install robotframework-excellibrary
pip install robotframework-sshlibrary
pip install pymysql
pip install pymssql
pip install robotframework-ride
pip install openpyxl
{% endhighlight %}

- [Clone repository using SourceTree to your local machine pt.1](https://www.sourcetreeapp.com/)
{% highlight js %}
Open SourceTree App 
Click Remote
Add you atlassian/bitbucket account
Search Organization Repos for ami-ph-qa
Click Clone
{% endhighlight %}

![Image with caption](https://i.imgur.com/3EPINdE.jpg "Image with caption")
_Image 1_

- [Clone repository using SourceTree to your local machine pt.2](https://www.sourcetreeapp.com/)
{% highlight js %}
Wait for SourceTree to finish loading the repositorys configuration
Click Clone button after SourceTree finished loading the configurations
It should automatically create a repository copy in your machine in Documents\ami-ph-qa
Now open the ami-ph-qa folder in your IntelliJ IDEA Community Edition 
{% endhighlight %}

![Image with caption](https://i.imgur.com/ttNUTm1.jpg "Image with caption")
_Image 2_

# Yay we're done!
![Image with caption](https://i.imgur.com/Ly4fhh5.jpg/200x300 "Image with caption")
_Good Job :trollface:_