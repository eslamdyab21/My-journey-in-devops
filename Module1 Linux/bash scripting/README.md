![](https://super.so/icon/light/edit-3.svg)

bash scripting
==============

Project

[![](https://super.so/icon/light/folder-plus.svg)Module1: Linux](https://www.notion.so/Module1-Linux-012f8f8155f745f68053f61714910da8)

Area

https://www.notion.so/db4d3f8fd47546eebe52fe130a4b4108


ID

\-Module1: Linux-

Created Time

@June 29, 2022 6:20 PM

Finished At

@June 29, 2022 11:57 PM

Related to Uni Courses (Active Tasks)

[Variables](#Variables)

[Conditions](#Conditions)

[Numeric compactors](#90725ef0-b056-49c9-bbcd-4a1cc42752fe)

[String operations](#b99b9d61-2b57-4696-b700-1a1bd96e7c5e)

[Passing arguments to a script](#25368090-6f2d-4aac-a364-8df251908143)

[Reading user input](#29cb6cd4-a09b-4600-b2de-cf8b39358e51)

[Loops](#2bdd13f6-5cb7-4cec-a63b-7829cc87681d)

[Functions](#6db1a98f-b7a7-4ff3-963f-2a99621f3afa)

*   it’s a way to execute more than one command together. the commands are written in bash files [`file.sh`](http://file.sh) , the first line (shebang #!) must reference the bash location, by default it’s `#!/bin/bash` . to run the bash file: `./file.sh` or `bash file.sh`
    
    [![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled.png)
    
    [![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%201.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%201.png)
    


### Variables

*   `file_name= config.yaml` variable in bash

*   `files = $(ls p0)` save the output of a command to a variable

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%202.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%202.png)

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%203.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%203.png)

### Conditions

    if [condition]
    then
    	statement
    else
    	statement
    fi

    #!/bin/bash
    echo "this isthe first line command in bash"
    
    file_name=config.yaml
    
    if [ -d "config" ]
    then
       echo "reading config directory conternt"
       config_files=$(ls config)
    else
       echo "config dir not found, creating one"
       mkdir config
    fi
    
    
    
    echo "using file $file_name to configure something"
    
    echo "here are all files inside config dir: $config_files"

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%204.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%204.png)

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%205.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%205.png)

`-d` in if condition is a `file test operator` which checks if a directory exists or not. And there are other test operators:

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%206.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%206.png)

### Numeric compactors

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%207.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%207.png)

*   `if [ “$num_files” -eq 10]`

### String operations

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%208.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%208.png)

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%209.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%209.png)

### Passing arguments to a script

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2010.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2010.png)

    #!/bin/bash
    
    file_name=$1
    
    config_dir=$2
    
    echo "-----------------"
    if [ -d "$config_dir" ]
    then
       echo "reading config directory conternt"
       config_files=$(ls $config_dir)
    else
       echo "config dir not found, creating one"
       mkdir $config_dir
       touch $config_dir/config.sh
       config_files=$(ls $config_dir)
    fi
    
    
    echo "-------------------"
    echo "using file $file_name to configure something"
    echo "-------------------"
    
    echo "here are all files inside config dir: $config_files"

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2011.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2011.png)

*   there are two special parameters which allow us to store all the user input parameters `$*`, and their number `$#`
    
    [![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2012.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2012.png)
    
    [![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2013.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2013.png)
    

### Reading user input

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2014.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2014.png)

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2015.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2015.png)

### Loops

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2016.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2016.png)

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2017.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2017.png)

*   loop with if
    
    [![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2018.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2018.png)
    
        #!/bin/bash
        echo "all params: $*"
        echo "number of params: $#"
        echo " "
        
        for param in $*
        do
          if [ -d "$param" ]
          then
            echo "$param is a directory, printing its content: "
            ls $param
            echo " "
          fi
        done
    
    [![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2019.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2019.png)
    

*   while
    
    [![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2020.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2020.png)
    
        #!/bin/bash
        
        sum=0
        while true
        do
           read -p "enter a score: " score
        
           if [ "$score" == "q" ]
           then
              echo " "
              echo "Quiting....."
              break
           fi
        
           sum=$(($sum+$score))
           echo "total score: $sum"
        done
    
    [![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2021.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2021.png)
    
    note that in line 17 `sum=$(($sum+$score))` if we typed it like this `sum=$sum+$score` it will concatenate two strings
    

### Functions

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2022.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2022.png)

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2023.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2023.png)

ex2

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2024.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2024.png)

    #!/bin/bash
    
    function sum(){
       total=$(($1+$2))
       return $total
    }
    
    sum 2 10
    result=$?
    # above two lines same as result=$(sum 2 10)
    
    echo "2 + 10 = $result"
    echo " "
    echo "----------------------------"
    
    
    function create_file() {
       file_name=$1
       is_shell_script=$2
    
       touch $file_name
       echo " file $file_name created"
    
       if [ "$is_shell_script" = true ]
       then
          chmod u+x $file_name
          echo "added execute permission"
       fi
       echo " "
    }
    
    create_file test.txt
    create_file con.yaml
    create_file script.sh true

[![](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2025.png)](bash%20scripting%20b7a47a71b7d44daba964b04294207d81/Untitled%2025.png)