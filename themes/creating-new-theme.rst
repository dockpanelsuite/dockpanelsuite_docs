Creating A New Theme
====================
By `Lex Li`_

This page shows you how to create a new theme.

.. contents:: In this article
   :local:
   :depth: 1

Start A New Theme
-----------------
Once you know the basics of Visual Studio 2012/2013 themes, it is quite easy to start your own themes. 
Below we show an example of developing a custom Visual Studio 2012 theme based on the Light theme.

#. Open Visual Studio 2012 and install Color Theme Manager extension.
#. Create a new theme there and export as a .vstheme file.
#. Open ``ThemeVS2012.csproj``.
#. Put the .vstheme file into ``ThemeVS2012\Resources`` folder and add it to Resources.resx.
#. Copy ``ThemeVS2012\VS2012LightTheme.cs`` to ``ThemeVS2012\VS2012CustomTheme``.
#. Open ``VS2012CustomTheme.cs``, and rename the class to ``VS2012CustomTheme``.
#. Change its constructor to use the .vstheme file from the resources.
#. (Optional) Write your own element factory classes and bind them to ``Theme.Extender`` if you want to further customize rendering effect.

Once the project can compile without an error, you get your own theme ready for testing.

Related Resources
-----------------

- :doc:`/getting-started/installing-on-windows`
- :doc:`/tutorials/basics`
- :doc:`/themes/existing-themes`
