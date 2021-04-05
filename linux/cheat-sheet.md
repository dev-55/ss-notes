# Linux Cheat Sheet

## Packages
To install/remove a package...
```
apt install nano
apt remove nano
```

To list packages in local database...
```
    apt list
```

To update the packages in the local database...
```
    apt update
```

&nbsp;
## File System
![](images/linux-file-system.png?raw=true)

- bin - binaries/programs
- boot - boot-related files
- dev - device-related files
- etc - (editable text configuration) config files
- home - user-specific files
- root - home directory of root user
- lib - software library dependencies
- var - variable - frequenlty updated files - log files, application data
- proc - files for running processes

In Linux, everything is a file - devices, processes, network sockets, etc

&nbsp;
### Navigation
```
    pwd [print working diretory]

    ls [list]
    ls -1 [list, 1 item per line]
    ls -l [list, long (more detail)]
    
    cd ~ [navigate to home directory]
```
&nbsp;
### Manipulating Files/Directories
```
    mkdir newDir
    mv newDir newName [rename directory]
    rm -r newDir [remove directory; -r means recursive]

    touch newFile.txt [creates file]
    touch newFile1.txt newFile2.txt newFile3.txt [creates multiple files]

    mv newFile.txt newFileName.txt [renames file]
    mv newFile.txt /etc [moves file to /etc folder]

    rm newFile.txt [removes a file]
    rm newFile1.txt newFile2.txt newFile3.txt [removes multiple files]
    rm newFile* [removes multiple files]
```
&nbsp;
### Editing/Viewing Files
```
    cat file1.txt [ouputs the file contents to console]
    more longFile.txt [pages the contents of a long file... scroll down only] [q to exit]
    less longFile.txt [pages the contents of a long file... up and down] [less needs to be installed... apt install less]
    head -n 5 longFile.txt [show the first 5 lines]
    tail -n 5 longFile.txt [show the last 5 lines]
    nano [open file editor; needs installed]
```