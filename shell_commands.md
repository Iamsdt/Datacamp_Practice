# All shell commands

#### pdw = > current directory

#### ls => list of all files

```
ls -R  => show all realtive path
ls -R -F => absolute path to your home directory to see everything it contains
```



#### cd => navigate path

```
cd ~/../. => take you home, also cd .
cd .. => navigate to base dir
```

Note: (..) always refers to the directory above your current location

#### cp => copy

```
cp shell/note.txt shell/note.bck => make a copy named note.bck
cp shell/note.txt shell/note.bck backup => copy file to backup
```

#### mv => move

```
mv seasonal/summer.csv seasonal/spring.csv backup => move to backup folder
mv course.txt old-course.txt => move and rename
mv note.bck backup/old_note.bck
```

#### rm => delete file

```
rm old_note.bck => delete files
rm backup/note.txt
```

#### rmdir => delete directory

```
rmdir backup => delete if it is empty
```

#### mkdir => create directory 

```
mkdir name => create folder 'name' 
mkdir name/data => create folder inside name directory
```

#### cat => read the file

```
cat note.txt
```

#### less => read file page by page

```
less note.txt
```

note: if you pass multiple file, use :n to next file :p to previous file and :q to quit 

#### head => print first 10 lines

```
head shell_commands.md
head -n 3 note.txt => first 3 line
!head => show previous executed command
```

#### tail => print show tail

```
tail -n +7 seasonal/spring.csv
```

#### man => show manual

```
man cut => show manual for cut
man head
```

#### history => show history

#### grep => search

```
grep apply note.txt => show all the lines contains apply
grep -v apply note.txt => show all lines not contains apply
grep 
```

- `-c`: print a count of matching lines rather than the lines themselves
- `-h`: do *not* print the names of files when searching multiple files
- `-i`: ignore case (e.g., treat "Regression" and "regression" as matches)
- `-l`: print the names of files that contain matches, not the matches
- `-n`: print line numbers for matching lines
- `-v`: invert the match, i.e., only show lines that *don't* match

####  > => copy into other files

```
last -n 5 note.txt > note.bck
cat note.txt > note2.txt
```

copy folder

```
cp Pictures/* shell/name
```

#### | => combined multiple column

```
wc -l seasonal/* | grep total -v | sort -n | head -n 1
=> select all files from seasonal
 - filter contains total
 - sort
 - select head only 1
```

### Looping for

```1
for filetype in docx odt pdf; do echo $filetype; done
for filename in people/*; do echo $filename; done
```

```
files=seasonal/*.csv
for f in $files; do echo $f; done
for file in seasonal/*.csv; do grep 2017-07 $file | tail -n 1; done
```

#### nano => edit files

```
nano note.txt
```

click => ctrl + o to save and ctrl + x => exit

#### bash => run bash command

```
create a files, command.sh
for f in name/*; do rm name/$f; done
and save files

bash command.sh
```



