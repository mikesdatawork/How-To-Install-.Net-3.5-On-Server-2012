![MIKES DATA WORK GIT REPO](https://raw.githubusercontent.com/mikesdatawork/images/master/git_mikes_data_work_banner_01.png "Mikes Data Work")        

# How To Install .Net 3.5 On Server 2012
**Post Date: March 7, 2016**        



## Contents    
- [About Process](##About-Process)  
- [SQL Logic](#SQL-Logic)  
- [Build Info](#Build-Info)  
- [Author](#Author)  
- [License](#License)       

## About-Process

<p>Here's how to install .Net 3.5 on Server 2012. Admittedly it's a real pain trying to get the good'ole .net 3.5 installed on Server 2012 through server manager. Here are some quick steps to get you started.

1. Open Command Prompt 'As Administrator'.
2. Run this script ( you don't have to modify anything ). This sets up the feature installation to allow you to select other sources such as files, cd's, mounted drives, etc.
dism /online /enable-feature /featurename:NetFX3 /all /Source:d:\sources\sxs /LimitAccess
3. Next go back to the OS and find the Server install files (probably .iso on network share), and 'mount' the drive as a cd, or copy all the installation files over to the server locoally.
Note: You can mount .iso files from the network. Just takes a minute longer to run the .net 3.5 install.
4. Run through the Server Manager, and navigating to the .NET 3.5 selection again. You'll noticed down below after you've selected it and clicked 'Next' you'll see the 'specify an alternate source path'.
5. Browse to the SXS folder #\Sources\SXS
6. Click Install.
Done.
Might be a good idea to restart the server afterwords to ensure the OS picks up the changes, and of course will undo the 'mount'. Otherwise you'll lock the .iso and keep others from using it.</p>


[![WorksEveryTime](https://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](https://shitday.de/)

## Build-Info

| Build Quality | Build History |
|--|--|
|<table><tr><td>[![Build-Status](https://ci.appveyor.com/api/projects/status/pjxh5g91jpbh7t84?svg?style=flat-square)](#)</td></tr><tr><td>[![Coverage](https://coveralls.io/repos/github/tygerbytes/ResourceFitness/badge.svg?style=flat-square)](#)</td></tr><tr><td>[![Nuget](https://img.shields.io/nuget/v/TW.Resfit.Core.svg?style=flat-square)](#)</td></tr></table>|<table><tr><td>[![Build history](https://buildstats.info/appveyor/chart/tygerbytes/resourcefitness)](#)</td></tr></table>|

## Author

[![Gist](https://img.shields.io/badge/Gist-MikesDataWork-<COLOR>.svg)](https://gist.github.com/mikesdatawork)
[![Twitter](https://img.shields.io/badge/Twitter-MikesDataWork-<COLOR>.svg)](https://twitter.com/mikesdatawork)
[![Wordpress](https://img.shields.io/badge/Wordpress-MikesDataWork-<COLOR>.svg)](https://mikesdatawork.wordpress.com/)


## License
[![LicenseCCSA](https://img.shields.io/badge/License-CreativeCommonsSA-<COLOR>.svg)](https://creativecommons.org/share-your-work/licensing-types-examples/)

![Mikes Data Work](https://raw.githubusercontent.com/mikesdatawork/images/master/git_mikes_data_work_banner_02.png "Mikes Data Work")

