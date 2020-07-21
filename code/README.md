# code directory structure

Explain briefly the structure of the directory. What do the different
directories contain.

Some guidelines on writing scripts.

- Scripts should contain as few hard-coded file paths as possible. If necessary,
  define these as command line arguments or at least put them in a variable at
  the start of the script.

Good

```sh
#!/bin/bash

datadir=$1

# or

datadir='/path/to/data'

for i in `ls $datadir`; do
	# do stuff
done
```

Bad

```sh
#!/bin/bash

for i in `ls /path/to/data`; do
	# do stuff
done
```

- All changes to any kind of data (raw sequencing data, importing and editing
  excel tables, extracting data from pdfs, csv tables, etc) should be done thru
  scripts containing the full command line, steps carried out, modifications,
  corrections of the data. Manual editing of data, for example an excel table,
  is only allowed if there is absolutely no other way. It is better to import an
  excel table into R, and correct problems using R functions, than manually
  editing the excel, saving it and importing the data later.
