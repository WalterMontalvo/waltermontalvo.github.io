# Jekyll Only

A starter kit for using [Jekyll](https://jekyllrb.com/) that includes:
* A barebones Jekyll starter theme

## What is Jekyll?
>"Jekyll is a simple, blog-aware, static site generator perfect for personal, project, or organization sites. Think of it like a file-based CMS, without all the complexity. Jekyll takes your content, renders Markdown and Liquid templates, and spits out a complete, static website ready to be served by Apache, Nginx or another web server. Jekyll is the engine behind GitHub Pages, which you can use to host sites right from your GitHub repositories."
–[Jekyll](https://jekyllrb.com/)

## Requirements
* [Bundler](http://bundler.io/)
* [Jekyll](https://jekyllrb.com/)
* [Node.js](https://nodejs.org/en/)
* [npm](https://www.npmjs.com/)
* [Ruby](https://www.ruby-lang.org/en/)

## Get started

To create a new Jekyll site, use the ```jekyll new``` command:
```
$ jekyll new --skip-bundle .
# Creates a Jekyll site in the current directory
```

Open the Gemfile that Jekyll created.

Add "#" to the beginning of the line that starts with ```gem "jekyll"``` to comment out this line.

Add the ```github-pages``` gem by editing the line starting with ```# gem "github-pages"```. Change this line to:
```gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins```

Replace GITHUB-PAGES-VERSION with the latest supported version of the ```github-pages``` gem. You can find this version here: "Dependency versions." (https://pages.github.com/versions/)

The correct version Jekyll will be installed as a dependency of the ```github-pages``` gem.

Add the ```webrick``` gem to the Gemfile

```gem "webrick"```

Save and close the Gemfile.

From the command line, run ```bundle install```.

Optionally, make any necessary edits to the ```_config.yml``` file. This is required for relative paths when the repository is hosted in a subdirectory. For more information, see "Splitting a subfolder out into a new repository."

```domain: my-site.github.io       # if you want to force HTTPS, specify the domain without the http at the start, e.g. example.com
url: https://my-site.github.io  # the base hostname and protocol for your site, e.g. http://example.com
baseurl: /REPOSITORY-NAME/      # place folder name if the site is served in a subfolder
```

Run your Jekyll site locally.

```$ bundle exec jekyll serve```
