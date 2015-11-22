Project History
===============
Microsoft first introduced the docking panel layout in Visual Studio .NET (2002), and soon it became popular in application design. Many commercial .NET component vendors started to provide docking libraries initially, but there was no good free and open source alternative, until WeiFen Luo released DockPanel Suite (DPS for short) on SourceForge.net in 2006.

http://sourceforge.net/projects/dockpanelsuite

WeiFen Luo's Efforts and Early Years
------------------------------------
Its 1.0 release was available on Feb 13, 2006, one day before the Valentine's day [1]. From the SVN repository we could no longer find the commits earlier than Mar 2, 2007. Therefore, we don't know exactly when WeiFen decided to implement this docking library and the day he started. This release has been downloaded more than 57,000 times on SF.net alone (binaries + source package), which is a huge success.

After that, WeiFen published several new releases. Release 2.0 RC was available on Mar 02, 2007. Release 2.0 followed on Apr 02, while release 2.2 was available on Nov 04, 2007 (more than 68,000 downloads)[2]

Danilo Corallo wrote an article titled "A Visual Studio 2005-like Interface"[3] on CodeProject.com initially on Jun 06, 2006 to introduce this library for broader audience. The article has been reviewed for more than 586,000 times with an average rate of 4.89. This article was last updated on 22 Jan, 2007, so it only targets DPS 1.0. However, DPS 2.0 and above do contains breaking changes, so the sample of this article does not work with newer DPS releases.

SharpDevelop [4], the open source C#/VB.NET IDE, has chosen DPS as its docking library for years (till SD 4.0 migrates to WPF and uses AvalonDock [5] instead of DPS). It is interesting that from SD code base, DPS source files appeared as early as Jan 04, 2005 [6].

On Aug 16, 2009, WeiFen wrote in a discussion thread, that he would like to move this project to CodePlex.com [7]. However, this move was never carried out. But in this thread WeiFen linked one of his important blog posts on DPS [8], which documented his ideas on why WPF based docking library is better. WeiFen's interest has been moved to WPF side product called WPF Docking [9].

Extended Maintenance by Steve Overton and Others
------------------------------------------------
Steve Overton and other contributors stepped up and started to maintain this library in 2009 [10]. He managed to release 2.3 on May 08, 2009 (more than 68,000 downloads)[11][12]. 2.4 Followed on Oct 30, 2010 with a few new patches [13]. For the first time, DPS is released with binaries/source code/release notes. This release has been downloaded over 8000 times. Soon release 2.5.0 (with RC1 flag) was available on Nov 25 the same year with more patches included [14]. This is the last stable release that can be found on SF.net with accumulated downloads of 61,000.

GitHub Fork and The DockPanel Suite Organization
------------------------------------------------
Frustrated DPS users started to discuss about the future of this project [15], and soon some agreed to create a fork on GitHub [16].

The new repository was created using svn2git [17] by Lex Li and now is hosted on GitHub under dockpanelsuite organization,

https://github.com/dockpanelsuite/dockpanelsuite

Ryan Rastedt purchased the dockpanelsuite.com domain name and designed a new home page [18] for this project.

This organization evaluated and merged many community patches. A few releases, such as 2.6, 2.7, 2.8, and 2.9 have been published in the past few years.

.. [1] http://sourceforge.net/projects/dockpanelsuite/files/DockPanel%20Suite/1.0.0.0/
.. [2] http://sourceforge.net/projects/dockpanelsuite/files/DockPanel%20Suite/2.2/
.. [3] http://www.codeproject.com/Articles/14336/A-Visual-Studio-2005-like-Interface
.. [4] http://www.icsharpcode.net/OpenSource/SD/Default.aspx 
.. [5] http://avalondock.codeplex.com/
.. [6] https://github.com/icsharpcode/SharpDevelop/tree/c4336b038c23fa37ee19bdd7d27bfa29b575a4a4/src/Libraries/DockPanel_Src
.. [7] http://sourceforge.net/projects/dockpanelsuite/forums/forum/402316/topic/3368441
.. [8] http://www.devzest.com/blog/post/WPF-vs-Windows-Forms-From-Control-Authoring-Perspective.aspx
.. [9] http://www.devzest.com/WpfDocking.aspx?Show=Overview
.. [10] http://sourceforge.net/projects/dockpanelsuite/forums/forum/402316/topic/3879095
.. [11] http://sourceforge.net/projects/dockpanelsuite/files/DockPanel%20Suite/2.3.1/ 
.. [12] https://sourceforge.net/news/?group_id=110642
.. [13] http://sourceforge.net/projects/dockpanelsuite/files/DockPanel%20Suite/2.4.0/
.. [14] http://sourceforge.net/projects/dockpanelsuite/files/DockPanel%20Suite/2.5.0%20RC1/
.. [15] http://sourceforge.net/projects/dockpanelsuite/forums/forum/402316/topic/5080422
.. [16] http://sourceforge.net/projects/dockpanelsuite/forums/forum/402316/topic/5271451
.. [17] https://github.com/nirvdrum/svn2git
.. [18] http://dockpanelsuite.com