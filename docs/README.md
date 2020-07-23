# docs directory structure

Explain briefly the structure of the directory. What do the different
directories contain.

```
metadata/
notebook/
results/
```

The `metadata/` and `notebook/` directories will only contain small files.
However, the `results/` directory might contain analysis results that are still
to large to store on github. Alternatives:

- Store almost everything on github, but use
  [git-lfs](https://git-lfs.github.com/). Only the very large files, like fastq
  files, alignments, genome indexes, etc are not stored here.
- Store most results in `data/`, update `.gitignore` accordingly, and put only
  smaller files here (smaller than 1MB or similar).
