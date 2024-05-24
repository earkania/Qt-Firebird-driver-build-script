# Qt Firebird driver build script
This explains how to build Qt's Firebird database driver for Windows



qt-cmake -G Ninja C:/Qt/6.7.1/Src/qtbase/src/plugins/sqldrivers -DCMAKE_INSTALL_PREFIX=C:/Qt/6.7.1/mingw_64 -DInterbase_INCLUDE_DIR="C:/interbase/include" -DInterbase_LIBRARY="C:/interbase/lib/fbclient_ms.lib"
