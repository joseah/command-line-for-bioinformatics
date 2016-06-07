---
title: Basic command-line utilities
extensions: supscript
---

# System commands

Get name of host (server)

```bash
hostname
```

Get username

```bash
whoami
```


Get working directory

```bash
pwd 
```

Show current running processes

```bash
top	
```

Show content (files and directories) in current directory

```bash
ls
```

```bash
ls -l
ls -la
ls -lah
ls -lahr
```


Change to parent directory

```bash
cd ..
```




Change to a directory

```bash
cd directory
```

Create a directory

```bash
mkdir new_directory
```

Change name to a file

```bash
mv oldfile newfile
```

Change name to a directory

```bash
mv old_folder new_folder
```

# Permissions 

Change permissions to file 

```bash
chmod 777 myfile
```
> This command sets to all users permissions to read, write and execute `myfile`


# Text files


Create an empty file

```bash
touch test.txt
```

File editor

```bash
nano test.txt
```

Terminal pagers

- more
- less

```bash
more text.txt
less text.txt
```

# Text manipulation


## cut

Get second column of a file

```bash
cut -f2 newEx.map
```

```bash
cut -f1,2 newEx.map
```

> `cut` assumes all columns are tab-separated. 

`-d` parameter is used to indicate the delimiter

```bash
cut -f1,2 -d' ' myfile.txt
```

In this case we use a whitespace as delimiter.


## grep

`grep` searches for pattern in a file and returns all lines where the pattern was found.


```bash
grep "Jose" myfile.txt
```

With `-v` parameter, `grep` returns all lines where the pattern was **not** found.

```bash
grep -v "Jose" myfile.txt
```

The pipe operator `|` can be used to indicate an **OR** statement.

```bash
grep 'Salazar\|Maria' myfile.txt
```

`-w` command searches for exact patterns

```bash
grep -w "22" newEx.map
```

## sed

`sed` command can be used to substitute text


Substitute **first** occurrence of `apple` by `red`

```bash
sed 's/apple/red/' myfile.txt
```

Substitute **all** occurrence of `apple` by `red`

```bash
sed 's/Jose/Juan/g' myfile.txt > output
```

# Combine commands

We use the `|` operator to combine commands.

```bash
grep 'fruit' list_of_fruits.txt | grep 'apple'
```


# Save output of commands

We use the `>` operator to redirect the output to a file

Example:

```bash
sed 's/apple/red/' list_of_fruits.txt > file.txt
```


pandoc terminal_notas.md -o commands.html -c /Users/joseah/Dropbox/Info\ científica/Proyectos/Ancestria/Reportes/PrimeraFase/report_3.css --self-contained --standalone -N --self-contained --table-of-content








