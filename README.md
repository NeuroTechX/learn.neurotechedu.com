# [www.learn.neurotechedu.com](http://learn.neurotechedu.com/)

The is the code to our education open-source website.
This project is built with the help of:

 * [Foundation](http://foundation.zurb.com/)
 * [Jekyll](http://jekyllrb.com/)
 * [Feeling Responsive Jekyll theme](https://phlow.github.io/feeling-responsive/) by Phlow

Github is necessary if you wish to contribute to NeurotechEDU. [You can learn about Github here.](https://guides.github.com/activities/hello-world/)

A combination of HTML and Markdown are used, but for the purpose of contributing you only need to know the [Markdown format which you can learn about here.](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) Unlike HTML, Markdown is _very_ sensitive about spacing. Elements such as lists might need a blank line before and after the element in order to work properly.

## Jekyll Setup for Mac OS and Linux

The website uses [Jekyll](http://jekyllrb.com/), a static website generator written in Ruby.
You need to have Version 2.0.0 or higher of Ruby and the package manager Bundler.
(The package manager is used to make sure you use exactly the same versions of software as GitHub Pages.)
After checking out the repository, please run:

```
$ bundle install
```

to install Jekyll and the software it depends on.
You may consult [Using Jekyll with Pages](https://help.github.com/articles/using-jekyll-with-pages/) for further instructions.

You will also need [Python 3](http://python.org/) with
[PyYAML](https://pypi.python.org/pypi/PyYAML/) available in order to
re-generate the [data files](#details) the site depends on.

## Jekyll on Windows

Installing Jekyll on Windows is considerably different from a Mac. [You can learn about it here.](https://jekyllrb.com/docs/windows/)

## Fundamental changes to default template

The Neurotech EDU logo HTML/CSS was changed for the header type "image_fullwidth". The affected files are "masthead.html", "navigation.html" and "layout.scss". The logo used to be positioned on top of the header image.

If you simply want to change the logo image, that is done from config.yml
