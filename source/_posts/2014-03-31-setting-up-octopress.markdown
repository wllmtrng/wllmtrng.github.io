---
layout: post
title: "Setting Up Octopress"
date: 2014-03-31 06:47:11 -0700
comments: true
categories: [octopress]
external-url: http://octopress.org/docs/setup/
---
[1]: http://octopress.org/docs/deploying
[2]: http://octopress.org/docs/configuring
[3]: http://octopress.org/docs/blogging
[4]: http://webdesign.tutsplus.com/tutorials/getting-started-with-octopress--webdesign-11442

**Note:** I'm also a novice at Octopress as well. As I
learn new things I will post new tips and links to
useful guides. Stay tuned!

Just like the link referenced in the title of this post suggests, **Octopress is a blogging framework for hackers.** I am expecting you as a reader to be someone who is familiar with Git, the terminal (or Windows equivalent).

As a pointer, any post I have with the &rArr; symbol in the title will be a link to the suggested guide I recommend to follow through. Go ahead and click on the link above to start the process of setting up with Octopress!

Be sure to follow the links under the "Next Steps" section to [set up deployment][1], [configure your blog][2], and [start blogging][3]. Below are some tips for each of the section.

##[Setting Up Deployment][1]&rArr;
As you can see, I am using github pages to host my
blog. I would imagine the other two choices would be
just as easy to set up if you are already using that
workflow.

##[Configuring Octopress][2]&rArr;
Now we're approaching the territory of information
overload here if you aren't knowledgeable in Jekyll or
YAML front matter. To narrow mind your focus, all you
need to pay attention to here is:

>In the _config.yml there are three sections for
>configuring your Octopress Blog. Spoiler: You must
>change `url`, and you'll probably change `title`,
>`subtitle` and `author`...

If you're like me and want to know how the heck this
stuff works, refer to Jonathon Cutrell's tuts+ Octopress guide [here][4].

##[Start Blogging!][3]&rArr;
Here you will learn how to create a new post. Executing the command, `rake new_post["Hello World"]`, will
create a post with ending with `.markdown` under the
`.../_posts/` directory. Open the file and you'll get
something like this:

	---
	layout: post
	title: "Hello World"
	date: 2014-03-30 5:59
	comments: true
	external-url:
	categories:
	---

This is a block of YAML front matter telling the blog
generator jekyll how to process the post. To write
content for this post just start writing underneath the
YAML front matter in markdown format.




