![](https://super.so/icon/light/edit-3.svg)

Vim editor
==========

Project

[![](https://super.so/icon/light/folder-plus.svg)Module1: Linux](https://www.notion.so/Module1-Linux-012f8f8155f745f68053f61714910da8)

Area

https://www.notion.so/db4d3f8fd47546eebe52fe130a4b4108



\-Module1: Linux-

Created Time

@June 29, 2022 12:32 AM

Finished At

@June 29, 2022 1:50 AM

Related to Uni Courses (Active Tasks)

Basics
------

*   install vim `sudo apt install vim`

*   `vim file` opens a file in a `command mode` , in command mode you can’t edit the file, but you can do anything else like navigate, search,delete, undo,…..

*   `vim` `readme.md`
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled.png)
    

*   to insert text type `i` to switch to the insert mode
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%201.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%201.png)
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%202.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%202.png)
    

*   to save the edit we need to go back to common mode first and then exit, to go back to common mode type `esc key` , then type `:wq` (write and quite) to write the changes and quite.
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%203.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%203.png)
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%204.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%204.png)
    

*   if you added some text and you want to quit without saving the changes you made, go to common mode and type `:q!`
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%205.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%205.png)
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%206.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%206.png)
    

*   `vim file` creates a file

Some useful commands/shortcuts
------------------------------

[![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%207.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%207.png)

*   to delete a line you can type `dd` in common mode instead of deleting character by character.

*   to delete next N lines, type `dNd` like deleting next 4 lines `d4d`
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%208.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%208.png)
    

*   to undo type `u`
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%207.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%207.png)
    

*   to jump to the end of the line type capital A `Shift + A` and it will switch to insert mode too.

*   to jump to the beginning of the line type `0`

*   to jump to line number N type NG like jumping to line number 12, type `12G`

*   to search for a word in the file type `/word` and it will find the first match, to go to the next match type `n`, to go to the previous match type `N`
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%209.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%209.png)
    

*   to replace a string who is frequent like nginx with another, type `:%s/stringName/newName` like `:%s/nginx/new-app`
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%2010.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%2010.png)
    
    [![](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%2011.png)](Vim%20editor%20082492737b7240e1b852a1dc8c80b2a5/Untitled%2011.png)