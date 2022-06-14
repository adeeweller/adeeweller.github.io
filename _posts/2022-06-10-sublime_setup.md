---
toc: true
title: "Setting Up Sublime with R, LaTeX, Python, and More"
categories:
  - Blog
tags:
  - text editor
  - setup
# link: https://github.com
---

**Info Notice:** This page is currently under construction. Please check back in soon.
{: .notice--info}


## Introduction

Are you looking for an easy, fast, and flexible text editor, but aren't sure where to start? Are you easily distracted and want all your files, programs, and projects in the same place? Do you want a editor than can handle a wide array of languages, programs, and platorms? If the answer to any of these questions is yes, then Sublime Text Editor is may be a great fit.

I first started using Sublime as a Political Science major in undergrad -- and I had no clue what I was doing. Like many others, I had no experience with any sort of coding, and just thinking about mysterious lines on a screen made my head spin. And I wasn't using it for python yet, only R and LaTeX. But within a short period of time, I was up and running. 

In this post, let us walk through what Sublime is, why may be the right fit for you, and how to get it set up with R, LaTeX, Python, and more!

## What is Sublime?

Sublime is a text editor. To be more specific, Sublime is a sophisticated, cross-platform source code editor. It supports a variety of programming and markup languages, and features an array of plugins, which are typically community-built and maintained under free-software licenses. You can think about Sublime as the swiss-army knife of text editing. The plugin ecosystem and its extensability make Sublime a worthy choice. It's incredibly fast and lightweight. An annual subscription costs $99 USD, but note that the free trial period is unlimited.

While downloading Sublime is easy, setting it up to work with R, LaTeX, and other platforms is often less straight forward. But don't be intimidated -- it can be quite easy and straight forward. In the following sections, we will walk through setting up Sublime and installing the appropriate plugins. Note too, that for this tutorial, I will be demonstrating the examples for Windows, but I will provide additional information for Mac and Linux when necessary.

## Setting up Sublime

To download Sublime, [follow this link to the Sublime webpage](https://www.sublimetext.com/).


If you are using the free unlimited trial, you may occasionally get a dialogue box prompting you to purchase a license, but if you wish to continue your trial, you can simply exit out of the box.

For the rest of this tutorial, we will be using the extension management system called '**Package Control**.' This is used to install extensions, themes, and color schemes. Since Sublime does not come with Package Control, we will need to install it. To install anything, we need to first open the '**Command Palette**'. The shortcut for this is <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> (<kbd>Command</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> on Mac), although you can also open it from the Preferences tab as well. Using the shortcut, a toolbar will drop down from the top, and search 'install.' The first option should be `Install Package Control.' Select it and hit <kbd>Enter<kbd>.

<figure>
    <a href="/assets/images/install_package_control2.jpg"><img src="/assets/images/install_package_control2.jpg"></a>
    <figcaption>Installing Package Control</figcaption>
</figure>

## Setting up R with Sublime

Sublime can also be an alternative to RStudio. While the visualizations may not be as immediately accessible (for instance, there is no variable viewer in the corner of the screen), it can also be less distracting. Further, all the data remains easily gatherable, and when simulateously writing in LaTeX, everything is in the same application. Again, for someone with a short attention span, the less distractions the better.


## Sublime Merge

A cross-platform Git client via Sublime Text


download

link somehow -->





















<!-- A notice displays information that explains nearby content. Often used to call attention to a particular detail.

When using Kramdown `{: .notice}` can be added after a sentence to assign the `.notice` to the `<p></p>` element. 

**Changes in Service:** We just updated our [privacy policy](#) here to better service our customers. We recommend reviewing the changes.
{: .notice}

**Primary Notice:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec odio. [Praesent libero](#). Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum imperdiet.
{: .notice--primary}

**Info Notice:** Lorem ipsum dolor sit amet, [consectetur adipiscing elit](#). Integer nec odio. Praesent libero. Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum imperdiet.
{: .notice--info}

**Warning Notice:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. [Integer nec odio](#). Praesent libero. Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum imperdiet.
{: .notice--warning}

**Danger Notice:** Lorem ipsum dolor sit amet, [consectetur adipiscing](#) elit. Integer nec odio. Praesent libero. Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum imperdiet.
{: .notice--danger}

**Success Notice:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec odio. Praesent libero. Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at [nibh elementum](#) imperdiet.
{: .notice--success}

Want to wrap several paragraphs or other elements in a notice? Using Liquid to capture the content and then filter it with `markdownify` is a good way to go.

```html
{% raw %}{% capture notice-2 %}
#### New Site Features

* You can now have cover images on blog pages
* Drafts will now auto-save while writing
{% endcapture %}{% endraw %}

<div class="notice">{% raw %}{{ notice-2 | markdownify }}{% endraw %}</div>
```

{% capture notice-2 %}
#### New Site Features

* You can now have cover images on blog pages
* Drafts will now auto-save while writing
{% endcapture %}

<div class="notice">
  {{ notice-2 | markdownify }}
</div>

Or you could skip the capture and stick with straight HTML.

```html
<div class="notice">
  <h4>Message</h4>
  <p>A basic message.</p>
</div>
```

<div class="notice">
  <h4>Message</h4>
  <p>A basic message.</p>
</div> -->