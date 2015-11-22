Existing Themes
===============
By `Lex Li`_

This page shows you what are the existing themes and how to use them.

.. contents:: In this article
   :local:
   :depth: 1

Visual Studio 2003 Theme
------------------------
This is a theme that simulates Visual Studio 2003.

To apply this theme, the following code can be used::

  var theme = new VS2003Theme();
  this.dockPanel.Theme = theme;
  
.. note:: for 2.10 and above, a reference to ``ThemeVS2003.dll`` (from NuGet package `DockPanelSuite.ThemeVS2003 <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2003>`_) is needed.

Visual Studio 2005 Theme
------------------------
This is the default theme of DockPanel Suite. When you create a new instance of ``DockPanel`` class, the dock panel and its contents use this theme automatically.

Visual Studio 2012 Light Theme
------------------------------
This is a theme that simulates Visual Studio 2012 Light. 

.. note:: It is introduced in 2.9 release.

To apply this theme, the following code can be used::

  var theme = new VS2012LightTheme();
  this.dockPanel.Theme = theme;

.. note:: for 2.10 and above, a reference to ``ThemeVS2012Light.dll`` (from NuGet package `DockPanelSuite.ThemeVS2012Light <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2012Light>`_) is needed.

Visual Studio 2013 Blue Theme
-----------------------------
This is a new theme that simulates Visual Studio 2013 Blue. 

.. note:: It is introduced in 2.10 release.

To apply this theme, the following code can be used::

  var theme = new VS2013BlueTheme();
  this.dockPanel.Theme = theme;

.. note:: for 2.10 and above, a reference to ``ThemeVS2013Blue.dll`` (from NuGet package `DockPanelSuite.ThemeVS2013Blue <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2013Blue>`_) is needed.

Switching among Themes
----------------------
The sample project demonstrates how to switch among themes,

https://github.com/dockpanelsuite/dockpanelsuite/blob/master/DockSample/MainForm.cs#L159