---
difficulty: 1
training: true
chapter: "Chapter 5: Best Practices"
tags: vue
---

# Fix the HTML Injection Vulnerability

In this challenge, we've created a dummy blog post that allows users to add rich text comments.

BUT the current implementation is a HUGE security risk. Yes, it allows users to add nicely formatted comments
but any commenter could also execute arbitrary JavaScript code on our page (a big deal if we were actually saving these comments to a database and displaying for other users). This is known as a cross-site scripting (or XSS) attack.

Your task is to refactor the commenting feature to be secure.

You could accomplish this in several ways:

1. Support markdown for commenting instead of html ([markdown-it](https://github.com/markdown-it/markdown-it) could be useful)
2. or use an HTML sanitizer like [@jitbit/HtmlSanitizer](https://github.com/jitbit/HtmlSanitizer)
3. or remove support for rich text and only allow plain text comments

> 💡 HINT: `@jitbit/HtmlSanitizer` and `markdown-it` are already installed in the project

In the solution, we use the markdown approach but the option you take is up to you. Just fix the security risk!

## Requirements

1. Refactor the code to eliminate the XSS security risk

> 💡 HINT: You'll want to work in `components/BlogPostComments.vue`

## Screenshot of the XSS Attack

![Screenshot of the xss attack](https://images.certificates.dev/csvd-training-code-challenge-18-before.gif)

## Screenshot of the Solution

![Screenshot of the solution](https://images.certificates.dev/csvd-training-code-challenge-18.gif)
