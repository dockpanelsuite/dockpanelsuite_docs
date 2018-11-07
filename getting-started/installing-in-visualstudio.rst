Adding DockPanel Suite to Toolbox in Visual Studio
==================================================

By `Lex Li`_

This page shows you how to install DockPanel Suite to your project on Windows. 

.. contents:: In this article:
  :local:
  :depth: 1

Recommended Steps
-----------------
.. important:: In latest Visual Studio 2017, you don't need the following.
   Please use the NuGet packages according to
   :doc:`/getting-started/installing-on-windows`.

#. Compile DockPanel Suite binaries, according to
   :doc:`/getting-started/installing-on-windows`.
#. Open Visual Studio, and navigate to its Toolbox panel.
#. Expand a tab such as General, or create a new tab by right clicking and
   choosing "Add Tab" menu item.
#. Right click in the tab area and choose "Choose Items..." menu item.
#. Under the ".NET Framework Components" "Choose Toolbox Items" dialog, click
   the "Browse..." button.
#. In the "Open" file dialog, navigate to ``bin\net40`` folder that contains
   the assemblies, and choose all related files,

   * ``WeifenLuo.WinFormsUI.Docking.dll``,
   * ``WeifenLuo.WinFormsUI.Docking.ThemeVS2003.dll``,
   * ``WeifenLuo.WinFormsUI.Docking.ThemeVS2005.dll`` (3.1+),
   * ``WeifenLuo.WinFormsUI.Docking.ThemeVS2012Light.dll`` (2.10),
   * ``WeifenLuo.WinFormsUI.Docking.ThemeVS2012.dll`` (2.11+),
   * ``WeifenLuo.WinFormsUI.Docking.ThemeVS2013Blue.dll`` (2.10),
   * and ``WeifenLuo.WinFormsUI.Docking.ThemeVS2013.dll`` (2.11+).

#. Click the "Open" button to exit the dialog.
#. In ".NET Framework Components" tab, click "Namespace" column header to
   reorder the list.
#. Make sure that "DockPanel", "VS2003Theme", "VS2005Theme", 
   "VS2012LightTheme", "VS2012DarkTheme" (2.11+), "VS2012BlueTheme" (2.11+), 
   "VS2013BlueTheme", "VS2013LightTheme" (2.11+), and "VS2013DarkTheme" (2.11+)
   are checked.
#. Click the "OK" button to exit the dialog.

Related Resources
-----------------

- :doc:`/getting-started/installing-on-windows`
- :doc:`/getting-started/history`
- :doc:`/tutorials/basics`
- :doc:`/themes/existing-themes`
