# Structure and outline of this book

[Introduction](README.md)

[Bayesian Network Development](chapter1.md)

[BN Workflows with R and RNetica](workflows.md)
This chapter describes any work-flows / best-practice procedures for saving / accessing / organising your work, as you iteratively develop your BN. This chapter addresses two key components of your work-flow:

* Documentation 
* Network Development
 

Documentation is a very important aspect of developing your BN that is essential to ensuring reproducibility. Good documentation is also vital when working in teams, and also just for your own self -- thank me later. In this section I suggest systems for documenting decisions with respect to the design and parameterisation of your BN.

We tend to build BN's in a piecemeal fashion; building an influence diagram of our domain, correcting the causal structure of the model, setting the levels of our nodes and parameterising them, maybe even building separate sub-models and joining them together to form one large network. 

Following the initial construction, testing and evaluation is necessary: we might make changes to a part or whole of the model and wish to compare the different versions of them. However, this process goes against the grain of version control! Version control tends to follow a more linear process -- of course you can create and then undo changes, reverting or restoring your files to previous versions. Ultimately, we may wish to revert to earlier versions of our network, which we *can* achieve with version control. However, in order to *make* that decision we need to access multiple versions of a part or whole of the network at a single moment in order to carry out analysis for testing and evaluation. How do we manage that with version control? I describe some potential workflows for dealing with this disconcordance between version control and BN development.