# NeurotechEDU
### [www.learn.neurotechedu.com](http://learn.neurotechedu.com/)

NeurotechEDU is an open-source project designed to promote collaboration and user-generated content towards emerging Neurotechnology practices.
The idea is that if you are not finding something that should be part of our resources or lessons you can go ahead make it, and upload it to our page.

The project is built with the help of:

 * [Foundation](http://foundation.zurb.com/)
 * [Jekyll](http://jekyllrb.com/)
 * [Feeling Responsive Jekyll theme](https://phlow.github.io/feeling-responsive/) by Phlow

Github is necessary if you wish to contribute to NeurotechEDU. [You can learn about Github here.](https://guides.github.com/activities/hello-world/)

<br>

## Contributing

We have set up the contribution process to be as simple as possible so that people who don’t have much experience programming are still able to contribute. 

+ There are two ways to do so:
  - [By editing a new page directly on Github](#editing-directly-on-github).
  - [By cloning this repository, installing jekyll and making the page locally (this option allows for previews)](#contributing-with-local-jekyll-build).

With either option, in order to publish you push a commit to us and once approved your content becomes part of the website.

The first option allows you to only use markdown, a very simple syntax designed to accomodate prose in web documents. It does require precise spacing. Elements such as lists might need a blank line before and after the element in order to work properly. You can read more about it [here](https://guides.github.com/features/mastering-markdown/).

The second option gives more freedom with HTML, Markdown and a local Jekyll build. You are able to have more flexibility with design and render a preview of the page as you go.  
  
#### *Please remember that all contributions need to be done as a new page*.  
<br>


## Editing directly on Github

Head to: 
```
/pages
```

1. Create a new file via "Create new file" button" name the file to your liking, but make sure it ends in `.md` [markdown format] and that *no other file in the folder has the name you wish to use*.
2. Change the file’s title, teaser and permalink. Make sure to keep the same formatting.
3. The page starts below the masthead markdown code, we have included examples of the code there. You can see what it looks like once rendered by jekyll by going to http://learn.neurotechedu.com/template/ and comparing it with `template.md` in the repository. 
4. DO NOT modify any HTML, simply add your markdown code inside 
5. If you want to include images, add them to 'http://learn.neurotechedu.com/images/'
6. Once done, push a commit that will be reviewed by one of our webmasters. Keep in mind that we are a non-profit and depend on the generosity of people in order to keep a high quality standard.
<br>
<br>


## Contributing with local Jekyll build

This option gives you more flexibility and input in the contribution process, but requires a bit of programming knowledge or the willingness to learn :) You'll have to install Jekyll and get a local build going. It's not very hard, but it does require some navigation with terminal.



### Jekyll Setup for Mac OS and Linux

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


### Jekyll on Windows

Installing Jekyll on Windows is somewhat different. [You can learn about it here.](https://jekyllrb.com/docs/windows/)

<br>

### Once Jekyll is working:

Head to: 
```
/pages
    /template.md
```

1. Make a copy of `template.md` AND rename it to your liking OR make a new `.md` file . The new file has to go in the `/pages` folder
2. Change the file’s title, teaser and permalink. Make sure to keep the same formatting.
3. The page starts below the masthead markdown code, we have included examples of the code there. You can see what it looks like once rendered by jekyll by going to http://learn.neurotechedu.com/template/
4. Add your markdown code inside the given HTML tags. If you want to change some HTML, that's fine with us but please don't add any styles to the .scss files. The HTML conventions come from our theme's use of the Foundation framework.
5. If you want to include images, add them to 'http://learn.neurotechedu.com/images/'
6. With local builds you can do `jekyll serve` in order to create a temporary server in your machine and see how the website comes together once built. We suggest you do this as much as possible before commiting any changes. Jekyll's potential really comes through once you have constant feedback capabilities.
7. If the previous command does not work correctly, try this one: `bundle exec jekyll serve --host $(hostname -I) 2> /dev/null` This will silence any Warnings and allow you to properly see the output from the jekyll server.
8. Once done, push a commit that will be reviewed by one of our webmasters. 

<br>

## Notes

1. Please don't add any styling to the scss files. If you want to stylize your page more, inline `<span>` or `style=""` tags are fine.
2. The theme we use implements the Foundation framework, that's where the naming conventions for our classes and ID's come from. Their documentation is available [here](http://foundation.zurb.com/sites/docs/v/5.5.3/components/grid.html).
3. If you are on Chrome and want to build the content first on Google Docs, you can use this [this plugin](https://chrome.google.com/webstore/detail/docs-to-markdown/igffnbdfnodiaphfmfaiiaegmoljbghf) to conver to markdown



## Feedback?

Get in touch with us [here](https://docs.google.com/forms/d/e/1FAIpQLScUB1BwxUr6pKxe8yTS4JqU7veFXyYgFOETUDRluG5pK7E7tg/viewform?c=0&w=1)

This Project is participating in the Mozilla Community Sprint. Check out their guidelines [here](https://www.mozilla.org/en-US/about/governance/policies/participation/)


