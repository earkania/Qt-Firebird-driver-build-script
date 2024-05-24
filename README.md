# Qt Firebird driver build script
This explains how to build Qt's Firebird database driver for Windows
1. You must install required version of firebird (In my case Firebird 3.0).
2. You must copy your firebird installation content to some simple path witout spaces (I have copied it to "C:\interbase\").
3. You must have "Ninja" installed. You can install it using Qt-s maintenence wizard.
4. You must have installd Qt-s sources. You can install it using Qt-s maintenence wizard.
5. You must edit environment variables on your PC. I have added this records:
  * C:\Qt\6.7.1\mingw_64     - for mingw
  * C:\Qt\Tools\CMake_64\bin - for CMake
  * C:\Qt\Tools\Ninja        - for Ninja
  * C:\interbase             - for Firebird
6. After all above is redy then you must open Qt-s ComandLine and run following commands:

qt-cmake -G Ninja C:/Qt/6.7.1/Src/qtbase/src/plugins/sqldrivers -DCMAKE_INSTALL_PREFIX=C:/Qt/6.7.1/mingw_64 -DInterbase_INCLUDE_DIR="C:/interbase/include" -DInterbase_LIBRARY="C:/interbase/lib/fbclient_ms.lib"
