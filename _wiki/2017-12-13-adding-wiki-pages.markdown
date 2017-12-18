---
layout: post
title:  "How to add wiki pages"
category: Meta
---

1. Make a GitHub account. If you are on the programming team, you should already have one.

1. Ask the programming lead to add you to the Team-2502 Github organization

1. Clone the [repository](https://github.com/Team-2502/Team-2502.github.io) for this wiki

1. Think about what kind of wiki page you will make. If it's a wiki page related to build, navigate to the `_build` directory. If it's related to maintaining this wiki, navigate to the `_wiki` folder. If it's related to programming, navigate to the `_programming` directory. These directories are called *collections*. The placement of your page will impact which index your page shows up in.

1. Make a new file. Ensure the name is all lowercase, has no spaces, and briefly describes the purpose of the page.

1. Now, you need to add some YAML front matter. YAML front matter goes at the beginning of your file and looks like

{% highlight yaml %}
---
layout: post
title:  "How to add wiki pages"
categories: meta
---
{% endhighlight %}

You will need to edit the title.

Additionally, edit the categories. If your programming page is about how to do something related to wpilib, change the line with categories to `categories: wpilib`. If your build page is related to design, change it to `categories: design`. Do your best to keep your page within the existing categories. The categories will impact the URL of your wiki page. Use categories to sensibly *categorize* your pages.

6\. Once you're done with your page, save, commit and push to the `new-pages` branch

7\. Make a merge request to `master` branch

8\. Once it is accepted, your page will be visible on the wiki!


We use a program called Jekyll for our wiki. Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
