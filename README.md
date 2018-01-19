---
title: Contribute
disableToc: true
---

# About

This is the Documentations for 96rocks. You can view the documents at the [docs.96rocks.com](http://docs.96rocks.com/). This documents is hosted on [Github Page](https://pages.github.com/) with custom domain at [gh-pages branch](https://github.com/96rocks/docs.96rocks.com/tree/gh-pages). The master branch is the souce for the documents.

# How to contribute

## Install hugo

The documents is generated by [Hugo](https://gohugo.io), a static site generator.

For deb package management based Linux

    sudo apt-get install hugo

For MacOS

    brew install hugo

Other platform please refer [Hugo install documents](https://gohugo.io/getting-started/installing).

## Local preview
Fork the repo and clone it

    git clone https://github.com/96rocks/docs.96rocks.com.git
    cd docs.96rocks.com
    hugo server

The output is like below:

    ...
    Serving pages from memory
    Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
    Press Ctrl+C to stop

Open your browser, go to http://localhost:1313/ and you can view the docs locally.

## Edit/Add documents

The documents are under **content** directory, starting with **_index.en.md**(with multiple language support). You can copy and paste the exsiting files to start new sections. Put all the images in one image directory. Hugo can auto refresh if there is any file changes. Commit and push the change to your repo if the preview is ok and send pull request from the master branch. We will merge it and update the gh-pages branch. Updating gh-pages branch is live instantly. Your contribution will be automatically added to the [credit](https://docs.96rocks.com/credits/) section once merged.
