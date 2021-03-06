---
title:  How did I put this website up in 5 minutes
header:
  teaser: https://jekyllrb.com/img/logo-2x.png
  og_image: https://jekyllrb.com/img/logo-2x.png
categories: 
  - Programming
tags:
  - Jekyll
  - Github
  - GithubPages
---

Due to the recent changes in life, I figured that I need to do something different, or learn something different.
Obviously, being a firmware/electronics engineer, I live in early ages in the context of software engineering. My 
bread and butter is C/C++ and Assembly and still lives in a world where memory and processing power considered to be
very scared resources. In addition to the above, I use fair-bit of Python for some high level visualization/data analysis 
and automation tasks.

Having said that, a friend of mine recommended [Jekyll] to me. It is a simple static blog aware platform where all your text
files written in markdown format are rendered as static web pages. The beauty of this is the user do not need to maintain 
any databases etc, or should worry about the capabilities of the web-host. [Github Page]s fully supports Jekyll hence the hosting
is free. 

I did the following.

1. Searched for Jekyll template designs and found [Minimal Mistakes] is very appealing.
2. Forked the [Minimal Mistakes] repository to my own [Github Account] and cloned it
3. Edit the `_config.yml` file to cater for the website.
4. Went to the repository settings and made it available as a [Github page].
5. Setup the [DNS] records on my domain name.
6. Forced [https] on Github (repository settings)
7. Write this post in [markdown] and put to the `_posts` directory
8. Push the page to the repository
9. Done 

Yep, thats all. Simple as that.

Any questions? Ask below. I'll explain as much as I can.

[Jekyll]:https://jekyllrb.com/
[Minimal Mistakes]:https://github.com/mmistakes/minimal-mistakes/fork
[Github Account]:https://github.com/samithar/jekyll
[Github page]:https://pages.github.com/
[DNS]:https://help.github.com/articles/using-a-custom-domain-with-github-pages/
[https]:https://help.github.com/articles/securing-your-github-pages-site-with-https/
[markdown]:https://raw.githubusercontent.com/samithar/jekyll/gh-pages/_posts/2018-07-01-How_I_put_this_up.md
