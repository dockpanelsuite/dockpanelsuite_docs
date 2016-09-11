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

To apply this theme, the following code can be used,

.. code-block:: csharp

  var theme = new VS2003Theme();
  this.dockPanel.Theme = theme;
  
.. note:: For 2.10 and above, a reference to ``ThemeVS2003.dll`` (from NuGet package `DockPanelSuite.ThemeVS2003 <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2003>`_) is needed.

Visual Studio 2005 Theme
------------------------
This is the default theme of DockPanel Suite. When you create a new instance of ``DockPanel`` 
class, the dock panel and its contents use this theme automatically.

Visual Studio 2012 Themes
-------------------------
Three themes are there to simulate Visual Studio 2012 Blue, Light and Dark. 

.. note:: The Light theme is introduced in 2.9 release. The Dark theme is introduced in 2.11 release.

To apply the Blue theme, the following code can be used::

.. code-block:: csharp

  var theme = new VS2012BlueTheme();
  this.dockPanel.Theme = theme;

To apply the Light theme, the following code can be used::

.. code-block:: csharp

  var theme = new VS2012LightTheme();
  this.dockPanel.Theme = theme;

To apply the Dark theme, the following code can be used::

.. code-block:: csharp

  var theme = new VS2012DarkTheme();
  this.dockPanel.Theme = theme;

.. note:: For 2.10, a reference to ``ThemeVS2012Light.dll`` (from NuGet package `DockPanelSuite.ThemeVS2012Light <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2012Light>`_) is needed. 

.. note:: For 2.11 and above, a reference to ``ThemeVS2012.dll`` (from NuGet package `DockPanelSuite.ThemeVS2012 <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2012>`_) is needed.

Visual Studio 2013 Themes
-------------------------
Three themes are there to simulate Visual Studio 2013 Blue, Light and Dark. 

.. note:: The Blue theme is introduced in 2.10 release. The Dark and Light themes is introduced in 2.11 release.

To apply the Blue theme, the following code can be used::

.. code-block:: csharp

  var theme = new VS2013BlueTheme();
  this.dockPanel.Theme = theme;

To apply the Light theme, the following code can be used::

.. code-block:: csharp

  var theme = new VS2013LightTheme();
  this.dockPanel.Theme = theme;

To apply the Dark theme, the following code can be used::

.. code-block:: csharp

  var theme = new VS2013DarkTheme();
  this.dockPanel.Theme = theme;

.. note:: For 2.10, a reference to ``ThemeVS2013Blue.dll`` (from NuGet package `DockPanelSuite.ThemeVS2013Blue <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2013Blue>`_) is needed.

.. note:: For 2.11 and above, a reference to ``ThemeVS2013.dll`` (from NuGet package `DockPanelSuite.ThemeVS2013 <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2013>`_) is needed.

Visual Studio 2005 Theme for Multiple UI Threads
------------------------------------------------
This is derived from the default theme of DockPanel Suite. It is released for applications that use multiple UI threads only, so not recommended for general usage.

Switching among Themes
----------------------
The sample project demonstrates how to switch among themes,

https://github.com/dockpanelsuite/dockpanelsuite/blob/master/DockSample/MainForm.cs#L139

Related Resources
-----------------

- :doc:`/getting-started/installing-on-windows`
- :doc:`/tutorials/basics`
- :doc:`/themes/creating-new-theme`
