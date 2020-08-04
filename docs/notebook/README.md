# notebook structure

## Analysis steps

Every `Rmd` or `md` file is a specific analysis, experiment, hypothesis.
Alternatively every file is a specific day/week. These notebooks should contain
the actual experiments, analysis steps, tests carried out, intermediate plots,
interesting results, bits of information, so basically the research process
itself, not the final publication ready information.

```
liver-cancer-analysis.Rmd
splicing-diversity-tests.Rmd
2021-W01.Rmd
2021-01-01.Rmd
2021-W01-aml-data-cleanup.Rmd
```

[R markdown](https://rmarkdown.rstudio.com/) files are an excellent way to keep
track of ideas, plots, results. Simple
[markdown](https://daringfireball.net/projects/markdown/syntax) files are good
for simple documentation without code.

## Daily summary

Keep the main `README.md` here to include a daily short summary with bullet
points, keywords. As it might get very long, start a new document annually or
monthly. `README.md` without dates is always the current one.

```
README.md
README-2020.md
README-2021.md
```

or

```
README.md
README-2021-10.md
README-2021-11.md
README-2021-12.md
```

### 2021-01-01

- Started project, collected first dataset from XXX
- Installed tool YYY and ZZZ
