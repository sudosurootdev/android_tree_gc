android_tree_gc
=====================

Building Android for a long time, making lots of changes, using temp branches, etc. causes a lot of space to be wasted by loose objects.

This script uses your build manifest(s) at .repo/manifest.xml (.repo/snippets/\*.xml & .repo/local_manifests/\*.xml) to find the path of each of the projects used in your manifest(s), and then it executes `git prune` & `git gc` on each of the directories.

Use:
====

The best way to use this tool, is to clone the repository and then copy the script into your ~/bin directory. This way if you have more than one Android build working directory you can use this on any or all of them, since we set the **TOP**, for the top of your Android build working directory, and work from there.

Make sure that you call this script from your Android Build **TOP** (containing .repo directory).

If your system is set up correctly, with ~/bin directory in your PATH, you should be able to cd into your Android Build **TOP** and just type **`tighten`**
