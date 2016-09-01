Basics
======

By `Lex Li`_

This page shows you the basics about DockPanel Suite themes. 

.. contents:: In this article:
  :local:
  :depth: 1

The Structure of A Theme
------------------------
A theme is a collection of multiple elements which control the rendering effect of DockPanel Suite.

.. code-block:: csharp
  
  public class VS2012LightTheme : ThemeBase
  {
      public VS2012LightTheme()
      {
          Skin = CreateVisualStudio2012Light();
      }
  }

Every themes should be derived from an abstract class of ``ThemeBase``, and initialize its skin in the 
constructor.

.. code-block:: csharp

  public static DockPanelSkin CreateVisualStudio2012Light()
  {
      var skin = new DockPanelSkin();

      skin.ColorPalette.MainWindowActive.Background = ColorTranslator.FromHtml("#FFEFEFF2");

      skin.ColorPalette.AutoHideStripDefault.Background = ColorTranslator.FromHtml("#FFEFEFF2");
      skin.ColorPalette.AutoHideStripDefault.Border = ColorTranslator.FromHtml("#FFCCCEDB");
      skin.ColorPalette.AutoHideStripDefault.Text = ColorTranslator.FromHtml("#FF444444");

      skin.ColorPalette.AutoHideStripHovered.Background = ColorTranslator.FromHtml("#FFEFEFF2");
      skin.ColorPalette.AutoHideStripHovered.Border = ColorTranslator.FromHtml("#FF007ACC");
      skin.ColorPalette.AutoHideStripHovered.Text = ColorTranslator.FromHtml("#FF0E70C0");

      return skin;
  }

``DockPanelSkin`` was a simple container of different kinds of colors. It was mainly developed for 
Visual Studio 2005 theme. 2.11 release introduces the new palette based skins, which makes creating 
new themes much easier.

Themes should implement one method so DockPanel Suite can apply them on demand,

.. code-block:: csharp

  public override void Apply(DockPanel dockPanel)
  {
      Measures.SplitterSize = 6;
      dockPanel.Extender.DockPaneCaptionFactory = new VS2012DockPaneCaptionFactory();
      dockPanel.Extender.AutoHideStripFactory = new VS2012AutoHideStripFactory();
      dockPanel.Extender.AutoHideWindowFactory = new VS2012AutoHideWindowFactory();
      dockPanel.Extender.DockPaneStripFactory = new VS2012DockPaneStripFactory();
      dockPanel.Extender.DockPaneSplitterControlFactory = new VS2012DockPaneSplitterControlFactory();
      dockPanel.Extender.DockWindowSplitterControlFactory = new VS2012DockWindowSplitterControlFactory();
      dockPanel.Extender.DockWindowFactory = new VS2012DockWindowFactory();
      dockPanel.Extender.PaneIndicatorFactory = new VS2012PaneIndicatorFactory();
      dockPanel.Extender.PanelIndicatorFactory = new VS2012anelIndicatorFactory();
      dockPanel.Extender.DockOutlineFactory = new VS2012DockOutlineFactory();
      Skin = CreateVisualStudio2012Light();
  }

The ``DockPanel`` class allows its rendering effect to be further changed by overriding properties of its 
``Extender`` property. The above sample shows that multiple elements are customized,

* DockPaneCapture
* DockPaneStrip
* DockPaneSplitter
* AutoHideStrip
* AutoHideWindow
* DockWindow
* DockWindowSplitterControl
* DockOutline
* PaneIndicator
* PanelIndicator

``Measures`` stores several numbers that control size/length of a few controls. ``SplitterSize`` is here to 
control the size of splitters.

``CleanUp`` method should be implemented if a customized ``IPaintingService`` implementation is used 
to clean up GDI+ resources.

You can refer to each of the factory classes to see how a specific part of the theme is customized. Below 
we will simply check what exactly the above names are there in a theme by highlighting them in screen shots.

Visual Elements of A Theme
--------------------------
Here is a full screen shot of an application that uses DockPanel Suite.

.. image:: _static/full.png

So generally speaking, such an application employs multiple dock panes, which are highlighted,

.. image:: _static/panes.png

You can see five panes are there and between panes, splitters are rendered.

A simple pane (such as pane 2 and 5) only contains a single dock content, but a complex pane (such as pane 
1 and 4) can contains multiple dock contents. 

For document panes, their strips (shown in red rectangle below) contain the tabs of the documents and are 
rendered at top, where clicking on a tab can switch to a document,

.. image:: _static/document_pane.png

For tool panes, their strips (shown in blue rectangle below ) contain the tabs of the tools and are rendered 
at bottom, where clicking on a tab can switch to a tool,

.. image:: _static/tool_pane.png

However, tool panes also have their captions (shown in red rectangle above), where the tool can be closed 
or hidden.

When a visible tool pane becomes auto-hide, it would be rendered as an auto-hide strip,

.. image:: _static/autohide_strip.png
  :width: 226

When this auto-hide tool pane is activated, it slides out and shows an auto-hide window,

.. image:: _static/autohide_window.png

When a dock content is dragged and move over the dock panel area, indicators are displayed to show where 
it can be dropped,

.. image:: _static/dock_indicator.png

It is very important to understand such elements and then you can see how the Extender mechanism works.

Related Resources
-----------------

- :doc:`/getting-started/installing-on-windows`
- :doc:`/tutorials/basics`
- :doc:`/themes/creating-new-theme`
- :doc:`/themes/existing-themes`
