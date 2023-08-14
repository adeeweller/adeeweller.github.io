---
toc: true
title: "Setting Up Sublime Text with R"
author_profile: true
categories:
  - Blog
  - Tutorial
tags:
  - text editor
  - setup
  - R 
  - Sublime
header: 
  image: assets/images/sublime_R.jpg
---



## Introduction

Are you looking for an easy, fast, and flexible text editor, but aren't sure where to start? Are you easily distracted and want all your files, programs, and projects in the same place? Do you want a editor than can handle a wide array of languages, programs, and platorms? If the answer to any of these questions is yes, then Sublime Text Editor is may be a great fit for you.

I first started using Sublime as a Political Science major in undergrad -- and I had no clue what I was doing. Like many others, I had no experience with any sort of coding, and just thinking about mysterious lines on a screen made my head spin. And I wasn't using it for python yet, only R and LaTeX. But within a short period of time, I was up and running. 

In this post, let us walk through what Sublime is, why may be the right fit for you, and how to get it set up with R. In future posts, we will work through how to set it up with LaTeX, python, markdown, and much more!

But before we continue, I assume in this tutorial that you already have R dowloaded on your computers. If you have not, please [do so here.](https://cloud.r-project.org/) For more information on R, check out their [introduction here.](https://www.r-project.org/about.html)

## What is Sublime?

Sublime is a text editor. To be more specific, Sublime is a sophisticated, cross-platform source code editor. It supports a variety of programming and markup languages, and features an array of plugins, which are typically community-built and maintained under free-software licenses. You can think about Sublime as the swiss-army knife of text editing. The plugin ecosystem and its extensability make Sublime a worthy choice. It's incredibly fast and lightweight. An annual subscription costs $99 USD, but note that the free trial period is unlimited.

While downloading Sublime is easy, setting it up to work with R, LaTeX, and other platforms is often less intuitive. But don't be intimidated -- it can be quite easy and straight forward. In the following sections, we will walk through setting up Sublime and installing the appropriate plugins. Note too, that for this tutorial, I will be demonstrating the examples for Windows, but I will provide additional information for Mac and Linux when possible.

## Setting up Sublime

To download Sublime, [follow this link to the Sublime webpage](https://www.sublimetext.com/). Download the appropriate **.exe** file for your computer from the home page. Go ahead and run the executable file through the Setup Wizard that appears. If you want to save the program in a non-default location, this is when you can do it. Otherwise, you can keep hitting next and finally, install.

That's it! You've successfully installed Sublime. Remember, if you are using the free unlimited trial, you may occasionally get a dialogue box prompting you to purchase a license, but if you wish to continue your trial, you can simply exit out of the box.

For the rest of this tutorial, we will be using the extension management system called '**Package Control**.' This is used to install extensions, themes, and color schemes. Since Sublime does not come with Package Control, we will need to install it. To install anything, we need to first open the '**Command Palette**'. The shortcut for this is <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> (<kbd>Command</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> on Mac), although you can also open it from the Preferences tab. Using the shortcut, a toolbar will drop down from the top, and search 'install.' The first option should be `Install Package Control.' Select it and hit <kbd>Enter<kbd>. It may take a minute.

After it is installed, I would recommend closing Sublime and re-opening it before we move to the next steps.

## Setting up R with Sublime

Sublime can be an nice alternative to RStudio, especially when writing multi-format articles or working in both R and LaTeX simultaneously. While the visualizations may not be as immediately accessible (for instance, there is no variable viewer in the corner of the screen, like there is in RStudio), it can also be less distracting. Further, all the data remains easily accessible, and when simulateously writing in LaTeX, everything is in the same application. Again, for someone with a short attention span, the less distractions the better.

Let's start with a blank .R file in Sublime. Open a file and save it as "file.R" -- this let's Sublime know you are working on an R file and it will automate some of the commands.

To set up R within Sublime, we need to install the appropriate packages. Again, open the Command Package and search 'install.' Now, '**Package Control: Install Package**' should be the first option. Select it and hit enter. This may take a moment.

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/install_package_control2.jpg "Installing Packages"){: .align-center}

From there, all the available repositories will be available to be chosen.

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/package_control.jpg "Package Control"){: .align-center}

Now, we need to install the following packages:

* _'sublime-ide-r'_
   + A package maintained by randy3k that transforms Sublime into R-Studio with some cool features added (formerly R-IDE).


* _'SendCode'_
   + This sends code from the text editor to be run in either the terminal or in the R user interface (RGui). 


(As a note, you can set this part up a couple different ways. You can send the code directly to the R GUI, send it to a terminal, or some other shell. To do that, use the package _'Terminus'_ and set that up instead. In this tutorial, we will be sending it to R's interface. However, know that there are options out there and pick the one that is best for you.)


![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/install_sendcode.jpg "Installing SendCode"){: .align-center}

Once those two are installed, open Package Control back up and select the option that says '*SendCode: Choose Program*' and hit enter. Sublime will open a list of all the consoles where the code can be sent.

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/sendcode1.jpg "Send Code Program Selection (1)"){: .align-center}

From there, you can select the program that you want to send the R script to -- choose R GUI. You can also use RStudio if you refer, but this page is set up for the R base. 

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/sendcode2.jpg "Send Code Program Selection (2)"){: .align-center}

The next step is to let Sublime know where the R GUI is located. To make the appropriate path to R, go to 'Preferences' then 'Package Settings' at the bottom of the drop-down tab. From there, we can access all the settings for our downloaded packages. Find the one for R-IDE and open Settings. 

Next, we will define the path for Sublime to access R. Hover over *Preferences* to *Package Settings* to *sublime-ide-r* to open the user settings. 

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/ide_r_settings1.jpg "Opening R-IDE Settings"){: .align-center}


You won't need to edit settings on the left -- these are the universal settings. We will focus on the panel on the right, where user settings are located. Edit the path to R to match the path to the .exe file in R. See the highlighted text below. This path must match exactly. Once this is changed, you can save the settings and exit them out. 

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/ide_r_settings2.jpg "Opening R-IDE Settings"){: .align-center}

Now you should be set up! Open the R GUI on one panel and your R script in Sublime on another. To run a line of code that you have written in Sublime in R, simply select it and hit <kbd>Ctrl</kbd> + <kbd>Enter</kbd>. The line and output should appear on the screen in the R GUI. Run whole files with ease!

Finally, this process only ever needs to be repeated once. Now you are ready to start maintaining, cleaning, analysing, and visualizing your data!














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