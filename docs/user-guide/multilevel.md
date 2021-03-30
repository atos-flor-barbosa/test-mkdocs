## Multilevel structure
Currently, MkDocs allows you to have up to a second level of navigation. 


### Configure Pages and Navigation

The nav configuration setting in your `mkdocs.yml` file
defines which pages are included in the global site navigation menu as well as
the structure of that menu. If not provided, the navigation will be
automatically created by discovering all the Markdown files in the
documentation directory. An automatically created
navigation configuration will always be sorted alphanumerically by file name
(except that index files will always be listed first within a sub-section). You
will need to manually define your navigation configuration if you would like
your navigation menu sorted differently.

A minimal navigation configuration could look like this:

```no-highlight
nav:
    - 'index.md'
    - 'about.md'
```

All paths in the navigation configuration must be relative to the `docs_dir`
configuration option. If that option is set to the default value, `docs`, the
source files for the above configuration would be located at `docs/index.md` and
`docs/about.md`.

The above example will result in two navigation items being created at the top
level and with their titles inferred from the contents of the Markdown file or,
if no title is defined within the file, of the file name. To override the title
in the `nav` setting add a title right before the filename.

```no-highlight
nav:
    - Home: 'index.md'
    - About: 'about.md'
```

Note that if a title is defined for a page in the navigation, that title will be
used throughout the site for that page and will override any title defined
within the page itself.

Navigation sub-sections can be created by listing related pages together under a
section title. For example:

```no-highlight
nav:
    - Home: 'index.md'
    - 'User Guide':
        - 'Writing your docs': 'writing-your-docs.md'
        - 'Styling your docs': 'styling-your-docs.md'
    - About:
        - 'License': 'license.md'
        - 'Release Notes': 'release-notes.md'
```

References: https://github.com/mkdocs/mkdocs/blob/master/docs/user-guide/writing-your-docs.md