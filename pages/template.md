---
layout: page-fullwidth
show_meta: false
title: "Template"
subheadline: ""
teaser: "Add a short introduction/teaser about your content here. A short paragraph will do. Perhaps be specific about what you cover so that people reading have a clear idea of what they will find. "
header:
   image_fullwidth: ""
permalink: "/template/"
---
<div class="row">
<div class="medium-4 medium-push-8 columns" markdown="1">
<div class="panel radius" markdown="1">
**Table of Contents**
{: #toc }
*  TOC
{:toc}
</div>
</div><!-- /.medium-4.columns -->


<div class="medium-8 medium-pull-4 columns" markdown="1">

# h1 Heading :)
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading


## Horizontal Rules

---


## Emphasis

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~~Strikethrough~~


## Blockquotes


> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.


## Tables

| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

Right aligned columns

| Option | Description |
| ------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |


## Links

[link text](http://dev.nodeca.com)

[link with title](http://nodeca.github.io/pica/demo/ "title text!")

Autoconverted link https://github.com/nodeca/pica (enable linkify to see)


## Images

![Minion](https://octodex.github.com/images/minion.png)
![Stormtroopocat](https://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")

Like links, Images also have a footnote style syntax

![Alt text][id]

With a reference later in the document defining the URL location:

[id]: https://octodex.github.com/images/dojocat.jpg  "The Dojocat"


## Giphy

For Giphy embeds go to the Giphy page, choose embed and click responsive. Once you have the code, delete the `<p>...</p>` code at then end and keep the `<div>...</div>`

<div style="width:100%;height:0;padding-bottom:56%;position:relative;"><iframe src="https://giphy.com/embed/4MxMvzhTEuqty" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div>

## Video

A responsive YouTube element with a 16x9 aspect ratio (default)

{% include youtube_embed.html id="dAIQeTeMJ-I" %}
<!-- Replace id with your video id -->

Add in aspect ratio for 4x3 (only this and 16x9 are supported)

{% include youtube_embed.html id="dAIQeTeMJ-I" aspect="4x3"%}

iFrame code for YouTube is set in `/_include/youtube_embed.html`


</div>
</div> <!-- end of row -->
