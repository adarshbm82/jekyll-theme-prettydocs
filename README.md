# Jekyll Theme PrettyDocs

Inspired on https://themes.3rdwavemedia.com/demo/prettydocs/

## Installation

Add this line to your Jekyll site's Gemfile:

```ruby
gem "jekyll-theme-prettydocs"
```
And then run:

```shell
$ sudo bundle update
```

Or install it yourself, run:

```shell
$ gem install jekyll-theme-prettydocs
```

After yor install theme, you should replace `minima` theme for new `jekyll-theme-prettydocs` theme.
To do it, change in `_config.yml` file, like this:

```yaml
#replace
theme: minima
#by
theme: jekyll-theme-prettydocs
```

To start jekyll server, run:

```
$ jekyll s
```

Open in your browser `http://localhost:4000`. See the site, with this wonderful theme.

![](./screenshot.png)

**After you install and start, you can to do your changes.**

## Customize theme

### Home Page

The first thing that you will want to change is home page links list. So, what you need is simple. Just create your pages, with these attributes:

```yaml
cards-section: blue
title: Title of page
intro: Intro of page
icon: icon_gift
```

So, with these small attributes into your pages, you can create a list of links in home page. Below, some description about each attribute.

#### cards-section

Cards section is usually the color of card. The colors availables is: blue, pink, purple, orange, green, and primary.

#### title

The title is title of card. It's the strong text on card.

#### intro

The intro is a introdution of card. It's a description about card.

#### icon

The icon is icon of card. 600+ FontAwesome icons.

### Header

Default header.

{% include header.html %}

Custom header, with no breadcrumb.

{% include breadcrumb="" %}

Below, some description about all attributes.

#### icon

The icon is icon of page. 600+ FontAwesome icons.

#### title

The title is title of page. It's the same color of page.

#### bold

The bold is white title of page.

#### breadcrumb

The breadcrumb usually show or hide the section of breadcrumb. Default value is 'true', but if you set '' or 'false' you don't show breadcrumb more.

#### breadcrumb-home-link

The link to home link.

#### breadcrumb-home-title

The title of Home page link.

#### breadcrumb-active

The breadcrumb-active usually show or hide the second part of breadcrumb.

Example with others attributes.

{% include header.html
    icon="fa fa-hashtag"
    title="Title"
    bold="White"
    breadcrumb=""
%}

### Promo Block

Default.

{% include promo-block.html %}

Custom promo block.

{% include
    title="My Project"
    figure="/assets/images/demo/appkit-account-drive-thumb.jpg"
    figure-link="http://maiconpinto.com.br"
%}

Below, some description about all attributes.

#### icon

The icon is icon of promo block. 600+ FontAwesome icons.

#### title

The title is title of promo block.

#### title-link

The title-link is the URL of title of promo block.

#### figure

The figure is the URL of image of promo block.

#### figure-link

The figure-link is the link image of promo block.

#### figure-title

The figure-title is the title of alt attribute of image.

#### content

The content is description of promo block.

#### content-title

The content-title is the title of content. It's the strong text.

#### author

The author is author name.

#### author-link

The author-link is URL to author.

### Content of Page

I'd like to do it the easy way, but for now I've only found this way.
You need to have the Emmet plugin installed in your editor.
Once installed, you will copy the below line, and paste into body of your page.

```html
div.doc-wrapper>div.container>((div#doc-header.doc-header.text-center>(h1.doc-title>i.icon.fa.fa-paper-plane{Quick Start})+(div.meta>i.fa.fa-clock-o{Last Update on}))+(div.doc-body>((div.doc-content>div.content-inner>section.doc-section#download-section>(h2.section-title{Download})+(div.section-block))+(div.doc-sidebar.hidden-xs>nav#doc-menu>li>a.scrollto[href=#download-section]{Download}))))
```

## A complete example of page

```html
---
layout: green
title: Page example
permalink: /example-page/
cards-section: green
title: Title of page
intro: Intro of page
icon: icon_gift
---

{% include header.html
    icon="fa fa-hashtag"
    title="Quick Start"
    bold="Page"
%}

div.doc-wrapper>div.container>((div#doc-header.doc-header.text-center>(h1.doc-title>i.icon.fa.fa-paper-plane{Quick Start})+(div.meta>i.fa.fa-clock-o{Last Update on}))+(div.doc-body>((div.doc-content>div.content-inner>section.doc-section#download-section>(h2.section-title{Download})+(div.section-block{div.doc-wrapper>div.container>((div#doc-header.doc-header.text-center>(h1.doc-title>i.icon.fa.fa-paper-plane{Quick Start})+(div.meta>i.fa.fa-clock-o{Last Update on}))+(div.doc-body>((div.doc-content>div.content-inner>section.doc-section#download-section>(h2.section-title{Download})+(div.section-block))+(div.doc-sidebar.hidden-xs>nav#doc-menu>li>a.scrollto[href=#download-section]{Download}))))}))+(div.doc-sidebar.hidden-xs>nav#doc-menu>li>a.scrollto[href=#download-section]{Download}))))

{% include promo-block.html
    title="My Project"
    figure="/assets/images/demo/appkit-account-drive-thumb.jpg"
    figure-link="http://maiconpinto.com.br"
    author="Maicon Pinto"
    author-link="http://maiconpinto.com.br"
%}
```

![](./assets/images/demo/a-complete-example-of-page.png)


## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/maiconpinto/jekyll-theme-prettydocs. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `bundle install`.

You theme is setup just like a normal Jelyll site! To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, and `_sass` tracked with Git will be released.

## License

The theme is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

