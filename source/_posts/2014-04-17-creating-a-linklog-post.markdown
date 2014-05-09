---
layout: post
title: "Creating a Linklog Post"
date: 2014-04-17 06:46:36 -0700
comments: true
categories: [octopress]
---
[1]: http://daringfireball.net
[2]: http://octopress.org/docs/blogging/linklog/

One of the things I do on this blog is reference
outside material with the &rArr; symbol in the title
of a post, which is also called a linklog. This was
popularized by John Gruber's [daringfireball][1] blog,
where &#9733; references an external link.

If you were curious prior to this post and tried to
follow [Octopress's Linklog Tutorial][2], only to
miserably find out it doesn't work and then end up
berating yourself because you are sure you did
something wrong but don't know what, apologize to
yourself right now since that tutorial does not apply
to the master branch octopress as of today, April 17,
2014. (A prime example of the Wild Wild West of Github.)

##Configuring for Linklog Support
### Add linklog support to the article html template
- Open the file `.../source/_includes/article.html`
- Under  `<header>` tag, replace the first if else block with:
``` html
{% raw %}
<header>
  {% if index %}
    {% if post.external-url %}<!-- This defines how Octopress will use posts with external-url. -->
      <h1 class="entry-title external"><a href="{{ post.external-url }}">{% if site.titlecase %}{{ post.title | titlecase }} <span>&rArr;</span>{% else %}{{ post.title }}{% endif %}</a></h1>
      {% else %}<!-- Now we're back to normal posts. Note the links used under href in both headers.-->
      <h1 class="entry-title"><a href="{{ root_url }}{{ post.url }}">{% if site.titlecase %}{{ post.title | titlecase }}{% else %}{{ post.title }}{% endif %}</a></h1>
    {% endif %}
  {% else %}
    {% if page.external-url %}
      <h1 class="entry-title external"><a href="{{ page.external-url }}">{% if site.titlecase %}{{ page.title | titlecase }} <span>&rArr;</span>{% else %}{{ page.title }}{% endif %}</a></h1>
    {% else %}
      <h1 class="entry-title">{% if site.titlecase %}{{ page.title | titlecase }}{% else %}{{ page.title }}{% endif %}</h1>
    {% endif %}
  {% endif %}
{% endraw %}
```
If you don't want to use my &rArr; symbol, search for
`&rArr;` and replace it with your own.

Your blog now has linklog support. To create a linklog
post, simply add a line defining the external-url in the
YAML block of your post like this:
```yaml
---
layout: post
title: "Setting Up Octopress"
date: 2014-03-31 06:47:11 -0700
comments: true
categories: [octopress, tutorial]
external-url: http://octopress.org/docs/setup/
---
```

