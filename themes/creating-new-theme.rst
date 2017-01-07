Creating A New Theme
====================
By `Lex Li`_

This page shows you how to create a new theme.

.. contents:: In this article
   :local:
   :depth: 1

Start A New Theme (2.11)
------------------------
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

.. note:: If you don't want to use Color Theme Manager, please analyze ``VS2012PaletteFactory`` source code to see from where each colors come.

Once the project can compile without an error, you get your own theme ready for testing.

Start A New Theme (2.12 and Above)
----------------------------------
Once you know the basics of Visual Studio 2012/2013 themes, it is quite easy to start your own themes. 
Below we show an example of developing a custom Visual Studio 2012 theme based on the Light theme.

#. Open Visual Studio 2012 and install Color Theme Manager extension.
#. Create a new theme there and export as a .vstheme file.
#. Use tools such as `7-Zip <http://7-zip.org>`_ to compress the file as .gz.
#. Open ``ThemeVS2012.csproj``.
#. Put the .gz file into ``ThemeVS2012\Resources`` folder and add it to Resources.resx.
#. Copy ``ThemeVS2012\VS2012LightTheme.cs`` to ``ThemeVS2012\VS2012CustomTheme``.
#. Open ``VS2012CustomTheme.cs``, and rename the class to ``VS2012CustomTheme``.
#. Change its constructor to use the .gz file from the resources (``ThemeBase.Decompress`` method decompresses the file at runtime).
#. (Optional) Write your own element factory classes and bind them to ``Theme.Extender`` if you want to further customize rendering effect.

.. note:: If you don't want to use Color Theme Manager, please analyze ``VS2012PaletteFactory`` source code to see from where each colors come.

Once the project can compile without an error, you get your own theme ready for testing.

Related Resources
-----------------

- :doc:`/getting-started/installing-on-windows`
- :doc:`/tutorials/basics`
- :doc:`/themes/existing-themes`
