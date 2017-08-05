####Please read the [Wiki/FAQ](https://github.com/SickRage/SickRage/wiki) before opening an issue####
All issues and bug reports must be opened at [GitHub](https://github.com/SickRage/SickRage/issues) and you **MUST** follow **ALL** [guidelines](https://github.com/SickRage/sickrage.github.io#submitting-a-bugissue-ticket).

<br/>

####2017-08-04####

Our main repository on Github [SickRage/SickRage](https://github.com/SickRage/SickRage) is now available.<br/>
If you installed SickRage using a mirror of **our** repository, or switched your installation to get updates from a mirror, please make sure that you're back on the main repo URL in order to be able to receive future updates.<br/>
The basic set of commands is described [here](https://github.com/SickRage/sickrage.github.io#before-you-open-an-issue):
```
git remote set-url origin https://github.com/SickRage/SickRage.git
git fetch origin
git checkout master
git branch -u origin/master
git reset --hard origin/master
git pull
```

<br/>


####2017-07-20####

A false DMCA takedown request was sent to GitHub, resulting in multiple repositories, including SickRage/SickRage, to be taken down.
We're countering this and should have the repo back very soon. We thank you for your patience.

<br/>

####2017-02-21####

It seems that the long-time free `Womble's Index` for nzb's has been taken offline.
We thank Womble for all of the years providing this free usenet index, and as a result of it going down we have had to remove the provider code for it from SickRage.

<br/>

####2017-01-26####

WINDOWS ONLY: SickRage now requires WinRar to be installed for windows users to be able to unrar releases.
The location of unrar should now be autodetected with the latest update, but if it is not you may need to add `C:\Program Files\WinRar` to your system path and restart SickRage.
As you windows users should know, restarting SickRage from the interface does not work, you will have to restart the service either through the service manager,
or from an administrator level command prompt with the following commands:
<br/>
```
    net stop sickrage
```
<br/>
```
    net start sickrage
```
<br/>
The library we use to interface with unrar had to be changed for several reasons, including unrar lockups, memory issues, and a lack of support for newer RAR5 format.


<br/>

####2016-12-20####

There is a small issue related to network timezones after the recent commits to make them case insensitive.
If stopping SickRage completely and then starting it again does not work, stopping it and deleting cache.db and then starting it back up should resolve the issue.

<br/>

####2016-04-11####

With my next commit, your web interface may revert to english translation. However, it is now a configurable option as to which language you want to use.  
You can find the option to change the language on http://localhost:8081/config/general/ at the top of the 'Interface' tab.
I hope you all are enjoying the translations, and please feel free to help out with them on [crowdin.com](https://crowdin.com/project/sickrage)

<br/>

####2016-04-08####

Among the many fixes in today's release, there is something special.  
**The web interface in SickRage is now translatable into any language!**  
If you would like to help translating the strings some information can be found on the [WIKI](https://github.com/SickRage/SickRage/wiki/Translations)  
Also, we would like to thank [CrowdIn](https://crowdin.com/project/sickrage) for our free open source project account to help managing the translations.

<br/>

####2016-03-25####

Quick note for Synology users. Yesterday Synology released [DSM 6,](https://www.synology.com/en-global/dsm/6.0) we advice users to wait with the update.
The problem is that the Sickbead-custom (and other Synocommunity) packages are not fully compatible yet.
If the packages are installed on DSM 5.2 and you upgrade they will keep working, but on a fresh DSM6 install or if you need to re-install the package they wont work anymore. More info and workarounds can be found on our [issue tracker](https://github.com/SickRage/sickrage-issues/issues/587#issuecomment-201275502)

<br/>

####2016-03-14####

Some users can experience that air-dates are not updated for every show.  
If that is the case, than go to "Mass-update" and select "Update" for all shows, and let it run.  

Also when you get a warning in your log like **Missing time zone for network:** those can be added [here.](https://github.com/SickRage/sickrage.github.io/blob/master/sb_network_timezones/network_timezones.txt)  
They are used to calculate the exact airtime of a show in your specific timezone. This allows Sickrage to start searching more precise, without this the search starts at exactly midnight local time.  

<br/>

####2016-01-12####

Here are another 200+ commits for you guys, which brings many bug fixes. Many providers were fixed up,
and a new 404 and error page has been added, along with the usual code cleaning and optimization.
Hope you enjoy!

<br/>

####2015-12-22####

The next release brings **many** fixes (~200 commits), and along with it will come some changes to how qualities are handled. Most specifically, **Archive on First Match** has been removed.

Before it is released tomorrow, we wanted to inform you of the changes, and steps you may need to take to keep your setup operating as expected. Please read [this wiki page](https://github.com/SickRage/sickrage-issues/wiki/Qualities-Changes) and take any necessary action before updating. You may also disable automatic updates until you can take the time to do so.

<br/>

####2015-12-01####

Currently we are (still) in the process of a large cleaning-up and optimization of the SickRage code.  
This was really overdue, and will pave the road to all the new and cool features we plan to implement for you.  
However there is always a risk that it will expose minor bugs, that we weren't able to catch during testing.  
In case you encounter one, please make sure to report it on the [issue-tracker](https://github.com/SickRage/sickrage-issues/issues) or [IRC channel](https://kiwiirc.com/client/irc.freenode.net/?theme=basic#sickrage-issues).  

This week we also launched our new [SickRage website](http://sickrage.github.io/).  

<br/>  

####2015-11-21####

For those who are not yet aware, we were forced to change/migrate the Repository on GitHub.
We apologize for any inconvenience this may have caused.  
As you can see, the team is up and running again and providing updates and support as before. Please make sure you update your bookmarks and links to point to the new repository:  

- New repository   :   https://github.com/SickRage/   
- New Issue tracker:   https://github.com/SickRage/sickrage-issues  
- New Wiki page    :   https://github.com/SickRage/sickrage-issues/wiki  

Please get the word out so your friends, package builders and tutorial makers are aware.  
For the Synology users, we made a tutorial so they can easily switch to the new [repository](https://github.com/SickRage/sickrage-issues/wiki/Switching-your-Synology's-Sickrage-to-the-new-repository).  
Again, apologies for any inconvenience this has caused.   

<br/>  

####2015-10-22####

There has been some confusion about yesterday's news about [nzbToMedia](https://github.com/SickRage/sickrage-issues/wiki/NZBtoMedia) and the removal of the outdated autoProcessTV files/folder.

- The built-in post-processor is not being changed or effected in any way. If you use The built in post-processor, these changes do not affect you whatsoever and you do not need to make changes to your setup.

- SickRage will still support the use of autoProcessTV and sabtosickbeard.py, but we are no longer including them in the SickRage folder. If you still prefer to use the (old) autoProcessTV script package then you will have to manually download and store it somewhere outside of SickRage. It is however, recommended that you start switching over to the newer/better nzbToMedia in this case.

- [nzbToMedia](https://github.com/SickRage/sickrage-issues/wiki/NZBtoMedia) is a rewrite/improvement upon autoProcessTV that adds support for Torrents, among other things. nzbToMedia is now included in the SickRage source in the contrib folder and you can find information about nzbToMedia and setup on our [Wiki](https://github.com/SickRage/sickrage-issues/wiki/NZBtoMedia) and the [nzbToMedia Wiki](https://github.com/clinton-hall/nzbToMedia/wiki).

<br/>

####2015-10-21####

- New subtitles changes in today's version include the very latest and greatest subliminal. We have also added a new
subtitle provider [Legendas.TV](http://legendas.tv/) on top of what subliminal has to offer, and added some options to the subtitles settings page. You now have the option to download hearing impaired subtitles, and set login information for OpenSubtitles, Addic7ed, and Legendas.TV. Enjoy.

- Just 9 days left before we remove autoProcessTV from SickRage, since it has been deprecated about a month ago in favor of nzbToMedia. Please make sure to switch over before then if you are using it, or make sure to be using an autoProcessTV that resides outside of the SickRage source directory.

<br/>

####2015-10-02####

- Recently we improved the searching of the KAT & TPB Torrent providers. Some users report that they are not able to find new downloads anymore. If that is the case, shut down SickRage and remove the cache.db file. That should solve the problem.  

<br/>

####2015-09-26####

- Today we introduced our new [Feature Tracker.](http://feathub.com/SickRage/SickRage) Let us know what features YOU would like to see added. And cast your vote for the already submitted features.
- (All feature requests should go to the new tracker, not the issue-tracker.)

<br/>

####2015-09-20####

- *ShowsRage*
- One of our contributors (MGaetan89) has released his Android application for managing SickRage to Google Play. Be sure to check it out, rate, and provide feedback to show your support.
You can read the full description and information on [Google Play](https://play.google.com/store/apps/details?id=com.mgaetan89.showsrage) and the [ShowsRage GitHub Project](https://github.com/MGaetan89/ShowsRage)

<br />

####2015-09-09####

- As you might have noted the [TVRage](http://www.tvrage.com) website pulled the plug/shut down. And that is causing some issues we needed to address. We pushed a fix that automatically converts the TVRage ID to a TheTVDB ID. So that new data is pulled from theTVDB.com instead. That works for most users but sadly not all. So be aware that when you used TVRage shows, you might experience some issues. Be assured that we are working hard to get this all sorted out.
Also as a consequence of the TVRage shutdown we where forced to push some changes for the theme/layout that where not completely tested. Therefore the Network logos are currently not working. Fix coming soon.

- But not only bad news, we have a brand new [SickRage installer](https://github.com/SickRage/sickrage-issues/wiki/SickRage-Windows-Installer) for Windows!

<br />

####2015-09-08####

- We are removing support for autoProcessTV in favor of Clinton Hall's nzbToMedia project, which we have imported in `contrib`
- autoProcessTV will be removed by 31-10-2015. Please update your post-processing scripts or they will break.

<br />

####2015-08-16####

- Switched to using mako templates in master. We should have ironed out all the issues regarding mako in past week. If not, please open an issue, using the guidelines above!

<br />

####2015-08-08####

- Switched to mako in develop branch. Please test it out and report in IRC, or on github. Security improvements such as moving sql out of the templates, form/input/uri validation coming soon. Performance improvements coming also, such as moving js out of the templates.

<br />

####2015-08-06####

 - We need some help writing the Wiki for Anime. If you want to help please contact neoatomic in IRC
 - All Wiki pages are now at this [URL](https://github.com/SickRage/sickrage-issues/wiki) so users can contribute

<br/>

####2015-07-24####

 - if you have issues with strange characters (ie. ƒÆ'A+â?TAƒâ) in files names and/or in the SR interface and/or your database file (sickbeard.db) is suddenly way bigger than it should be please FULL update & refresh all your shows and force a mass rename after. Depending on your library size it can take some minutes or some hours. Backup DB first.

<br/>

####2015-07-23####

 - Now you can choose your default page when opening/logging to SR (General Options > Misc > Initial page)

<br/>

####2015-07-21####

- Added ability to run an external script for every subtitle downloaded (can be used to embed subs in mkv/mp4)
    For info about the parameters passed see [PR#2139](https://github.com/SickRage/SickRage/pull/2139)

- Added IRC tab in web ui, to connect to the SickRage IRC channel

<br />

####2015-07-18####

- Added setting to disable SSL certificate verification under Config -> General -> Advanced Settings
  (Committed on July 15)

  This might help if you have SSL errors

<br/>

####2015-07-17####

- Added new sub-menu called "Changelog". You can check what has changed in SickRage in each release

<br/>

####2015-07-16####

+ **Default Episode Status**: We recently fixed this feature so you need  to:

    - Edit your shows via 'Mass update' and set the default status to WANTED instead of SKIPPED (if you want unaired episodes to be downloaded)
    - Set all new episodes that were marked SKIPPED before that to WANTED. You can check all of them at "Episode Status Management" selecting "SKIPPED" in "Manage episodes with status". Be careful with this! Make sure you have a backup of your database. Be advised!
    - Now when you will add a **NEW** show you will be asked for two status settings: already aired episodes and unaired episodes.

<span style="margin-left:100px">
<img src="https://cloud.githubusercontent.com/assets/2620870/8724471/3cb943f4-2ba6-11e5-99cd-d645fb9e824f.png" width="300">
</span>

+ **Providers:** Sick beard index and Womble provider are blocking SR application so avoid using them

+ **Develop branch**

    - We are upgrading Subliminal module and this may and will break your installation
    - Please avoid using the develop branch until we fully tested everything unless you know what you are doing
