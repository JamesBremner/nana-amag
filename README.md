# nana-amag

This repository demonstrates building a GUI application with the nana GUI framework using the nana source rather than linking to a pre-built library.

The advantage is that the developer does not need to ensure that the application and the library have been built with the exact same options, defines, flags, compiler and standard libraries.  A glance through the nana forum will show that many difficulties are caused by nana library and application builds with slight differences that cause obscure link errors or, even worse, impossible to track down application crashes.  If the application and the nana code are build together by the same project then these problems cannot occur.

The snag is that the nana source contains a great deal of complex code, which keeps the compiler busy for a significant time.  On my 4 core machine, compiling the nana source takes just under one minute.  I consider this acceptable, especially since there is no extra time required on doing an incremental build following a bug fix or implementation of a minor feature.  It is certainly preferable to spending hours tracking down configuration management issues!

The idea for this approach arose from the SQLite database engine which demonstrates the advantages in a large open source project used widely.

The codeblocks project for building the application is in `build/codeblocks`.  I welcome additional projects, please add them into a folder names `build/your_favourite_ide`.

 
