# Author Intrusion Linux Utilities

Linux-based utilities for bootstrapping into and from [Author Intrusion](http://mfgames.com/author-intrusion/). These utilities use a number of Linux-based applications which may be available for Windows, including `awk`, `sed`, `perl`, and `csplit`.

It is intended that this will track changes to Author Intrusion and various utilities will be removed as the main application's CLI can handle the same functionality.

## Tools

* `author-intrusion-to-creole`: Takes the `Content.xml` file of a AI project and converts it into a directory of Creole-based files, splitting on the "Chapter" block type. The first chapter will be `chapter-01.txt` and will incrementally increase until the last chapter. (Uses `bash`, `grep`, `awk`, `perl`, and `csplit`)
* `author-intrusion-from-creole`: Takes a series of ordered Creole files and creates a Content.xml file from them. This assumes that lines starting with "=" are Chapters and all other lines are paragraphs. It does not handle additional metadata at this point. (Uses `perl`)
