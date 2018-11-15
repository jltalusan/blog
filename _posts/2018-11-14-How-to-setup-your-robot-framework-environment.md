---
title: "How to setup your Robot Framework environment"
date:   2018-11-14 15:23:10 +0800
categories: "QAEngineers"
---

### Installing the following Prerequisites

- [SublimeText](https://www.sublimetext.com/3)
- [SourceTree](https://www.sourcetreeapp.com/)
- [GitBash](https://git-scm.com/downloads)
- [BeyondCompare](https://www.scootersoftware.com/download.php)
- [Python](https://www.python.org/downloads/windows/)
<br>
`Install Python 2.7.xx whichever is most recent, currently Python 2.7.15`
<br>

![Image with caption](https://i.imgur.com/Pdy95h0.jpg "Image with caption")
_Select Install for All Users -> Next -> Add Python.ext to Path -> Next -> DONE_
- [Pip](https://bootstrap.pypa.io/get-pip.py)
<br> `Save as Python file in Downloads`
<br> `Open Windows Powershell`
<br> `cd Downloads`
<br> `python get-pip.py`

- [Chromedriver](http://chromedriver.chromium.org/downloads)
<br> `Click latest release version`
<br> `Download Wndows Version zip`
<br> `Move chromedriver file to C:\Python27\Scripts`

- [IntelliJ IDEA : Community Edition](https://www.jetbrains.com/idea/download/#section=windows)
<br> `Go To File -> Settings -> Plugins`
<br> `Uninstall IntelliBot (if you don't have it, better)`
<br> `Browse repositories -> Install the ff. plugins`
<br> - `Python Community Edition`
<br> - `Robot Framework Support`
<br> - `Robot Plugin`

- [Robot Framework + Plugins](http://robotframework.org/)
<br> `Open Windows Powershell`
<br> `pip install robotframework`
<br> `pybot --version`
<br> `pip install robotframework-seleniumlibrary`
<br> `pip install robotframework-selenium2library`
<br> `pip install robotframework-databaselibrary`
<br> `pip install robotframework-excellibrary`
<br> `pip install robotframework-sshlibrary`
<br> `pip install pymysql`
<br> `pip install pymssql`
<br> `pip install robotframework-ride`
<br> `pip install openpyxl`

- [Using SourceTree to clone our repository to your local machine pt.1](https://www.sourcetreeapp.com/)
<br> `Open SourceTree App` 
<br> `Click Remote`
<br> `Add you atlassian/bitbucket account`
<br> `Search Organization Repos for ami-ph-qa`
<br> `Click Clone`

![Image with caption](https://i.imgur.com/3EPINdE.jpg "Image with caption")
_Image 1_

- [Using SourceTree to clone our repository to your local machine pt.2](https://www.sourcetreeapp.com/)
<br> `Wait for SourceTree to finish loading the repository's configuration`
<br> `Click Clone button after SourceTree finished loading the configurations`
<br> `It should automatically create a repository copy in your machine in Documents\ami-ph-qa`
<br> `Now open the ami-ph-qa folder in your IntelliJ IDEA Community Edition` 

![Image with caption](https://i.imgur.com/ttNUTm1.jpg "Image with caption")
_Image 2_