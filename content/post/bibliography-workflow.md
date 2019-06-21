---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Bibliography Workflow (precursor)"
subtitle: "Zotero to: LaTeX+moderncv and hugo+academic"
summary: ""
authors: []
tags: []
categories: []
date: 2019-06-21T20:34:05+02:00
lastmod: 2019-06-21T20:34:05+02:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

I recently switched from [Mendeley](https://www.mendeley.com) to [Zotero](https://www.zotero.org) - or rather from [Mendeley Desktop](https://www.mendeley.com/download-desktop/) to the [Zotero Desktop App](https://www.zotero.org/download/). 
This had multiple reasons: 

1. It had started a (long) while ago when I couldn't make papers accessible on the web in a way (anymore) so that users wouldn't have to login first
2. The file upload/syncing to the web (for the users with login...) was very fluky, and the bug tracker for this issue has very long history. 
3. Eventually, in the course of the implementation of the GDPR mendeley started to [encrypt our data](https://eighty-twenty.org/2018/06/13/mendeley-encrypted-db) - which seemed wrong on many levels but most notably on the one that connected this to the GDPR.

So, with Zotero my workflow to (semi-automatically) update my [CV](https://github.com/iiegn/pub/tree/master/CV) needed to be adapted... and so did the workflow to update my [website](https:/iiegn.eu).
This [old website](https://github.com/iiegn/iiegn.eu-jekyll-site) was made with [Jekyll](https://jekyllrb.com/) and I was quite happy with it.
Well, yes, still, for reasons-for-another-post I decided to give [Hugo](https://gohugo.io/) a try.

The new mix now looks like this:

- Zotero + [Better BibTeX for Zotero](https://retorque.re/zotero-better-bibtex/) automatically feeding biblatex files into
  - [(lua)LaTeX + biblatex](https://github.com/iiegn/pub/tree/master/CV) + [moderncv](https://ctan.org/pkg/moderncv)
  - [hugo + academic](http://github.com/iiegn/iiegn.eu-academic-kickstart-site/) + [academic-admin](https://github.com/iiegn/academic-admin)

I found these links very helpful...:

- [Customising exports from Zotero+BetterBibTeX](https://retorque.re/zotero-better-bibtex/customized-exports/)
- [Citeable Item Types not Included in Zotero](https://www.zotero.org/support/kb/item_types_and_fields#citeable_item_types_not_included_in_zotero)
- http://docs.citationstyles.org/en/1.0.1/specification.html#appendix-iii-types
- https://nwalsh.com/tex/texhelp/bibtx-7.html
- https://en.wikibooks.org/wiki/LaTeX/Bibliography_Management
