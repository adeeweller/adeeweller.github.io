---
toc: true
title: "Setting Up Sublime Text with LaTeX"
author_profile: true
categories:
  - Blog
  - Tutorial
tags:
  - text editor
  - setup
  - LaTeX
  - Sublime
header: 
  image: assets/images/sublime_latex.jpg
---



## Introduction

In this series, we will be walking through how to set up Sublime Text Editor -- a fast, flexible, and user-friendly text editor -- for a variety of different programming languages and softwares. (For a more in-depth discussion on the value and pitfalls of Sublime, check out my previous post on Sublime and R.)

In this post, I will work through how to get Sublime set up to write in LaTeX, a typesetting software that is used by publishers and professionals alike. Easily customizable, LaTeX is often far preferred over processors like Microsoft Word in academia. In short, it makes documents, posters, presentations, and other formats clean, clear, and professional.

For this tutorial, I assume you already have Sublime downloaded and set up on your computer. If you haven't done that yet, do it! Or at least, stop reading here, and go do something fun while there's still time.



## What is LaTeX and why is it useful?

LaTeX (pronounced _lay-tek_ by some and _lah-tek_ by others) is a software system used to typeset documents. Unlike programs like Word, which pre-define formats and layout of documents, LaTeX is a more flexible and customizable option. Unfortunately, this also means there is a bit more of a learning curve than a simple point-and-click system, as more options need to be defined _ex ante_. However, this program is quite simple and usually intuitive once mastered, and will soon Word feel clunky and restrictive.

Widely used in academia, becoming comfortable with LaTeX is a critical skill for many junior scholars. With it, one can produce beautiful tables, figures, articles, presentations, posters, C.V.s, resumes, books, cover letters, and a whole range of other documents. LaTeX is also highly functional in multilingual environments and non-Latin scripts, typesetting complex mathematical equations, and adding extensive tables. 

To produce a LaTeX product, we will edit an input, through which the software will produce an output (usually a PDF) upon each build. This is different from Word, where both of these are displayed to the user as one joint product. We won't be covering how to format things in LaTeX here (check out [one of many online tutorials here](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)), just getting everything set up.



## Setting up LaTeX with Sublime

### Downloading Software

Let's start by downloading three pieces of software:

* [MiKTeX](https://miktex.org/download): Open-source TeX distribution

* [SumatraPDF](https://www.sumatrapdfreader.org/download-free-pdf-viewer): Lightweight, clickable PDF viewer

* [ImageMagick](https://imagemagick.org/script/download.php#windows): Open-source software for editing and manipulating digital images

Follow the installation directions for each, and as always, be cognizant about what paths you are using to store the files.

Got them? Great.

## Settings Adjustments


To set up LaTeX within Sublime, we need to ensure that Package Control is successfully installed. With Sublime open, click <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>. The dropdown Package Control display should appear, like this:

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/package_control.jpg "Package Control"){: .align-center}

If it does not, try installing Package Control again.

Assuming you're still on board, let's change a few of the Package Control settings.

Follow the path to Package Control Settings: <kbd>Preferences</kbd> + <kbd>Package Settings</kbd> + <kbd>Package Control</kbd> + <kbd>Settings</kbd>

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/path_to_pc_sttings.jpg "Path to Package Control Settings"){: .align-center}


This will open up two panels. The left panel is preset settings, while the right is for user settings. We'll be using the right one. Copy and add the following code:

<kbd>
{
	"bootstrapped": true,
	"in_process_packages":
	[
	],
	"installed_packages":
	[
		"Agila Theme",
		"CiteBibtex",
		"Citer",
		"Grammatical Framework",
		"ImageMagick",
		"knitr",
		"Language - Spanish",
		"LaTeX Word Count",
		"LaTeXing",
		"LaTeXTools",
		"LSP",
		"LSP-Grammarly",
		"LSP-ltex-ls",
		"LSP-R",
		"Package Control",
		"Pandoc",
		"R-Box",
		"R-IDE",
		"SendCode",
		"sublime-github",
		"SublimeLinter",
		"SublimeLinter-contrib-write-good",
		"SublimeREPL",
		"Terminus",
		"View In Browser",
	],
}
</kbd>


![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/pc_settings2.jpg "Package Control Settings"){: .align-center}

(Depending on what you use, your final packages will undoubtedly look different from mine!)

Save and close the settings file. This will initiate Sublime to start downloading and setting up all the packages, and can take up to 15 minutes. Grab a coffee or a snack during this time.

In the meantime, we can adjust some of the other settings. Open Prefence settings by selecting <kbd>Preferences</kbd> + <kbd>Settings</kbd>.

Here you can customize the font size, color scheme, and other pretty factors.

Once some time has passed, we can check if all the packages have been successfully installed by following: <kbd>Preferences</kbd> + <kbd>Package Settings</kbd> + <kbd>Latex tools/kbd> + <kbd>Check system</kbd>.

Sublime will run through the files and issue any warnings that arise. All programs should say 'Available'.

## Opening a Document

To build a PDF, open any .tex file (a LaTeX file) in Sublime. Note that if you have errors, the PDF may not compile. But if everything is working, the PDF should automatically be built upon <kbd>CTRL</kbd> + <kbd>b</kbd> and open in Sumatra. 

On the Sumatra PDF, double click anywhere on the page, which will take you to the respective location in Sublime.


Some other helpful editing tips:

* <kbd>CTRL</kbd> + <kbd>r</kbd> shows all sections by their headers for easy navigation.

* You can save whole LaTeX projects, just like in R, with multiple folders, or just keep track of your paths.

* LaTeX preambles (the bit that formats the document) can be a bit repeatitive. I often copy and paste, adjusting as needed to save time.

* To select multiple lines simultaneously, hold down <kbd>CTRL</kbd> as you click.

And with that, you should be off to the races! Or at least, off to the publishers.

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
