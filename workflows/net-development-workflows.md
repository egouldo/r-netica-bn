# Workflows for iteratively developing your network

## THE PROBLEM:

As we have seen in (SECTION ABOUT THE CYCLE OF DEVELOPMENT)... Developing a Bayes Net is an inherently iterative process that might continue for days, weeks, or even months. 

Other code development projects are also iterative, we add new lines and delete buggy, redundant, or otherwise unwanted lines. However, there is a difference in the necessary workflow for managing the development of your net because when we construct bayes nets we might like to retract changes we make, revert to an old version of the net, or even compare different versions of a whole or a part of our nets (essentially two different networks!). In this case version-controlling a single file for your net isn't the most useful workflow anymore...



Workflow thoughts: still not sure of exactly the best workflow to implement... in terms of versioning different versions of the int.

For documentation purposes, we might like to demonstrate different iterations of the net. Consequently when we use the regular git versioning workflow where we simply make changes to an existing model e.g. a text file of a Netica Net. (reminds me that should have an entry on setting up textiles and git-- recommend saving as .dne rather than .neta -- MUST for RNetica anyway). SO the problem is -- do we save each new version as a different file -- MANY files?? For a large project, this could become unwieldy.? Also it kind of defeats the purpose of using a GIT versioning system, and you still have the pre-git problem of having different names for files... Another workaround is to be meticulous in documenting your work as you go -- take PICTURES as you go if you want to include them (save as PNGs to version if you want to include in your rendered RMarkdown files).  OR we simply have a 'REMAKE' system implemented that runs each of the different model iteration steps. AND you have a great system for documenting )(and potentially visualising) what each of the files do -- See Fin's links.

### SOLUTIONS

WHAT ABOUT BRANCHING??
Well all good and all, but what happens when we wish to compare different versions of the model, say we wish to perform a sensitivity analysis on two versions of the same network? Branches are not useful then, because one you can't access different versions if they're on different branches at the same time. Two because once it comes time to merging your branches

## ANOTHER PROBLEM:

DOCUMENTING YOUR WORK USING RMD... RMD tends to be a bit of a 'linear' process... BUT the thing about Bayes Nets, is that there is nothing linear about them. We construct them in pieces,

MAKING CHANGES IN SCRIPTS VERSUS READING AND WRITING TO YOUR NETWORK IN RMD... you want to document your code right? But every time you knit your Rmd files, you don't want to be over-writing your network.. what's the solution??

REMAKE that Finn mentioned could be a good get around.