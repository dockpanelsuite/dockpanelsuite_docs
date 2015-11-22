Installing DockPanel Suite On Windows
=====================================

By `Lex Li`_

This page shows you how to install DockPanel Suite to your project on Windows. 

.. contents:: In this article:
  :local:
  :depth: 1

Install DockPanel Suite via NuGet
---------------------------------

The easiest way to get started building applications with DockPanel Suite is to install via NuGet in the latest version of Visual Studio 2015 (including the free Community edition). 

#. Install `Visual Studio 2015 <https://go.microsoft.com/fwlink/?LinkId=532606>`__

  Be sure to specify that you include the Windows and Web Development.

#. Install latest `NuGet Package Manager <https://docs.nuget.org/consume/installing-nuget>`_. 
  
  This will install the latest NuGet tooling.

#. Open/create an empty Windows Forms project.
  
#. Install DockPanel Suite NuGet packages following `NuGet conventions <https://docs.nuget.org/Consume/Package-Manager-Dialog>`_. 

  The latest packages can be found at,
  
  * `Main Library <https://www.nuget.org/packages/DockPanelSuite/2.10.0-beta1>`_.
  * `VS2003 Theme <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2003/2.10.0-beta1>`_.
  * `VS2012 Light Theme <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2012Light/2.10.0-beta1>`_.
  * `VS2013 Blue Theme <https://www.nuget.org/packages/DockPanelSuite.ThemeVS2013Blue/2.10.0-beta1>`_.
    
  *Note that the 2.10 packages are pre-release.*

#. Create the ``DockPanel`` control in code and insert to the main form::

  public MainForm()
  {
      InitializeComponent();
	  
  	  this.dockPanel = new WeifenLuo.WinFormsUI.Docking.DockPanel();
      this.dockPanel.Dock = System.Windows.Forms.DockStyle.Fill;
      this.Controls.Add(this.dockPanel); 
  }
  
#. Create other panels by creating new Form or new UserControl in Visual Studio::

  public class NewForm : Form
  {
  
  }

  Change the base type to ``WeifenLuo.WinFormsUI.Docking.DockContent``::
  
  public class NewDockContent : WeifenLuo.WinFormsUI.Docking.DockContent
  {
  
  }
  
#. Show the custom ``DockContent`` in ``DockPanel`` as a document::

  public void ShowDockContent()
  {
      var dockContent = new NewDockContent();
	    dockContent.Show(this.dockPanel, DockState.Document);
  }
  
Install DockPanel Suite via source code
---------------------------------------

DockPanel Suite source code can be directly used in your project. 

#. Download the source code from `GitHub <https://github.com/dockpanelsuite/dockpanelsuite/releases>`_, or clone the repo directly.

#. Open/create a empty Windows Forms project in a solution.

#. Add WinFormsUI.csproj in ``WinFormsUI`` directory to your solution.

#. (optional) Add other theme projects such as ThemeVS2003.csproj to your solution.
 
#. Compile the solution and DockPanel Suite controls are automatically added to Toolbox panel.

#. Open main form of the empty project, and drag the DockPanel control from Toolbox on to it.

  This will let Visual Studio generate the necessary code.

#. Create other panels by creating new Form or new UserControl in Visual Studio::

  public class NewForm : Form
  {
  
  }

  Change the base type to ``WeifenLuo.WinFormsUI.Docking.DockContent``::
  
  public class NewDockContent : WeifenLuo.WinFormsUI.Docking.DockContent
  {
  
  }
  
#. Show the custom ``DockContent`` in ``DockPanel`` as a document::

  public void ShowDockContent()
  {
      var dockContent = new NewDockContent();
	    dockContent.Show(this.dockPanel, DockState.Document);
  }
  
Related Resources
-----------------

- :doc:`/how-tos/index`