---
layout: post
title:  "How to add wiki pages"
date:   2017-12-13 21:39:43 -0600
categories: meta
---

1. Make a GitHub account. If you are on the programming team, you should already have one.

1. Ask the programming lead to add you to the Team-2502 Github organization

1. Clone the [repository](https://github.com/Team-2502/Team-2502.github.io) for this wiki

1. Navigate to the  `_posts` directory and make a new file that follows the convention `YYYY-MM-DD-name-of-post.markdown`

1. Now, you need to add some YAML front matter. YAML front matter goes at the beginning of your file and looks like 

{% highlight yaml %}
---
layout: post
title:  "How to add wiki pages"
date:   2017-12-13 21:39:43 -0600
categories: meta
---
{% endhighlight %}

You will need to edit the title and date as you see fit. The date follows the `YYYY-MM-DD` convention, while the time follows the `HH:MM:SS` 24-hour format. The `-0600` represents the GMT-6 (CST) timezone. 
Additionally, edit the categories. If your page is about how to do something related to build/design, change the line with categories to `categories: build`. If it's related to programming, change it to `categories: programming`. Do your best to keep your page within the existing categories. The categories will impact the URL of your wiki page. For example, a page with `categories: build` will have a URL of `https://team-2502.github.io/build/YYYY/MM/DD/title-of-page.html`. Similarly, a page with `categories: programming auton` will have a url of `https://team-2502.github.io/programming/auton/YYYY/MM/DD/title-of-page.html`. Use categories to sensibly *categorize* your pages.

6\. Once you're done with your page, save, commit and push to the `new-pages` branch

7\. Make a merge request to `master` branch

8\. Once it is accepted, your page will be visible on the wiki!


We use a program called Jekyll for our wiki. Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
