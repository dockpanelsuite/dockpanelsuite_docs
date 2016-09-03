Creating A New Theme
====================
By `Lex Li`_

This page shows you how to create a new theme.

.. contents:: In this article
   :local:
   :depth: 1

New Themes in Incubation
------------------------
Lex Li has `a few blog posts <https://blog.lextudio.com/category/dockpanel-suite/>`_ on theming when he attempted 
to integrate the VS 2012 Light theme to the code base, which might get you started.

The following themes are currently under development (mainly contributed by community members),

* Visual Studio 2013 Blue
* Visual Studio 2013 Light
* Visual Stuido 2013 Dark

Please join the `GitHub issue <https://github.com/dockpanelsuite/dockpanelsuite/issues/316>`_ if you are 
interested in it.

Start A New Theme
-----------------
Once you know the basics of Visual Studio 2012/2013 themes, it is quite easy to start your own themes. 
Below we show an example of developing a custom Visual Studio 2012 theme based on the Light theme.

#. Open ``ThemeVS2012.csproj``.
#. Copy ``ThemeVS2012\Light`` folder to ``ThemeVS2012\Custom folder``.
#. Copy ``ThemeVS2012\VS2012LightTheme.cs`` to ``ThemeVS2012\VS2012CustomTheme``.
#. Open ``VS2012CustomTheme.cs``, and rename the class to ``VS2012CustomTheme``.
#. Change its color palette to the combination you like.
#. Replace the icons in ``ThemeVS2012\Custom\Resources`` with the version you like.
#. (Optional) Write your own element factory classes and bind them to ``Theme.Extender``.

Once compiled, you get your own theme.

Related Resources
-----------------

- :doc:`/getting-started/installing-on-windows`
- :doc:`/tutorials/basics`
- :doc:`/themes/existing-themes`
