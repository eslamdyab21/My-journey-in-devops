![](https://super.so/icon/light/edit-3.svg)

Pipelines
=========

Project

[![](https://super.so/icon/light/folder-plus.svg)Module1: Linux](https://www.notion.so/Module1-Linux-012f8f8155f745f68053f61714910da8)

Area

https://www.notion.so/db4d3f8fd47546eebe52fe130a4b4108


\-Module1: Linux-

Created Time

@June 29, 2022 4:17 PM

Finished At

@June 29, 2022 5:25 PM

Related to Uni Courses (Active Tasks)

*   in linux commands, the output of one command can be the input to another command. This is known as piping

Pipelines with less
-------------------

for example `cat /var/log/syslog` output the log data in the shell directly, but it’s not user friendly because it outputs all the data in one big page.

a tool called `less` can take this data and displays it in different pages making it easier to read.

[![](Pipelines%20667fbf3d2255461e860716383752e565/cat_logg.gif)](Pipelines%20667fbf3d2255461e860716383752e565/cat_logg.gif)

*   `cat /var/log/syslog | less` pipline that pass the output of cat to the input to less
    
    [![](Pipelines%20667fbf3d2255461e860716383752e565/cat_log_less.gif)](Pipelines%20667fbf3d2255461e860716383752e565/cat_log_less.gif)
    
    type `q` to quite, `b` to navigate up, `space` to navigate down
    

*   `history | less`
    
    [![](Pipelines%20667fbf3d2255461e860716383752e565/history_less.gif)](Pipelines%20667fbf3d2255461e860716383752e565/history_less.gif)
    

Pipelines with grep
-------------------

*   `history | grep “sudo chmod”` filter the history to find lines which have “`sudo chmod`” in them.
    
    [![](Pipelines%20667fbf3d2255461e860716383752e565/Untitled.png)](Pipelines%20667fbf3d2255461e860716383752e565/Untitled.png)
    

*   `history | grep sudo | less`
    
    [![](Pipelines%20667fbf3d2255461e860716383752e565/grep_less.gif)](Pipelines%20667fbf3d2255461e860716383752e565/grep_less.gif)
    

*   `cat README-cloudshell.txt | grep cloud`
    
    [![](Pipelines%20667fbf3d2255461e860716383752e565/grep_cloud.gif)](Pipelines%20667fbf3d2255461e860716383752e565/grep_cloud.gif)
    

Redirecting
-----------

*   `history | grep sudo > sudo-commands.txt`
    
    [![](Pipelines%20667fbf3d2255461e860716383752e565/redirect.gif)](Pipelines%20667fbf3d2255461e860716383752e565/redirect.gif)
    

if we want to append to a copy of `sudo-commands.txt`,

*   `history | grep tom` `>>` `sudo-tom-commands.txt`
    
    [![](Pipelines%20667fbf3d2255461e860716383752e565/tom.gif)](Pipelines%20667fbf3d2255461e860716383752e565/tom.gif)
    

💡

Note: the above methods are useful in a scenario when we filter the log file for a particular application and direct/save this log info to a file to share with someone for troubleshooting

*   `ls; sleep 2; echo "Hi after waiting and ls”`
    
    [![](Pipelines%20667fbf3d2255461e860716383752e565/sleep.gif)](Pipelines%20667fbf3d2255461e860716383752e565/sleep.gif)
    
    those commands are independent of each other, no piping no redirecting