booker
======

Converts diy scanned images into PDF


Process
------

- Take folder of page images and perform OCR. Output  hOCR text file for each
  page
- Compress full-resolution images into compressed but still good quality images
  (jbig2?)
- Combine hOCR and compressed images into PDF. 


Some Additional Requirements
------

* Eye on performance. It would be nice to multithread the process, but anything
  to improve time over the original Homer script would be great.
* It should be configurable so that it can run in a default way but also
  overridden. For example, pdf name and path could just be
  "PARENT_FOLDER/PARENT_FOLDER.pdf". 
* PDFs should be good quality yet not too large in filesize. Homer output was
  good in this reguard. 


Nice To Have (Not vitial)
------

* Email notification when job is completed
* Ability to automactially move file to Google Drive
* Ability to run in a queue situation ( script pulls files to be converted from
  a central system )



Git Basics
------

Here's a good way to use git:

  $ git clone git@github.com:cfitz/booker.git
  $ cd booker
  $ git branch my_branch
  $ git checkout my_branch
  do some work, edit some files, add some files...for this example we just update the README
  $ git add README.md
  $ git commit -m 'here is your commit message. '
  $ git checkout master 
  $ git pull # just a sanity check to make sure nobody else has done updates
  $ git merge my_branch
  $ git push
  $ git branch -d my_branch #delete your branch


This is a really verbose way of doing things, there are lots of shortcuts. 

What you're doing is checking out the code, then making your own branch to work
on ( its a bad idea to work only in the master.. ). You do your work, add your
changes, and commit them to your branch. You then switch back to master, check
if there are any chances upstream, then merge in your branch into the master. 
You then push your master to the remote origin and you delete your local branch.


