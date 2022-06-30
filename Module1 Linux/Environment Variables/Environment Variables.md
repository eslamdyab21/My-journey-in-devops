
Environment Variables
=====================

Project

[![](https://super.so/icon/light/folder-plus.svg)Module1: Linux](https://www.notion.so/Module1-Linux-012f8f8155f745f68053f61714910da8)

Area

https://www.notion.so/db4d3f8fd47546eebe52fe130a4b4108


\-Module1: Linux-

Created Time

@June 30, 2022 12:56 AM

Finished At

@June 30, 2022 2:43 AM

Related to Uni Courses (Active Tasks)

[Intro to environment variables](#06251891-7793-493b-b4d0-25ab52db1e38)

[Benefits of environment variables](#73846a41-f4ad-4608-8ce0-c133b653d9a9)

[Operations on environment variables](#d8db585b-d915-4661-9185-645147ed0387)

[The PATH environment variable](#12af4457-e69c-4e4b-abe5-a5447bfc6901)

### Intro to environment variables

*   environment variables are a set of dynamic named values, stored within the system that are used by applications launched in shells. In simple words, an environment variable is a variable with a name and an associated value

*   `printenv` print all system env var
    
    [![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled.png)
    
    [![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%201.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%201.png)
    

*   `printenv VAR` print the value of VAR environment variable
    
    [![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%202.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%202.png)
    

*   environment variables can be accessed by linux programs and commands and also programming languages by typing $ before the variable `$USER` just like in bash script
    
    [![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%203.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%203.png)
    

### Benefits of environment variables

Note that environment variables are not only a way for the os to store some info, it has other important use cases, like when running an application on a linux server which connects to google api, this connection have credentials (username and password).

how can we provide this sensitive credentials info in a secure way? we can’t just put them in our program in plain sight for anyone to see.

[![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%204.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%204.png)

the answer is using environment variables, the application can access the sensitive data without showing them, we create an environment variables for every sensitive data entry.

[![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%205.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%205.png)

also environment variables are used to make applications more flexible

[![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%206.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%206.png)

### Operations on environment variables

*   `export ENV_VAR=value` creating env var

*   `unset ENV_VAR` deletes env var

[![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%207.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%207.png)

💡

Note that if we closed this terminal the created env vars will be gone, to save them permanently we need to add export commands in the `.bashrc` file and then source it.

[![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%208.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%208.png)

[![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%209.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%209.png)

💡

Note that the above `.bashrc` is unique for each user, which means that the env vars we created won’t be accessible by other users. however we can make them global to all users by adding them in the `.bashrc` of the root which is located in `/etc/environment`

### The PATH environment variable

[![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%2010.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%2010.png)

is a list of directories to executable files separated by :

it tells the shell which directories to search for for the executables that we write in our commands

ex: when we type `ls` command, the shell searches in every directory in the PATH env var (every element in the list) until it finds it to execute it.

so if we added a directory of a new created exeuteble file to the PATH env var, we can execute it like `ls` anywhere.

Use case for me will be to save the github token in an env var.

*   Adding a custom command/program to the PATH env var
    
    *   creating the new script
        
        [![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%2011.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%2011.png)
        
    
    *   adding it to the PATH env var
    
    [![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%2012.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%2012.png)
    
    note that we didn’t use export with PATH because it’s already an existing env var, we’re just changing it
    
    [![](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%2013.png)](Environment%20Variables%2083336bedfe134e6b9e98283c61d952fb/Untitled%2013.png)
    

so the benefit here is that instead of specifying the entire path `/home/eslamdyab21/p0/`[`welcome.sh`](http://welcome.sh) we just type `welcome.sh` anywhere