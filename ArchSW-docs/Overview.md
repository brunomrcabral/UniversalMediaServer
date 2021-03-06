###Navigation
---
* [How it works](#how-it-works)
* [Compatibility](#compatibility)
* [Features](#features)
* [Dependencies](#dependencies)
* [Limitations](#limitations)
* [Restrictions](#restrictions)
* [4 + 1 Archietecture](#4-+-1-archietecture)
  * [Logical View](#logical-view)
  * [Process View](#process-view)
  * [Development View](#development-view)
  * [Physical View](#physical-view)
  * [Use Case View](#use-case-view)
* [Conclusion](#conclusion)
  


###Universal Media Server 
---
Universal Media Server (UMS) is a media server, developed using Java, capable of sharing  videos, audio and images to any DLNA-capable device ( Digital Living Network Alliance)  basically it is a set of interoperability guidelines for sharing digital media among multimedia devices. DLNA works with cable and satellite  to provide link protection on each end of the data transfer.
Universal Media Server is also a DLNA-compliant UPnP media server ( Universal Plug and Play ) is a set of networking protocols that permits networked devices, such as personal computers, printers, Internet gateways, Wi-Fi access points and mobile devices to seamlessly discover each other's presence on the network and establish functional network services for data sharing, communications, and entertainment. UPnP is intended primarily for residential networks without enterprise-class devices.

It allows streaming to many devices including Sony PlayStation 3 (PS3) and PlayStation 4 (PS4), Microsoft Xbox One and 360, many TVs (Samsung, Panasonic, Sony, Vizio, LG, Philips, Sharp), smart phones (iPhone, Android, etc.), Blu-ray players, and more.

Originally it was based on PS3 Media Server which allows the user to access windows media player that's on your computer. If the user is sharing the media player, the ps3 media server will pick up whatever is added to windows media player.Which in time allows the user to have access to any recently added content in the computer using the ps3 system which in turn makes it much easier and faster than burning disks to watch a new movie or listen to the new album the user just downloaded.

Although being based on PS3 Media Server , Universal Media Server , has some enhancements over its predecessor which include web interface support for non-DLNA devices, more supported renderers , automatic bit rate adjustment, and many other transcoding improvements.

###How it works
---
After installing UMS to your PC, Mac, or Linux machine, you then start creating your server via the main panel. You'll have to access this panel from your desktop toolbar since the program initially runs in the background.

Universal Media Server automatically detects compatible media renderers on the network, from Windows Media Player to Google Chrome, to an Android phone, to an console and displays IP addresses along with big, shiny graphics in the Status tab. General Configuration is where you'll adjust networking settings like which renderers to enable and make defaults, which router to stay bound to, and which open port on your firewall to go through.

Moving down the tabs, Navigations/Share Settings is where you tell UMS which folders to make available on the server. When it first launches, the program scans everything on your system. You'll want to change this as soon as possible or your new server will get cluttered with junk and the file structure will be messy. You'll need to keep your media nice and manageable with different folders for music, movies, and photos to ensure easy acces to the files you want.

Once you're finished, restart the server for your changes to take effect. The handy Log tab tracks all changes in chronological order, so if something goes wrong you can retrace your steps to find a possible solution. There is also a Transcoding Settings tab to adjust video quality and audio preferences, but  UMS has a automatic settings that should be just fine.

###Compatibility
---
Universal Media Server supports all major operating systems, with versions for Windows, Linux and Mac OS X. The program streams many different media formats with little or no configuration. It is powered by MEncoder, FFmpeg, tsMuxeR, MediaInfo, VLC, OpenSubtitles.org and more, which combine to offer support for a wide range of media formats , allowing the user to obtain any subtitle and to play any type of video format without having to look for a video player that is able to decode it either it being a .mkv, .mp4, .flv, .wmv, .avi or .3gp .

###Features
---
Universal Media Server provides many features that might not be available on other popular media servers, such as:  
* **Automatic maximum quality** - 100% video and audio quality maintained when possible by multiplexing.  
* **Intant browsing** - Files can be viewed without the need to wait for folders to be rescanned, which could take a long time with large libraries.  
* **Subtitles** - Even if the device used does not support the subtitle format in the video, it will be added anyway to the video stream. Subtitles can also be added via options on the device.  
* **DTS support** - Full quality DTS instead of downmixing it to a different format.  
* **H.264 transcoding** - Provides the same quality as MPEG-2, with lower filesize, a good option for wireless networks.  
* **True Motion (frame interpolation)** - Adds frames to the regular framerate to make the motion smoother and realistic. This is achieved using InterFrame, an AviSynth plugin that uses SVP libraries.  
* **Overscan compensation** - If the device is a TV, it might cut off the edges of the video, UMS compensates so the whole video is displayed.  
* **Automatic plugin download/install** - It is possible to download and install plugins automatically from within the program.  
* **Unlimited folders on PS3 and Xbox** - Traditionally, PS3 and Xbox 360 only display a limited number of folders, UMS has a work around for that.  
* **AviSynth** - UMS supports AviSynth, a powerful and flexible video and audio serving program.  
* **iTunes** - UMS supports iTunes, the user can browse his iTunes library by playlist, artist, album, genre.  
* **Renderers** - UMS supports rederers with search capability.  
* **Network Bandwith Settings** - User can set the speed of his network to ensure smooth playing.    
* **DVD Support** - DVD playing is supported, whether they are in the DVD drive or in the hard drive.    
* **Archives** - Browsing archives is supported, like ZIP, RAR, GZ, etc.  
* **High-quality video thumbnails** - Maximum quality and resolutions thumbnails that the device can handle.  

Universal Media Server is free, that itself can be considered a feature.

###Dependencies
---
This software requires Java and mediainfo (mediainfo openjdk-7-jre). Optionally, dcraw and VLC can also be used with Universal Media Server.

To compile from source, it requires Eclipse IDE for Java Developers, Maven, m2e Eclipse plugin and EGit Eclipse plugin.

The website of the founder also has the option to download a little program that installs the UMS without having to compile it from source , it's available for Mac Os X, Linux and Windows.

###Limitations
---
Confusing setup, web interface is plain and does not offer any remote access options (the ability for server owners to access their content outside the home).

There exists a rather bad limitation in the PS3. The PS3 will only allow a folder depth (that is the number of folders that can be opened after each other) of 8. So if you stack more than 8 folder after each other you can't access the last once. Which of course is bad. The limitation is built in to the PS3 so it is not possible to get around it in a easy way. 

There is a way to fix it the UMS has a folder limit workaround. The workaround must be enabled by adding "folder_limit=true" to your UMS.conf.

Once done you'll see a new folder at the top on your render called "Folder Limit". This folder is empty at start. When you browse around and hit the folder limit UMS will log it that you've hit it and it will add the point of where you hit the limit in the "Folder Limit" folder.

###Restrictions 
---
Universal Media Player uses DLNA . Now DLNA is a protocol that doesn't have any real definition of a "user". You don't have to "logon" to your TV for example. This leads to that all renders gets access to the same data. This might not be what you want. For example if you have two folders one that is kid-Friendly and another that is kid-Unfriendly you might want restrict the renders in the kids room to only have access to the kid-Friendly folder. UMS provides a number of methods to control the access, of information , by defining a Pin(just like the Atm one a sequence of 4 numbers from 0-9) ensuring that only the people tha know the code have access to its contents. 

###4 + 1 Archietecture
---
In this report we will use the model views [ 4 + 1  ] ( https://en.wikipedia.org/wiki/4%2B1_architectural_view_model ) Software Architecture to describe the project that we selected . This model is useful because it is the same software interpreted through different points of view. The 5 components of this model are as follows :
 - Logical view ( Package Diagram ) 
 - Process view ( Activity Diagram )
 - Development View ( Component Diagram ) 
 - Physical View ( Deployment Diagram ) 
 - Use Case View

###Logical View
---
In the next package diagram you can see the separation of the system in various source components and dependencies between packages. 
The Logical View shows the project has a organization and relationship between folders and import modules necessary for the operation of the program.
![alt tag](https://github.com/txEn/UniversalMediaServer/blob/master/ArchSW-docs/Logical View.jpg)
In our example we identified two major packages :
 * **NewGui** : This is the main package it's responsible for all the display of the graphical interface , be it buttons or tabs, so that the user can use it in an easy and convenient way.
 * **Network** : Is made up of all the files that allow access to the network that was created and at the same time its the main component between the graphical interface and all the content that is stored in the database.

###Process View
---
Allows us to show what the system does at high-level, it is also useful to represent how all the steps within a process are complementary, making it possible, to evaluate the non-functional requirements such as performance, scalability among others.

![alt tag](https://github.com/txEn/UniversalMediaServer/blob/master/ArchSW-docs/Process View.jpg)

###Development View
---
The development view or implementation view represents the organization of the system components. It can be divide in several diagrams, and each one it's used to model parts of the system like documents, executables and libraries and to show their dependencies. At the end the main function of this type of view is to visualize the system components and their organization and relationships.

![alt tag](https://github.com/joaomrsilva/UniversalMediaServer/blob/master/ArchSW-docs/Implementation_view.jpg)


###Physical View
---
The physical view describes the hardware components in wich software is developed. The main functions of this type of diagrams are show the hardware organization (nodes and their connections) and describe the hardware components used to unfold software. So, it's responsable to show to the developers how the components are unfolded in hardware.

![alt tag](https://github.com/joaomrsilva/UniversalMediaServer/blob/master/ArchSW-docs/Physical%20View.jpg)

There exists a host device that acts has an intermediary between the user inputs and the content that the user wants to access which is located in the network.
The host device contains all the encoders, gui and formats for the content, on the other hand the network is responsible for keeping track of all accesses to the network and the databases of content that exist within the network.

###Use Case View
---
In software and systems engineering, a use case is a list of actions or event steps, typically defining the interactions between a role and a system, to achieve a goal.
As already mentioned above the Universal Media Server is a program that allows its users to use it without the need to know any details of the implementation to interact with this software and take full advantage of the program such as sharing content over a private network using an easy to understand interface.
![alt tag](https://github.com/txEn/UniversalMediaServer/blob/master/ArchSW-docs/Use Case View.jpg)

###Conclusion
---
All diagrams present in the report were prepared by the authors of the same, and these are based on their interpretation of the various aspects of the project. It is possible that different interpretations can lead to different diagrams.

The [Logical View](#logical-view) is expressed by a package diagram, shows an abstraction of a system as a set of classes and the relationships between them. The packages are divided according to the features that implement and are described explicitly in the project repository.

[Process View](#process-view) is represented by an activity diagram, which shows the most relevant activities performed by the user side. They could be identified more activities, particularly on the server side, but we think that those are performed by the user have greater relevance.

[Development View](#development-view) this view illustrates a system from a programmer's perspective and is concerned with software management. Showing how the system is organized between modules.

With the [Physical View](#physical-view) we can show how are distributed the components of software and hardware, and managed to have a better idea of the functioning of some interactions of the system.

The project presents a satisfactory structure, but the task of extracting information to build some of the diagrams presented was not the simplest.
