# codeX docs Jekyll Skellington :skull:

A barebones skeleton for applying to codeX documentation (such as the narrative, code katas, and concept cards) to publish it as a Jekyll and GitHub Pages-powered web site.

This lets us write the docs in Markdown, and use [fancy syntax highlighting](http://jekyllrb.com/docs/templates/#code-snippet-highlighting).

## Things to update

### Title and base url

In the `config.yml` file, you need to update:

* the `title`. This should be the name of the module.
* the `baseurl`. This should match the name of the repository (to avoid path funkiness when you publish to GitHub Pages). E.g. `\kata`

### Navigation

In `_includes/footer.html`, add links to any other pages inside the ordered list.


### Layout in the YAML front-matter

There are two layouts:

* `default` for most things
* `single` for single-page doc items that don't need a navigation block.
