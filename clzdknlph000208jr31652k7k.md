---
title: "Your comprehensive guide to shell scripting"
datePublished: Fri Aug 02 2024 07:06:45 GMT+0000 (Coordinated Universal Time)
cuid: clzdknlph000208jr31652k7k
slug: your-comprehensive-guide-to-shell-scripting
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1722655579145/08ec781e-01c3-449d-abfb-b17c05974d05.jpeg

---

Have you ever wondered what shell scripting is and why it’s so important? When building a website or mobile application, writing code is essential to make it function. But what if you need to automate repetitive tasks on your system? This is where shell scripting comes in handy. By writing a shell script, you can automate various tasks, saving time and effort, and making your workflow more efficient.

And do you know what according to [stackoverflow survey](https://survey.stackoverflow.co/2024/technology#most-popular-technologies-language) shell scripting is used more than java? yes, in a professional level too.

![survey results](https://cdn.hashnode.com/res/hashnode/image/upload/v1722655565721/ebc19deb-6a21-4c5a-8845-a5d3f471c4dc.png)

## Table of contents

- [Your comprehensive guide to shell scripting](#your-comprehensive-guide-to-shell-scripting)
  - [Table of contents](#table-of-contents)
  - [What is shell script?](#what-is-shell-script)
  - [Structure of shell script](#structure-of-shell-script)
    - [Header](#header)
    - [Script](#script)
  - [How to create shell script?](#how-to-create-shell-script)
  - [Let's create a simple shell script](#lets-create-a-simple-shell-script)
  - [Hello world in shell script](#hello-world-in-shell-script)
  - [Running shell script 🏃](#running-shell-script-)
  - [Defining variables in shell script](#defining-variables-in-shell-script)
  - [Passing arguments to shell script 🔑](#passing-arguments-to-shell-script-)
  - [Using Variables in shell script 🔄](#using-variables-in-shell-script-)
  - [Conditions in shell script 🔎](#conditions-in-shell-script-)
  - [Loops 🔁](#loops-)
  - [Functions 🔨](#functions-)
  - [Debugging the shell script](#debugging-the-shell-script)
  - [Note](#note)
  - [Arrays in shell script](#arrays-in-shell-script)
  - [Importing files in shell script](#importing-files-in-shell-script)
  - [Wrapping up 🎉](#wrapping-up-)

## What is shell script?

Shell script is a scripting language ( programming language) that can be used to automate task in you system via command line interface.

So let's start learning shell scripting.

## Structure of shell script

Every shell script has 2 parts

- Header
- Script

### Header

- In header we define in which shell the script should be executed. like `sh`, `bash`, `fish` or any other [shell](https://simple.wikipedia.org/wiki/Unix_shell#:~:text=command%2Dline%20interpreter%20for%20Unix,ls%20to%20list%20files).
- The header is optional, but it is recommended to use it.
- If you do not defined header, it will be default to the default shell of the operating system in which the script is executed.
- To know which shell is default in the system, type `echo $SHELL` in your terminal.
- To define header, the syntax is as below.

```sh
#!/bin/sh
```

- `#!/bin/sh` is the header.
- The `#!` is called [shebang](https://en.wikipedia.org/wiki/Shebang_(Unix)).
- and `/bin/sh` where shell is located, most probably all the shells are located in `/bin` directory, unless you are unlucky enough to work on some tricky system.

### Script

- The script is bunch commands that you want to execute line by line.

## How to create shell script?

- When you work with languages like `javascript`, `python` or `java`, you can write a script and save it in a file like `script.js`, `script.py` or `script.java`.
- Same as above, shell script has extension `.sh` and you can write your script in it.

## Let's create a simple shell script

- Open your terminal and type `touch script.sh` to create a file.

![create script.sh](https://cdn.hashnode.com/res/hashnode/image/upload/v1722655567157/17579889-78b1-4357-ad75-72d0b9d4a69c.png)


- It will create a file called `script.sh` in your current directory.
- Now open the favorite editor and we will write some script to execute in terminal, I use [vscode](https://code.visualstudio.com/), you can use any editor of your choice.

## Hello world in shell script

- Let's print hello world in terminal.
- Just type `echo hello world` in the file you have created and save it.

## Running shell script 🏃

- Now you might be wondering how to run this script?
- Your shell can run this script by typing `./script.sh` in your terminal, as shown below.
![run script.sh](https://cdn.hashnode.com/res/hashnode/image/upload/v1722655569415/91821e00-3900-4506-a8b8-a674838ad1f0.png)


- Now you might get an error like `permission denied: ./script.sh`, because by default shell scripts are not executable, we need to make it executable.
- To make it executable type `chmod +x ./script.sh` in the terminal.
![Image description](https://cdn.hashnode.com/res/hashnode/image/upload/v1722655570928/30ed9963-19c7-4c31-8028-bb0fbab87645.png)

- Now you can run the script by typing `./script.sh` in the terminal, and you will get the output as hello world.
![running script.sh](https://cdn.hashnode.com/res/hashnode/image/upload/v1722655573018/44c69a00-277b-42f2-965b-4a41de5fc75f.png)



## Defining variables in shell script

- Same as other programming languages, shell script also has variables.
- To define a variable see the syntax below.

```sh
#!/bin/sh

# define variables
name="Bhoomit"
```

- To access the variable, we use `$` and the name of the variable.
  
```sh
#!/bin/sh

# define variables
name="Bhoomit"

# access variables
echo $name
```

- It will print `Bhoomit` in the terminal.

## Passing arguments to shell script 🔑

- Now let's pass some input to the script.
- This input is known as arguments.
- To pass arguments to the script, type `./script.sh message1` in the terminal.
- And to access the arguments in the script we can use $1 and $2 and so on.
- We do not have named arguments in shell script, so we use $1 and so on ( we will also use this in next section as well).
- To accept arguments in shell script, we need to define the arguments in the header of the script.
- The syntax is as below.

```sh
#!/bin/sh
# define arguments
echo $1;
```

- This will print the first argument in the terminal.
![variable output](https://cdn.hashnode.com/res/hashnode/image/upload/v1722655574342/ae4d4965-136f-4040-bb37-965b477557c3.png)


- If we need to pass something like `hello world` as an argument, we need to wrap it in quotes, else it will be treated as multiple arguments.

## Using Variables in shell script 🔄

- Now we know that we can pass input to the script, let's store them in variable and print the variables.
- To define variable the syntax is as below.

```sh
#!/bin/sh
message=$1;

echo $message;
```

- This will print the first argument in the terminal.
- We can also use this variable in string, like string interpolation.

```sh
echo "Message is $message";
```

- Make sure to use double quotes in the string interpolation, else it will print the variable as it is.

## Conditions in shell script 🔎

- Now that we know we can pass arguments and store them in variable, now let's check if passed argument is valid or not, but using if else condition.
- The syntax for if else condition is as below.

```sh
if [ CONDITION ]
then
    CODE TO BE EXECUTED IF CONDITION IS TRUE
else 
    CODE TO BE EXECUTED IF CONDITION IS FALSE
fi
```

- In some places use will see `[[ CONDITION ]]` instead of `[ CONDITION ]`, it also works but if you wish to improve portability of scripts use single square brackets, as these are inbuilt and older than `[[`.

- Now let's check if passed arguments in the script is empty or not, check the code below.

```sh
#!/bin/sh
message=$1;

if [ -z $message ]
then
    echo "Invalid message!";
else
    echo "Message is $message";
fi
```

- In above code the `-z` operator is used to check if the variable is empty or not, there are many more like `-n`, `-eq`, `-ne`, `-lt`, `-le`, `-gt`, `-ge` and so on.
- I have created a [github gist](https://gist.github.com/bhumit070/707c5225eab7728631537e954a4bd439) for common operators in shell scripting.
- Now I will leave it on you to search for how to use `else if` and `switch case` in shell scripting.

## Loops 🔁

- Sometimes in shell script we need to perform some simple task multiple times, and at that time loops can be your friend.
- There are 4 types of loops in shell scripting.
  1. While
  2. For
  3. Until
  4. Select

- Each loop has it's own syntax but the structure remains same

```sh
LOOP_NAME CONDITION
do
    CODE TO BE EXECUTEED
done
```

- Now let's see the example of for loop.

```sh
#!/bin/bash

for file in "$PWD"/*
do
    echo "Processing file: $file"
done
```

- In above example we are looping through all the files in the current directory and printing the file name.
- The `$PWD` is a shell built-in variable that holds the current working directory.
- The `*` is a wildcard that matches any sequence of characters.
- The `do` keyword is used to start the loop and `done` is used to end the loop.
- We can also use `break` keyword to exit the loop and `continue` keyword to skip the current iteration.
- Here is example of that in for loop.

```sh
#!/bin/bash

for file in "$PWD"/*
do
    if [[ $file == *".skip" ]]; then
        continue  # Skip files with ".skip" extension
    fi

    echo "Processing file: $file"

    if [[ $file == *".stop" ]]; then
        break  # Stop processing if file has ".stop" extension
    fi
done
```

- I have created a [github gist](https://gist.github.com/bhumit070/6285ed8cdbadf82a36b1d40d8161f2fc) for other loop examples in shell scripting.

## Functions 🔨

- Functions are way to reuse code all the programming languages, now let's see how we can create a function in shell scripting.

```sh
#!/bin/bash

# Define a function

greet() {
    echo "Hello, How are you?"
}
```

- In above example we have defined a function named `greet` that prints `Hello, How are you?` in the terminal.
- In shell scripting we do not have to write `function` keyword or `def` or something else to defined it as a function.
- Now to call the function we use `function name` to call the function as shown below.

```sh
#!/bin/bash

greet
```

- Now when you will build real shell script, you might be wondering how to pass arguments to the function? Well we can pass arguments to the function in the same way we pass arguments to the script.
- To pass arguments to the function we use `$1`, `$2` and so on.
- Let's see how we can achieve this in the script.

```sh
#!/bin/bash

greet() {
    message=$1

    if [ -z $message ]; then
        message="How are you?"
    fi

    echo "Hello, $message"
}

greet "Bhoomit"

```

- Now if you pass arguments to the function, `greet "Bhoomit"` it will print as expected.
- But what if we want to pass arguments to the function via script?, we can't be doing `greet $1 $2` and so on, it is tedious and error prone.
- To overcome this problem we can use we can call function like this `greet "$@"` and it will pass all the arguments to the function.
- Now the one more issue you might encounter is if you define message variable in the function, it will be accessible in the function and outside the function.
- To solve this issue we can use `local` in front of the variable so it will be local to the function only.

```sh
#!/bin/bash

localVariables() {
    local message=$1

    # other code
}
```

- Note: If you use `local` outside function body, it will give error.

## Debugging the shell script

- Sometimes the code is against us, and does not work as expected, nah it's not code never lies, and it would be some mistake in the code, but how do we debug that?
- To debug the shell script you can use `echo` statement to print but the funny thing is that the shell script will continue to execute even if it encounters an error.
- To debug the shell script we can use `set -x` to print the commands before executing them.
- It will show you how the script is executing and what is the output of the commands, something like this.
![debugging shell script](https://cdn.hashnode.com/res/hashnode/image/upload/v1722655576191/862fd827-e473-43aa-b556-0e28b2ee4daa.png)


- Now that's cool but what if we want to terminate the script on error?
- Well we can use `set -e` to terminate the script on error.
- It will show you the error and exit the script.
![stop on error](https://cdn.hashnode.com/res/hashnode/image/upload/v1722655577594/1b1ac548-4a63-41ae-b748-7e75199647d5.png)


- It will stop on error but it will not stop if it encounters an undefined variable, to stop this on undefined variable we can use `set -u`.
- Note: There can be many ways you can shoot yourself in the foot, so I highly recommend to use `set -u`, because sometimes undefined variables can make a lot of mess.
- Check this [github issue](https://github.com/ValveSoftware/steam-for-linux/issues/3671#issuecomment-70161790) Where steam tries to delete everything on system due to undefined variable.

## Note

- The above things are more than enough to do shell scripting.
- And if you are using below features of shell script, I would highly recommend to move to any other language to perform the tasks like `js`, `python` or `golang` or any other language of your choice.
- Unless you are working on some tricky system, where only shell scripting can be used, or you are maintaining [dotfiles like me](https://github.com/bhumit070/dotfiles).

## Arrays in shell script

- Same as other programming languages, in shell script we can also use arrays.
- To define an array in shell script the syntax is as below.

```sh
#!/bin/sh

# define array
array=("January" "February" "March" "April" "May" "June" "July" "August" "September" "October" "November" "December")

# access array
echo ${array[0]}
```

- To access the array we use `${array[index]}` and the index of the array.
- Also we can use `${array[@]}` to access all the elements of the array, and it will print all the elements in the terminal.
- We can also use `for` loop to iterate through the array.

```sh
#!/bin/sh

# define array
array=("January" "February" "March" "April" "May" "June" "July" "August" "September" "October" "November" "December")

# loop through array
for element in "${array[@]}"
do
    echo $element
done
```

## Importing files in shell script

- Now it is common to split the code in multiple files and import them in the main script.
- Let's say we have multiple files like this.
  - script.sh
  - functions.sh
  - variables.sh
- `script.sh` is main script and `functions.sh` has functions and `variables.sh` has variables.
- now to import the files we can use `source` keyword, as shown below.

```sh
#!/bin/sh

# script.sh

source ./variables.sh
source ./functions.sh

functionFromFunctionsFile

```

```sh
#!/bin/sh

# functions.sh

functionFromFunctionsFile() {
    echo $variableFromVariablesFile
}
```

```sh
#!/bin/sh

# variables.sh
variableFromVariablesFile="Hello, World!"
```

- If you run the `script.sh`, the final output should be `Hello, World!`.

## Wrapping up 🎉

- Now that you have super power of shell script, just remember to use it wisely, because with great power comes great responsibility.
- This is all the things that I have learned in shell scripting, and I hope you have learned something new too.

- Connect with me on other platforms as well.
  - [Linkedin](https://www.linkedin.com/in/bhoomit-ganatra/)
  - [Twitter](https://twitter.com/bhumit070)
  - [Github](https://github.com/bhumit070)
