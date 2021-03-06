# Linux

#### Filesystem

###### List files
```
ls 
```

###### List files with details
```
ls -l
```

###### List files in reverse order sorted by modification time
```
ls -latr
```

###### Change directory
```
cd <dirname>
```
###### Move back to previous directory
```
cd -
```

###### Copy file1 to file2
```
cp file1 file2
```

###### Create a symbolic link to a file
Symbolic links can point to a file on any volume
```
ln -s file link
```

###### Create a directory
```
mkdir dir1
```

###### Create a directory and its intermediate directories if they don't exist
```
mkdir -p /dir1/dir2/dir3
```

###### Show size of current directory
```
du -sh
```

###### Show size of current directory and all its sub-directories
```
du -sh *
```

#### Process Management

###### List all running processes
```
ps -ef
```

###### Suspend current running job
```
CTRL + Z
```

###### Let suspended job run in the background
```
bg
```

###### List all background jobs
```
jobs
```

###### Move a job (say 2) from the jobs list back to the foreground
```
fg %2
```

###### Move last stopped/background job back to the foreground
```
fg
```

#### Miscellaneous

###### for loop
```
for f in $(ls dir/); do echo $f; done
```

###### Clear terminal screen
```
clear OR [Crtl + l]
```
###### New terminal screen
```
[Crtl + Alt + T]
```
###### Switch terminal tabs
```
[Crtl + PgUp/PgDn]
```
###### Check which shell I'm running
```
echo $SHELL
```

###### Check the exit status of the last run program
```
echo $?
```

###### Check installed services
```
chkconfig --list
```

###### Search and replace a phrase in files
```
sed -i 's/pharase/replacement/g' *
```

###### Create ISO Image
```
genisoimage -o myimage.iso -V MyLabel -R -J /home/source/folder
```
###### Mount ISO
```
mount -o loop /home/myimage.iso /mnt/cdrom
```
###### Print 2 lines before and 3 lines after search match in grep
Alternately, you can use -C to match <n> lines both before and after.
```
cat file | grep -B 2 -A 3 "pattern"
```
###### Recursively change all occurences of a string in multiple files
```
grep -r -l "get-dc-abbr" * | xargs sed -i 's/get-dc-abbr/my-site/g'
```
###### ffmpeg extract mp4 container audio without conversion
```
ffmpeg -i video.mp4 -vn -acodec copy audio.aac
```
