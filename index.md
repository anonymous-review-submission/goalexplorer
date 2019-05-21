---
layout: default
title: Home
nav_order: 1
description: "GoalExplorer is a tool that performs goal-driven exploration to trigger functionality of interest for Android apps."
permalink: /
---

# <span style="font-variant:small-caps;">GoalExplorer</span>
{: .fs-9 }

Goal-driven Exploration for Android Apps.
{: .fs-6 .fw-300 }

[Overview](docs/overview.md){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [Download](https://github.com/pmarsceill/just-the-docs){: .btn .fs-5 .mb-4 .mb-md-0 }

---

<span style="font-variant:small-caps;">GoalExplorer</span> automatically generates an executable test script that directly triggers the functionality of interest. The core idea behind <span style="font-variant:small-caps;">GoalExplorer</span> is to first statically model the application UI screens and transitions between these screens, producing a Screen Transition Graph (STG). Then, <span style="font-variant:small-caps;">GoalExplorer</span> uses the STG to guide the dynamic exploration of the application to the particular target of interest: an Android activity, API call, or a program statement. The results of our empirical evaluation on 93 benchmark applications and 95 the most popular GooglePlay applications show that the STG is substantially more accurate than other Android UI models and that <span style="font-variant:small-caps;">GoalExplorer</span> is able to trigger a target functionality much faster than existing application exploration.

This repo contains the API calls, collected from [Android Developers](https://developer.android.com/), that are used to identify fragments transaction, menu/drawer/dialog creation, and inter-component transitions.
The repo also contains the details of our empirical evaluation on 93 benchmark applications and 95 the most popular GooglePlay applications, with app version, category, and size.

### Configure <span style="font-variant:small-caps;">GoalExplorer</span>

- [See instructions]({{ site.baseurl }}{% link docs/instruction.md %})

### Dependencies

Just the Docs is built for [Jekyll](https://jekyllrb.com), a static site generator. View the [quick start guide](https://jekyllrb.com/docs/) for more information. Just the Docs requires no special Jekyll plugins and can run on GitHub Pages' standard Jekyll compiler.

### Quick start: Use as a GitHub Pages remote theme

1. Add Just the Docs to your Jekyll site's `_config.yml` as a [remote theme](https://blog.github.com/2017-11-29-use-any-theme-with-github-pages/)
```yaml
remote_theme: pmarsceill/just-the-docs
```
<small>You must have GitHub Pages enabled on your repo, one or more Markdown files, and a `_config.yml` file. [See an example repository](https://github.com/pmarsceill/jtd-remote)</small>

### Local installation: Use the gem-based theme

1. Install the Ruby Gem
```bash
$ gem install just-the-docs
```
```yaml
# .. or add it to your your Jekyll site’s Gemfile
gem "just-the-docs"
```
2. Add Just the Docs to your Jekyll site’s `_config.yml`
```yaml
theme: "just-the-docs"
```
3. _Optional:_ Initialize search data (creates `search-data.json`)
```bash
$ bundle exec just-the-docs rake search:init
```
3. Run you local Jekyll server
```bash
$ jekyll serve
```
```bash
# .. or if you're using a Gemfile (bundler)
$ bundle exec jekyll serve
```
4. Point your web browser to [http://localhost:4000](http://localhost:4000)

If you're hosting your site on GitHub Pages, [set up GitHub Pages and Jekyll locally](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll) so that you can more easily work in your development environment.

---

## About the project

Just the Docs is &copy; 2017-2019 by [Patrick Marsceill](http://patrickmarsceill.com).

### License

Just the Docs is distributed by an [MIT license](https://github.com/pmarsceill/just-the-docs/tree/master/LICENSE.txt).

### Contributing

When contributing to this repository, please first discuss the change you wish to make via issue,
email, or any other method with the owners of this repository before making a change. Read more about becoming a contributor in [our GitHub repo](https://github.com/pmarsceill/just-the-docs#contributing).

### Code of Conduct

Just the Docs is committed to fostering a welcoming community.

[View our Code of Conduct](https://github.com/pmarsceill/just-the-docs/tree/master/CODE_OF_CONDUCT.md) on our GitHub repository.
