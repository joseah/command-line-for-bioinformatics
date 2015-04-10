# One-liners for exploratory data analysis
--------------
These are some one-liners and commands that I have found useful in bioinformatics and genomics when exploring text files

# Basic commands in unix

## cut

When you have a file separated by a delimiter, use **cut** to get specific columns.
In a separated file by tabs:
If you want to get the first column use
```
cut -f1 filename
```
First 3 columns
```
cut -f1,2,3 filename
```
From column 1 to 5
```
cut -f1-5 filename
```
Get all columns starting from column number 3
```
cut -f3- filename
```
Often, files are not tab-separated. When other delimiter is used, you can specify the delimiter of interest to cut. Use the **-d** option to do this.
Example:
Get first 3 columns separated by spaces
```
cut -f1-3 -d' ' filename
```
## less

When trying to see the content of a file in terminal, use **less** command.

```
less filename
```

> Note:

> - Use \<up\> and \<down\> to scroll or \<RePag\> and \<AvPag\>. You can also use enter to go down.
> - To exit, type \<q\>.
> - Once you typed \<q\>, the prompt will be available again.

## more

Similar to **less**. Displays text files printing their content on the terminal.

```
less filename
```
> Note:

> - Unlike the **less** command, just use \<enter\> to explore the text.
> - Printed text will remain on screen unless **clear** command is used.
