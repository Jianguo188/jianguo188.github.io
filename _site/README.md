# Run the site locally

This site uses Jekyll and the GitHub Pages gem. Preview it locally before pushing changes.

## Requirements

- Ruby 3.2 through 3.x (Ruby 4 is not supported by the GitHub Pages dependencies)
- Bundler

On macOS with Homebrew, install a compatible Ruby 3 release. Avoid the unversioned `ruby` formula if it installs Ruby 4:

```sh
brew install ruby@3.3
export PATH="$(brew --prefix ruby@3.3)/bin:$PATH"
```

Add the `PATH` line to your shell profile if you want Ruby 3.3 to remain the default in new terminals.

Check the active versions:

```sh
ruby --version
bundle --version
```

If `bundle` is not available, install Bundler with `gem install bundler`.

## Install and preview

From the repository root, install the site's dependencies and start Jekyll:

```sh
bundle install
bundle exec jekyll serve
```

Open <http://127.0.0.1:4000/> in your browser. Jekyll rebuilds the site when files change; refresh the browser to see the latest version. Stop the server with `Ctrl+C`.

## Add a guide

Put an `.html` guide in a folder under `guides/` and give it Jekyll front matter at the very top:

```yaml
---
title: "Guide title"
description: "A short summary of the guide."
---
```

The homepage discovers guides from their folders, so adding a guide does not require editing the homepage. The local preview uses the same Jekyll configuration as the published site.
