APPEND
======
Enables programs to open data files in specified directories as if the files were in the current directory.

Copyright 2004-2006 Eduardo Casino, under the terms of the GNU GPL, Version 2


Syntax:
-------

  `APPEND [[drive:]path[;...]] [/X[:ON|:OFF]] [/PATH:ON|/PATH:OFF] [/E]`

  `APPEND ;`

 *   [drive:]path Drive and directory to append.
 *   /X[:ON]      Extend APPEND to searches and command execution.
 *   /X:OFF       Applies APPEND only to requests to open files.
                  Defaults to /X:OFF
 *   /PATH:ON     Searches appended directories for file requests that already
                  include a path.  This is the default setting.
 *   /PATH:OFF    Switches off /PATH:ON.
 *   /E           Stores the appended directory list in the environment.
                  /E may be used only in the first invocation of APPEND. You
                  can not include any paths on the same command line as /E.


-  APPEND ; clears the list of appended directories.
-  APPEND without parameters displays the list of appended directories.


Note:
-----
  APPEND installs itself as an internal command after its first execution.
  Second and successive invocations MUST exclude file path and extension.
