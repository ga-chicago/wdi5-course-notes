# Creating and Moving Files in the Terminal

## Objectives

- How to rename files/folders
- Move files/copy files
- Delete files and folders
- Create files in 2 ways
- Create folders

## Creating a file

The `touch` command creates new empty files. It takes one argument, name or path of the file to be created. Example:

```
touch ~/Sites/README.md
```

The above command creates a file called `README.md` in the `Sites` folder. You can also create a file in whichever directory you're currently in by running `touch myFile.txt`.

### Another way to make a file

The `echo` command will output text to the terminal.

It works like this: `echo "Some text"`.

When combined with UNIX concepts like piping and redirecting you can redirect the output of `echo` into a file like this: `echo ".DS_Store" > .gitignore`. That command will put the text ".DS_Store" (which is an annoying hidden file OS X puts in folders) into a file called `.gitignore`. If the file doesn't exist it will be created. If the file had already been full of text, the contents of the file would have been replaced with whatever you passed to `echo`. To append some text to the end of a file using echo you use a double angle bracket like thic: `echo "This will go to the end of an existing file" >> .gitignore`.

## Moving Files

The `mv` command will move a file from one place to another. This command can also be used to rename a file. Suppose we have a file called `example.txt` and we wanted to rename it to be a Markdown filewe would use `mv` like this:

```
mv example.txt example.md
```

If we wanted to move the file somewhere else we would do it like this:

```
# Method 1 - Moves the file without renaming
mv example.txt ~/Desktop/

# Method 2 - Moves the file and renames it to "sample.txt"
mv example.txt ~/Desktop/sample.txt
```

## Deleting Files

The `rm` and `rmdir` commands will remove files and folders respectively.

`rm` is made for deleting files. When you `rm` on the command line the file is immediately deleted - it __does not go to the Trash first__. This command cannot be used on folders. The only exception is deleting a folder and all of its contents recursively. To do this, run this command: `rm -rf folder_name_to_delete/`

In the above example the `-rf` flag tells `rm` to recursively remove the files and folders.

`rmdir` will remove folders but only if they're empty. If the folder contains files or other folders then you need to use the `rm -rf` command (the `rm` command with the `rf` flag).

## Try it yourself

1. Create a folder named "zoo"
2. Now add some animals to your zoo. Create text files for these animals:
  - snake.txt
  - spider.txt
  - spider2.txt
  - sloth.txt
  - dolphin.txt
3. All of these animals can't live together in the zoo. Create folders to categorize the animals as:
  - insects
  - reptiles
  - mammals
  - water_animals
4. Now put the animals in their correct folder
5. Uh oh, the spiders got in a fight or mated or something and one ate the other one. Delete the second, eaten spider
