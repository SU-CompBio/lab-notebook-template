# Project title

Recommended structure for bioinformatics projects, and lab notebooks. Work in
progress, comments are welcome.

### Name and University/Institute/Department

Started on: 2021-01-01

Supervisor: Jane Doe at Top University, Important Department

Short summary of the project, with links to additional repositories, software
and databases relevant for the project. The summary should include the
following:

- Main question you are trying to answer. If pigs could fly, would they have
  bat, insect or bird-like wings? What would be their maximum speed?
- The tools and methods you are using to investigate this. CRISPR-editing of pig
  genes, linear modeling in R to find out the relationship between weight and
  maximum speed, field investigations in rural areas. Of course, this will
  change, but a starting set of tools and methods should be mentioned.
- Some background information. What is known in the field, is it a well-studied
  area, or flying pigs are a completely new groundbreaking research topic? Link
  a few reviews, or the paper(s) leading to the main question.

### Repository structure

```
data/
docs/
code/
README.md
LICENSE
.gitignore
```

Explain the content of the `data/`, `docs/` and `code/` directories, and edit
the above block as needed, to include additional top-level directories or files.

Modify `LICENSE` and `.gitignore` as needed.

### Notes

Choose a proper license [here](https://choosealicense.com/), also taking into
account university intellectual rights, your contract, requirements of granting
agencies, etc. Ask your patent office, grant office, etc if unsure.

Update `.gitignore` using
[gitignore.io](https://www.toptal.com/developers/gitignore) and add various file
types based on the languages, tools and operating systems you are using.

[Think about naming](https://speakerdeck.com/jennybc/how-to-name-files)
directories, result files, scripts, figures long and hard. As said elsewhere, if
your names are wrong, your entire life (project) is wrong.

In some cases, countersigning the work might be needed, verifying that the
scripts, documentation, results, figures are correct. A lightweight method would
be git signed tags. See more
[here](https://git-scm.com/book/en/v2/Git-Basics-Tagging) and
[here](https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work). An example:

```sh
git tag -a verified-2021-01-10 -m "Repo checked and verified on 2021-01-10" -s
git push origin --tags
```
