# code directory structure

Explain briefly the structure of the directory. What do the different
directories contain.

Some guidelines on writing scripts.

- Scripts should alwas follow a style-guide, so code is more readable and your
  future self or collaborators will understand it easily.
  - [R style guide](https://style.tidyverse.org/)
  - [Python style guide](https://www.python.org/dev/peps/pep-0008/)
  - [shell style guide](https://google.github.io/styleguide/shellguide.html)
- Comment your code, so others know what what your code is doing, what is the
  expected input, and what is the expected output.
- If your code is getting complex and reused regularly, it is time to think
  about writing a package or at least a well maintained script with command line
  arguments and version numbers in a separate repository.
  - Use [semantic versioning](https://semver.org/)
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
