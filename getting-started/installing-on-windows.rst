Installing DockPanel Suite On Windows
=====================================

By `Lex Li`_

This page shows you how to install DockPanel Suite to your project on Windows. 

.. contents:: In this article:
  :local:
  :depth: 1

Install DockPanel Suite via NuGet
---------------------------------

The easiest way to get started building applications with DockPanel Suite is to install via NuGet in the latest version of Visual Studio 2017 (including the free Community edition). 

#. Install Visual Studio 2017.

   Be sure to specify that you include "Windows" and "Web Development".

#. Install latest `NuGet Package Manager <https://docs.nuget.org/consume/installing-nuget>`_ . 

   This will install the latest NuGet tooling.

#. Open/create an empty Windows Forms project.
#. Install DockPanel Suite NuGet packages following `NuGet conventions <https://docs.nuget.org/Consume/Package-Manager-Dialog>`_ . 

   The latest packages can be found at,

   * `Main Library <https://www.nuget.org/packages/DockPanelSuite/>`_ .
   * `VS2003 Theme <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2003/>`_ .
   * (3.1+) `VS2005 Theme <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2005/>`_ .
   * (2.10) `VS2012 Light Theme <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2012Light/>`_ .
   * (2.11+) `VS2012 Themes <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2012/>`_ .
   * (2.10) `VS2013 Blue Theme <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2013Blue/>`_ .
   * (2.11+) `VS2013 Themes <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2013/>`_ .

   .. note:: VS2005 Theme is moved out of main library in 3.1+.

   .. warning:: Theme package version should match main library version
      whenever possible. Otherwise, there can be compatibility issues.

#. Create the ``DockPanel`` control in code and insert to the main form

   .. code-block:: csharp

      public MainForm()
      {
          InitializeComponent();
          
          this.dockPanel = new WeifenLuo.WinFormsUI.Docking.DockPanel();
          this.dockPanel.Dock = System.Windows.Forms.DockStyle.Fill;
          this.Controls.Add(this.dockPanel); 
      }

   .. note:: Latest Visual Studio 2017 loads the controls from NuGet packages, so
      you can also drag ``DockPanel`` control from ``WinFormsUI Components`` tab
      in Toolbox to your form in Visual Studio design view.

#. Create other panels by creating a new ``Form`` or new ``UserControl`` in Visual Studio

   .. code-block:: csharp

      public class NewForm : Form
      {
      
      }

   Change the base type to ``WeifenLuo.WinFormsUI.Docking.DockContent``

   .. code-block:: csharp

      public class NewDockContent : WeifenLuo.WinFormsUI.Docking.DockContent
      {
      
      }
  
#. Show the custom ``DockContent`` in ``DockPanel`` as a document

   .. code-block:: csharp

      public void ShowDockContent()
      {
          var dockContent = new NewDockContent();
          dockContent.Show(this.dockPanel, DockState.Document);
      }

Install DockPanel Suite via Source Code
---------------------------------------
.. note:: This approach requires Visual Studio 2017 and above. Please switch to
   NuGet package approach if you use older VS releases.

DockPanel Suite source code can be directly used in your project. 

#. Download the source code from `GitHub`_ or clone the repo directly.

#. Open/create a empty Windows Forms project in a solution.

#. Add WinFormsUI.csproj in ``WinFormsUI`` directory to your solution.

#. (optional) Add other theme projects such as ThemeVS2003.csproj to your
   solution.

#. Compile the solution and DockPanel Suite controls are automatically added to
   Toolbox panel.

#. Open main form of the empty project, and drag the ``DockPanel`` control from
   Toolbox on to it.

   This will let Visual Studio generate the necessary code.

#. Create other panels by creating new ``Form`` or new ``UserControl`` in
   Visual Studio，

   .. code-block:: csharp

      public class NewForm : Form
      {
      
      }

   Change the base type to ``WeifenLuo.WinFormsUI.Docking.DockContent``

   .. code-block:: csharp

      public class NewDockContent : WeifenLuo.WinFormsUI.Docking.DockContent
      {
      
      }

#. Show the custom ``DockContent`` in ``DockPanel`` as a document,

   .. code-block:: csharp

      public void ShowDockContent()
      {
          var dockContent = new NewDockContent();
          dockContent.Show(this.dockPanel, DockState.Document);
      }

Compile DockPanel Suite from Source Code
----------------------------------------
#. Download the source code from `GitHub`_ or clone the repo directly.
#. Install Visual Studio 2017 (like Community edition) or above.
#. Install .NET Framework 4.0 (or above) if it is not yet installed.
#. Install .NET Framework 3.5.1 if it is not yet installed.
#. Run ``all.bat`` in the source code to start compilation.

If everything works, then the binaries are in the ``bin`` folder.

Related Resources
-----------------

- :doc:`/getting-started/installing-in-visualstudio`
- :doc:`/getting-started/history`
- :doc:`/tutorials/basics`
- :doc:`/themes/existing-themes`

.. _GitHub: https://github.com/dockpanelsuite/dockpanelsuite/releases>
