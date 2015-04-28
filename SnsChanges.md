# Introduction #

Because we run multiple build configurations per TeamCity project, we've added a screen that shows the state of all the build configurations on a project.  We've also made some additions to the build config page.

# Details #

## Project Page ##

  * The spinners in some of the boxes indicate that they are currently building.
  * The reduce/enlarge buttons resize the boxes, so you can get them all to fit on a single screen.
  * In addition to a monitor showing the entire project status, we have monitors for each team showing them the status of the projects they are working on.  The checkboxes at the bottom allow the team to decide what projects they see.

![http://team-piazza.googlecode.com/svn/wiki/sns-changes/project-page.png](http://team-piazza.googlecode.com/svn/wiki/sns-changes/project-page.png)

## Invidual Build Page ##

  * The page updates via Ajax rather than meta refreshes
  * An image indicates the status of the last build (the big green check)
  * The spinner in the upper right corner indicates the build is in progress (as does the progress bar).  The comments box no longer turns yellow.
  * The elapsed time of the current build
  * The build number link opens the TeamCity project page in a new window

![http://team-piazza.googlecode.com/svn/wiki/sns-changes/individual-build.png](http://team-piazza.googlecode.com/svn/wiki/sns-changes/individual-build.png)