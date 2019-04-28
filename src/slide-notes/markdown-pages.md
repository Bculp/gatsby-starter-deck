Using Markdown
- Required plugins
  - gatsby-source-filesystem
    - allows Gatsby to read local files
    - requires path to these files
  - gatsby-transformer-remark
    - transforms markdown
    - transforms to "frontmatter", passed to React component as data
    - you can add other keys
```
---
path: "/blog/my-first-post"
date: "2017-11-07"
title: "My first blog post"
---
```
- transforms markdown content to HTML
- Create template to pull in "frontmatter" (requires some destructuring shown in plugin info)
- Markdown content is HTML, which we pass to `dangerouslySetInnerHTML` - "React’s replacement for using innerHTML in the browser DOM"
- Inside gatsby-node.js:
  - we call createPages API to programically create a new page for each of the markdown files we have using the template component we specify