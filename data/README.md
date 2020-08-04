# Data directory structure

Explain briefly the structure of the directory. What do the different
directories contain.

## Excluded and personal data

Exclude directories using `.gitignore` as needed and keep in mind that no
identifiable patient data should be included here. These include, but are not
limited to:

- given name, family name, nickname
- birthdate and location
- personal address
- any type of healthcare or insurance identifier
- detailed diagnostic information
- job and job address
- online profile information

## Directory structure details

```
original/
```

This directory should be always present, and contain the original unmodified
data, coming from collaborators, experiments, the sequecing machine, etc.

## Shared data

If you are working with data that is shared among users and not present in the
`data/` directory, add a short description with the exact location, like:

Data available at server 1.2.3.4

```
/path/to/data
```

Additionally, provide a `README-shared.md` describing any data processing steps on the
shared data, with command lines, tools, tool parameters, and tool version. Use a
symlink to link your README from the repo to the shared data location.

```
ln -s /my/repo/data/README-shared.md /shared/data/README.md
```
