# SQLite Build in Visual Studio

I needed a 64 bit Windows DLL of Visual Studio with some compile 
time settings set, and I could not find one - so I made this project.

I am just using the [SQLite Amalgamation](http://www.sqlite.org/download.html).

The current version is 3.8.4.1.

The [compile time options](http://www.sqlite.org/compile.html) set are:
  * SQLITE_API=__declspec(dllexport)
  * SQLITE_ENABLE_FTS4
  * SQLITE_ENABLE_FTS3_PARENTHESIS
  * SQLITE_ENABLE_COLUMN_METADATA

This sets the define needed to export from the DLL, tells
the compiler to include the [Full Text Search 4](http://www.sqlite.org/fts3.html#fts4) in
the build, and includes the additional APIs for meta-data about tables and queries.