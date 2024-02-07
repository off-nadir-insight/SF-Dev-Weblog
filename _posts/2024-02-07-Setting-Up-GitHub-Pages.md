---
layout: post
title: "Setting up GitHub Pages"
date: 2024-02-07
categories: github documentation
---

# GitHub Pages Setup

Description: My single page referenceable quick notes consolidated from working through the GitHub skills exercise for GitHub Pages found at https://github.com/skills/github-pages. Great exercise to work through!! :star2:

## Steps

### Set up repository

1. create a new repository
1. enable GitHub Pages in the repository
    1. Under the repository name, navigate to `Settings` -> section named `Code and Automation` -> `Pages`
    1. Ensure the `Source` drop-down has `Deploy from a branch` selected
    1. Select `Main` from the `Branch` drop-down menu
    1. Save!
        > To locate the URL for a repository, the **Pages** setting should provide a link at the top, alongside a 'Visit Site' button

### Configure site

-   Configuration is handled in the `_config.yml` file for site settings, theme, site title, etc
    -   ([Jekyll Docs](https://jekyllrb.com/docs/configuration/) on customizing deployment)
    -   Simple Example
        ```yaml
        theme: minima
        title: Site Title
        author: FirstName LastName
        description: Weblog of FirstName LastName
        ```
    -
-   The 'Home' page is handled by either an `index.md` file or the `README.md`.
    -   Pages first searches for the `index.md` by default

### Creating a new post

#### Details

-   use specific file name syntax and [Front Matter](https://jekyllrb.com/docs/front-matter/) to automate page creation
    -   template for file names: `_posts/YYY-MM-DD-page-title.md`
        -   located in the `_posts` folder
        -   hyphenate required date and between title words
        -   markdown file type

##### Front Matter

-   Front matter is the YAML syntax Jekyll files use. Goes at the top of the file and looks like:

```yaml
---
layout: post
title: "Welcome to my blog"
date: 2019-01-20
categories: CATEGORY-1 CATEGORY-2
---
```

#### Actions
1. New branch
1. Create a new file
   1. `_posts/YYYY-MM-DD-page-title.md`
1. Add the front matter
    ---
    ```yaml
    layout: post
    title: "Post Title"
    date: 2024-01-20
    categories: CATEGORY-1 CATEGORY-2
    ---
    ```
1. Quick commit the first draft
1. Add and edit content!
1. Commit further changes
1. When ready to publish, create a pull request
1. Review changes and after the merge, GitHub Actions kick off steps to publish the new page!

## Further References

-   [GitHub Pages Docs](https://docs.github.com/en/pages)
-   [Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github)
-   [Github markdown emoji](https://gist.github.com/rxaviers/7360908)
