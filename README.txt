rthompson_site v.1.2
#### patch notes ####
-Removed escapedSidebar and sidebar.css
-Removed javascript features that controlled sidebar
-Placed site in a global container for aesthetic reasons
-Added a navbar feature
-Customized color of navbar links
#####################


This website is designed to be simple and customizable. In this document, I will provide instructions on how to make changes, add new pages, and host the website online on Github Pages.

Part 1: Style Changes
If you want to change the colors of the page or the header, you can do this in the myStyle.css page. Just go to the part you want to change and update it to a different hex code (you can find hex codes for colors with tools like google's color picker: https://www.google.com/search?q=color+picker). If you're hosting on a local server, you may need to clear your computer's cache before you see the change. If you're hosting on github, it may take up to 10 minutes for github to implement the change.

Part 2: Adding and Removing Pages
If you want to add a page for a given class, there are a few steps to go through. First, create a new page-- for the sake of this example, we'll call it math120.html, but the name doesn't matter. Copy the text from classTemplate.html into math120.html. Change the name at the top of the page from Sample Name to the name of your course. Then modify the table of assignments and links as you want. Add this new page to your github repository.
Next, go into escapedHeader.txt and replace:
<li class="nav-item active">\
  <a class="nav-link" href="classTemplate.html">Sample Class</a>\
</li>\
with
<li class="nav-item active">\
  <a class="nav-link" href="math120.html">Math 120</a>\
</li>\

In general, you can add a link to any new page by placing the line:
<li class="nav-item active">\
  <a class="nav-link" href="[classID.html]">[Class Name]</a>\
</li>\
before the line </div>\

It is very important that there are no empty lines, and no lines that do not have a '\' at the end of them, as otherwise the header and navbar will not display at all.
To remove a page, just delete it from your directory/repository and remove the corresponding line from the sidebar. Again, it may take GitHub a few minutes to reflect any change.

Part 2b: Adding Assignments to a Class
In classTemplate.html, I've delineated the place to copy the table with the comments "Start Copying Here" and "Stop Copying Here". To add a new row to the table, just copy the text in between those comments and add it to the end of the table, before the <\tbody> tag. Everything within each <td></td> block can be formatted just as it was on the old site.

Part 3: Hosting on Github (Ignore if not using GitHub)
On your Github page, create a repository called "username.github.io". It has to be this specific name, or else you won't be able to use this repository to host the site.
In terminal, make a directory where you want to put the website. Next, cd into that directory, using: 'cd /path/to/directory'.
Type in the command: 'git clone https://github.com/username/username.github.io', replacing username with your username.
Copy the website files into your directory, either using a command: 'cp /path/to/website_files/* /path/to/directory', or by dragging the files in.
In terminal, run the following sequence of commands:
'git add --all'
'git commit -m "Initial commit" '
'git push -u origin master'
Give GitHub up to 10 minutes to update the site, then navigate to username.github.io, and the site should be hosted there.

