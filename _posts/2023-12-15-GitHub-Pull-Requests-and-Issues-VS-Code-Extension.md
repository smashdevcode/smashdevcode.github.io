---
layout: post
title: "GitHub Pull Requests and Issues VS Code Extension"
date: 2023-12-15 09:00:00 -0800
tags: [GitHub, Visual Studio Code, Extensions]
comments: true
---

The other day I was starting to review a large pull request on GitHub's website. I was getting frustrated with the experience (overall slowness of the web UI), so I decided to see if there was a better way. I found the GitHub Pull Requests and Issues extension for Visual Studio Code.

This extension allows you to view and comment on pull requests and issues directly within Visual Studio Code. For large pull requests, it's a much better experience than using the GitHub website, and it's a great way to stay in the flow of your work.

## Installing the Extension

The extension is available in the [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github). You can install it from within Visual Studio Code by searching for "GitHub Pull Requests and Issues" in the Extensions tab.

After installing the extension, you'll need to sign in to GitHub (VS Code should be prompt you to do this).

## Using the Extension

You'll see a new icon in your Activity Bar (the left sidebar within VS Code). Clicking on this icon will open the Pull Requests and Issues tab.

![GitHub Pull Requests and Issues Activity Bar Icon](/images/github-pull-requests-and-issues-vs-code-extension/github-pr-vs-code-extension1.png)

The Pull Requests tab will show you all of the pull requests for the repository you have open in VS Code. You can create a new pull request by clicking on the "Create Pull Request" button at the top of the tab.

![GitHub Pull Requests and Issues Pull Requests Tab](/images/github-pull-requests-and-issues-vs-code-extension/github-pr-vs-code-extension2.png)

Then you can select your base branch, provide a name and description, and click the "Create" button.

![GitHub Pull Requests and Issues Create Pull Request](/images/github-pull-requests-and-issues-vs-code-extension/github-pr-vs-code-extension3.png)

After creating the pull request, you'll see it in the Pull Requests tab.

![GitHub Pull Requests and Issues Pull Requests Tab](/images/github-pull-requests-and-issues-vs-code-extension/github-pr-vs-code-extension4.png)

Now for the good part! You can easily review and comment on any file in the pull request by clicking on the file in the Pull Requests tab. To add a comment, hover over the line of code you want to comment on and click the "+" button.

![GitHub Pull Requests and Issues Pull Requests Tab](/images/github-pull-requests-and-issues-vs-code-extension/github-pr-vs-code-extension5.png)

After writing your comment, you can add the comment or start a review.

![GitHub Pull Requests and Issues Pull Requests Tab](/images/github-pull-requests-and-issues-vs-code-extension/github-pr-vs-code-extension6.png)

You can also reply to existing comments or resolve conversations.

![GitHub Pull Requests and Issues Pull Requests Tab](/images/github-pull-requests-and-issues-vs-code-extension/github-pr-vs-code-extension7.png)

## Give It a Try

_Want to give it a try?_ I created a simple "Happy Holidays" repository that you can use to test out the extension. Send me a message and I'll add you as a collaborator (or you can fork the repo and create your own pull request). You can find it here: [smashdevcode/happy-holidays](https://github.com/smashdevcode/happy-holidays/pull/1).

## Resources

If you'd like to learn more pull requests and using the GitHub Pull Requests and Issues extension, check out the following YouTube video:

[YouTube: Pull Requests in VS Code](https://www.youtube.com/watch?v=LdSwWxVzUpo)
