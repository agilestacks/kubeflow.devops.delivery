# This project is build for [kubeflow.devops.delivery](https://kubeflow.devops.delivery) website

[![GitHub Pages](https://github.com/agilestacks/kubeflow.devops.delivery/actions/workflows/gh-pages.yml/badge.svg)](https://github.com/agilestacks/kubeflow.devops.delivery/actions/workflows/gh-pages.yml) [![pages-build-deployment](https://github.com/agilestacks/kubeflow.devops.delivery/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/agilestacks/kubeflow.devops.delivery/actions/workflows/pages/pages-build-deployment)

This website is based on [hugo](https://gohugo.io/) framework for building websites. Also using next assets:

- [hugo-book] as theme.

## Prepare

One of way how to install `hugo` is just run command:

```shell
brew install hugo
```

For more details visit official hugo [site](https://gohugo.io/getting-started/installing/)

To get [hugo-book] theme just run

```shell
git submodule update --init
```

## Local development

To run site locally just call command:

```shell
hugo server --minify --theme hugo-book
```

## Build and publish to github pages

This is done via GitHub Actions.

[hugo-book]: https://github.com/alex-shpak/hugo-book
