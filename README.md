
# Hugo Theme Base

This repo is a starting point for building a Hugo theme.

There is content in the following directories:
- content (demo content for the structure)
- layouts (layout files showing structure)

The other directories are empty, since they are not necessary for the 
base of a simple hugo template.

## Necessary files for pulled repositories

For repos to be pulled and integrated into the Hugo build process, there need to 
be a few things in the repository and in the individual files:

- All Repositories need to have a file named `_index.md` in the root of each directory with 
markdown files (typically README.md) so that Hugo can "understand" that the files are part of 
the documentation.  The file only needs to have the following frontmatter content:
```code
---
title: "what will appear in the menu"
--- 
```
- If there are multiple directory levels in the repository, each level with markdown files to 
be included in the documentation needs the above file included.

Example:
```code
# Repository

my-project
  |_index.md (title: My Project)
  |  
  |-- sub-project-one
  |   |-- _index.md (title: Sub Project One)
  |
  |-- sub-project-two
      |-- _index.md (title: Sub Project Two)

```
- All markdown files are required to have a frontmatter header for them to be processed correctly.  The
frontmatter should be in the following format with this minimum of data:

```code
---
title: "what will appear in the menu"
date:  2024-10-05
---
```

- Additional frontmatter can be included in the files as well

