Customizing DockContent
=======================

By `Ryan Rastedt`_

This page shows you how to customize ``DockContent``. 

.. contents:: In this article:
  :local:
  :depth: 1

Prevent the DockContent from being closed
-----------------------------------------
To prevent a ``DockContent`` from every being closed, utilize the ``CloseButton`` property. You can also utilize the ``CloseButtonVisible`` property to hide the close button when docked in the ``DockPanel`` control::
  
  public CustomContent : DockContent
  {
      public CustomContent()
      {
          InitializeContent();

          // Prevent this content from being closed
          CloseButton = false;

          // Hide the close button so the user isn't even tempted
          CloseButtonVisible = false;
      }
  }
  
You can also use the ``OnFormClosing`` method to prevent the user from closing under certain conditions that cannot be determined until runtime (for example, showing a dialog box asking the user if they are really sure they wish to close the tab)::

  public CustomContent : DockContent
  {
      protected override void OnFormClosing(FormClosingEventArgs e)
      {
          bool cancel = /* add your closing validation here */;
          e.Cancel = cancel;
          base.OnFormClosing(e);
      }
  }