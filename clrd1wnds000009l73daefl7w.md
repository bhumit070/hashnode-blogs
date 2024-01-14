---
title: "Destiny: A Tool to Manage Cluttered Folders"
seoTitle: "Destiny: A Tool to Manage Cluttered Folders"
seoDescription: "Destiny is a command line tool written in go that simplifies the organization of cluttered folders."
datePublished: Sun Jan 14 2024 05:23:52 GMT+0000 (Coordinated Universal Time)
cuid: clrd1wnds000009l73daefl7w
slug: destiny-a-tool-to-manage-cluttered-folders
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1705209796197/c8db6be4-4e85-4161-8141-27d8c24e52cd.jpeg
tags: go, tooling, cli

---

## Table of Contents

* [Description](#description)
    
* [How to Use](#how-to-use)
    
    * [Installation](#installation)
        
    * [Organizing Files](#organizing-files)
        
* [How it Works](#how-it-works)
    
* [Conclusion](#conclusion)
    

## Description

Destiny is a command line tool written in `go` that simplifies the organization of cluttered folders. If you've ever struggled with maintaining a tidy file system, Destiny is here to make your life easier. Unlike a traditional shell script, Destiny includes checks for excluded files and provides a more manageable and user-friendly experience.

## How to Use

### Installation

If you are on macOS or Linux, use the following command to install Destiny:

```bash
curl https://raw.githubusercontent.com/bhumit070/destiny/main/install.sh | bash
```

### Organizing Files

* To organize files in the current folder, run:
    

```bash
destiny
```

* To organize files in a specific folder, provide the folder path as an argument:
    

```bash
destiny /path/to/folder
```

## How it Works

Destiny employs a simple yet effective approach to file organization:

1. File Scan:
    

* Destiny scans all files in the target folder.
    

1. Folder Creation:
    

* For each unique file extension, Destiny checks if a corresponding folder exists. If the folder does not exist, Destiny creates a folder with the same name as the file extension. File Movement: Destiny moves each file to the folder associated with its file extension.
    

1. Example: If you have a file named hello.txt, Destiny creates a folder named txt (if not exists) and moves the file into it.
    

## Conclusion

Destiny is a user-friendly tool that significantly improves the organization of your files. Whether you're dealing with a cluttered workspace or aiming for a more systematic approach, Destiny has got you covered. For suggestions or feedback, please create an issue on the [GitHub repo](https://github.com/bhumit070/destiny).

Also if you like Destiny, please star the repo.