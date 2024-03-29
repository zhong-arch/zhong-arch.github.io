---
layout: post
title:  "Hosting and formatting resume"
date:   2022-10-13 14:35:10 -0500
categories: jekyll update
---

## Title: Hosting and formatting resume

## Purpose: Describe the practical steps of how to host and format a resume using the software stack
The software stack includes Markdown, a Markdown editor,
GitHub Pages, and Jekyll.

## Prerequisites: 
>1. We need to prepare a resume that is formatted in Markdown, some of the steps are illustrated in the instructions below.

>2. We need to install Ruby and Jekyll as a static website generator to process the files into websites.

>3. Using markdown requires a markdown editor, I used the Virtual Studio Code to edit the resume in markdown format. The Virtual Studio Code could install the dynamic markdown side-by-side extension, I could preview the document after I made any edition to my markdown files.

## Instructions:
According to Etter, there are multiple strengths of lightweight makeup because writing XML(Extensible Markup Language) by hand is crazy, markdown is the most widely used lightweight markup language, it has the cleanest syntax. Markdown is chosen to be used in this resume documentation. 

### More Resources:
Markdown tutorial: https://www.markdownguide.org/basic-syntax/  
Etter’s book: https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS  
Gitbub and Jekyll tutorial: https://www.youtube.com/watch?v=EmSrQCDsMv4

We need to host the resume as a static website. Etter pointed out that Distributed Version Control such as Github could help users to store their documentation and shared it with other users. Etter also suggested that each documentation should place a file named “README.md” in order to provide a summary of the product that is documented, and instructions about building the documentation locally and how to contribute it. So, before we build websites, we need to set up our own Github site.

- On the homepage of the GitHub, we need to create a new repository and name it” your username.github.io”.  
- Click the “setting”, Under the “Github pages”, click the “Check it out here!”, a new website link will be created, copy the address of the link.  
- Go back to the main page of the repository, click the “setting” button at the right of “About”, paste the link in the box of “Website”, and click “Save changes”. Now, the website link will be displayed under the “About”.

Now, we need to clone the new repository to the Virtual Studio Code in the computer. 

- Open the Virtual Studio Code, Click the “source control” tab on the top left corner.  
- Clone the repository to the computer, open the repository, now, we could see all files are displayed at the left panel of explorer. 

According to Etter, we could manually create a simple static website but it is quite complex, we could use a generator to process it. I chose Jekyll among some of the website generators recommended by Etter. We could set up the Jekyll.

- Open the Virtual Studio Code, open the resume Markdown file.
- Click Terminal – New Terminal.  
- Type “Jekyll new . – force” in the terminal, the Jekyll will automatically create a bunch of files in the repository.  
- Type “bundle exec jekyll serve” in the terminal, the Jekyll will create a site. If there are errors, please type “bundle add webrick” before “bundle exec jekyll serve”. There will be a local server address revealed on the terminal. You could open it to see the created webpage by Jekyll. If we typed “bundle exec jekyll serve –livereload”, all changes will be automatically revealed on the web browser without any refresh implementations.  
- Click into the Gemfile file in the repository, comment out the “gem “Jekyll”, “~>4.22 “ by adding ‘#’ before the lines. Uncomment the “gem “github-pages”, group: Jekyll_plugins” by deleting the ‘#’. The reason for these implementations is Github may not support everything that jekyll supports. It could limit functionality to what GitHub could provide. Save the Gemfile.  
- We should type “bundle update” in the terminal to update the bundle.  
- Type “bundle install” in the terminal to install the bundle.  
- Now, it is time to commit changes to the Github. We could click “commit” button on the source control panel and type messages to commit it.  
- Next, in the “_config.yml” file, we should change the “url” to the website address to the link that we created in the Github described above. 

Now, we could start work on the resume to put it on the website.
- Under the “_posts” folder, create a new file with year-month-day-filename format.  
- Under the same folder, there is a file named “welcome-to-Jekyll.markdown”, Copy the title information include layout, title, date and categories.
- Paste them in the new file, change the title and date, I changed the title to “my resume”.
- Copy all contents from the resume to the new file. Now, we could see the link of the resume on the homepage of the created website.  
- Terminate the local server.  
- Click into the “_config.yml” file, change the “title” and email address.   
- We could edit the “twitter_username” and “github_username” here as well. 

![animated resume](/assets/resume_animated.gif)

## Authors and Acknowledgements: 
The Jekyll theme is default “minima”.
Author: Zhong He
Group members: Chowdhury Abdul Mumin Ishman, PokYee Tsu, Sungjae Hyun, Kieran Ketelsen

## FAQs
>1. Why is Markdown better than a word processor?
According to Ettr, PDFs created by word processor required to be downloaded onto hard drives and then sit there, users may never update them. In contrast, users could always update markdown files. Ettr also pointed out that hosting the content on a website with Markdown format could fix content instantly and keep the content in sync with the latest software release. Markdown has more features than the word processor, it is more convenient if users could it well.

>2. Why is my resume not showing up?
There are multiple factors that caused the problem that the resume could not be shown up on the webpage. The Jekyll should be properly configured, the resume could be displayed well after the above steps are implemented well. The Github server required some time to update your changes on the website after you commit and pushed your changes.
