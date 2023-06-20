# Web Development Fundamentals

The files for Kibo's Web Development Fundamentals course. 

_Note: This course was previously called Web Foundations, and was only 5 weeks. It uses the same repository, but has a different deployed url: https://web-foundations.vercel.app/_

## What's here?

```
$ tree .
.
├── README.md
├── book.toml
└── src
    ├── SUMMARY.md
    └── lessons
        └── chapter_n.md
```

### README.md

You're lookin at it.

### book.toml

Config file for the course. Authors, title, other mdbook settings.

https://rust-lang.github.io/mdBook/format/configuration/index.html

### src

Holds all the course files 

### output

The static site is built here, but it gets ignored by git.

To generate the static site, run:

```
mdbook build
```

You can usually ignore the files in `output`, git will.


### src/SUMMARY.md

This gets turned into the sidebar on the site. 

It's the text that should show, plus links to other md files in `src/`.

https://rust-lang.github.io/mdBook/format/summary.html

Pages that aren't linked in the summary don't get built.

### src/*

These are the pages that actually make up the course. It's nice to put
things in folders to organize the different pages.

## Getting Started

Install mdbook: https://rust-lang.github.io/mdBook/guide/installation.html

if you use rust:

```
cargo install mdbook
```

Or use your package manager (e.g. `brew install mdbook`), or download a release from
Github.

## Run the book locally

```
mdbook serve --open
```

## Deployment

We use `vercel` to handle deploys. It takes some setup to connect a repo to
vercel, assign a production domain, and set up auto-deploys.

If all that's been done...

* Github actions will run `mdbook build` on pushed changes
* All pushes will automatically deploy to vercel
* Vercel will notify the #tech-status channel on Slack with the deploy preview
* If you pushed to `main`, it will also deploy to the live site. Watch out!

## Previews and Drafts

If you'd like to preview changes, push to a branch. Check the #tech-status channel in Slack for a link to the
preview when you make a change.

Remember - commits to main get built and deployed to the production site; others
just get previews.
