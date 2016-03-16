Basics
======

By `Lex Li`_

This page shows you the basics about DockPanel Suite. 

.. contents:: In this article:
  :local:
  :depth: 1

Show Contents as Documents
--------------------------
It is quite common to have a list of dock contents shown as a list of documents.

To show a single document, the following code can be used

.. code-block:: csharp

  doc1.Show(dockPanel, DockState.Document);

To show a list of documents in order, the following code can be used,

.. code-block:: csharp

  doc1.Show(dockPanel, DockState.Document);
  doc2.Show(doc1.Pane, null);
  doc3.Show(doc1.Pane, null);
  doc4.Show(doc1.Pane, null);
  
  // reorder doc1 and doc2
  doc1.Show(doc1.Pane, null);
  doc2.Show(doc1.Pane, null);

.. note:: Note that the ``DockContent.Pane`` property is used so that documents are placed in the same dock pane.

Show Multiple Contents in The Same Dock State
---------------------------------------------
By default if two or more dock contents are shown in the same dock state will share the same dock pane and become tabs in that pane.

.. code-block:: csharp

  dmcDownloadMonitor.Show(dockPanel, DockState.DockBottom);
  amcActivateModsMonitor.Show(dockPanel, DockState.DockBottom);

However, sometimes the contents should be placed into different panes and shown side by side. This requires some changes in code,

.. code-block:: csharp

  dmcDownloadMonitor.Show(dockPanel, DockState.DockBottom);
  amcActivateModsMonitor.Show(dmcDownloadMonitor.Pane, DockAlignment.Right, 0.5);

How to Lock Layout and Prevent Dock Panels From Moving
------------------------------------------------------

Lock Entire Layout
^^^^^^^^^^^^^^^^^^
To lock the entire layout, the following snippet can be used to disable all end user docking at ``DockPanel`` level,

.. code-block:: csharp

  dockPanel.AllowEndUserDocking = false;

Lock A Single Panels
^^^^^^^^^^^^^^^^^^^^
To lock only a single panel, the following snippet can be used to disable all end user docking at ``DockContent`` level,

.. code-block:: csharp

  dockContent.DockHandler.AllowEndUserDocking = false;

Avoid A Few Dock States
^^^^^^^^^^^^^^^^^^^^^^^
To prevent a dock panel from entering some dock states, set ``DockContent.DockAreas`` to only the areas that are desired.
