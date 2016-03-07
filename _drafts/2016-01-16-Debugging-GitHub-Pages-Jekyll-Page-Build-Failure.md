---
layout: post
title: "Debugging GitHub Pages Jekyll Page Build Failure"
date: 2016-01-16 16:00:00 -0800
tags: [GitHub Pages, Jekyll]
comments: true
---

Working on my blog
Made a bunch of changes locally and then push to my repo
Public site wasn't updating

What was happening?

Received emails

```
The page build failed with the following error:

Page build failed. For more information, see https://help.github.com/articles/troubleshooting-github-pages-build-failures.

If you have any questions you can contact us by replying to this email.
```

GitHub Settings page also show that there's a problem

TODO Take screenshot of settings page

Okay... What do I do now?

Thinking of my recent changes, the most likely candidate seemed like the code highlighting

Process of elimination
Remove my recent changes
Get the blog building again
Incrementally add in my changes
Surprise! It wasn't the code highlighting, but rather the "post_url" command to cross link between two posts

Here's what that looks like:

```
{% raw %}
_If you are unfamiliar with Entity Framework Code First work flows, please see my previous blog post: [Jumpstart Development with Entity Framework Code First.]({% post_url 2012-10-04-Jumpstart-Development-with-Entity-Framework-Code-First %})_
{% endraw %}
```

It's this part `{% raw %}{% post_url 2012-10-04-Jumpstart-Development-with-Entity-Framework-Code-First %}{% endraw %}` that was breaking the build.

Weird... it works in my local environment

Searching the web I found this GitHub issue on the Jekyll repo
https://github.com/jekyll/jekyll/issues/3051

Way down the page there's the suggestion that it's a time zone issue
Let's give this a try

I live in Portland, which is in the Pacific timezone, so the dates in my posts look like this:

```
---
layout: post
title: "Jumpstart Development with Entity Framework Code First"
date: 2012-10-04 16:00:00 -0800
tags: [Entity Framework, .NET, Database]
comments: true
---
```

The suggested fix is to make sure that your Jekyll configuration (see http://jekyllrb.com/docs/configuration/) specifies a timezone like this:

```
timezone: America/Los_Angeles
```

You can find a list of timezones here:
https://en.wikipedia.org/wiki/List_of_tz_database_time_zones

Publish that change... Viola! That did the trick.

Turns out that others were having the same problem, so it has been suggested that the `post_url` tag match on post.name instead of slugs and dates. See this issue:
https://github.com/jekyll/jekyll/pull/3058

This issue behavior has been changed in version 2.5.2!

Checking the versions for GitHub Pages, we can see that they are currently using 2.4 (at the time of this writing)
https://pages.github.com/versions/
