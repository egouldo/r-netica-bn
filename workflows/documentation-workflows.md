# Documenting Your Bayesian Networks

Documenting your the ongoing development of your work as well as the final 'product' is extremely important. (NB there will be a section discussing the case for documenting BN's, this part merely explains some practical procedures / workflows for documentaiton).

## Node Tables

(Vegetable Network Paper) - Explain how to set up tables for each of your node that list the parent, children nodes, as well as the conditional behaviour of this node, it's states and their levels also. A Brief description of the node and any other pertinent information about the units of the variable or other structure logic is also relevent. That text may end up going in another document. 

The main purpose of this section is to explain the code / R workflow, which is:

- Have a central ```csv``` file with columns being the different categories of information listed above (i.e. the column of the node table)
- The CSV file must have its first collumn containing the node-names (not titles) so that you can access the table in your Rmarkdown files.
- Within each Rmd document with a node table in it, you load the csv file using ```dplyr::fread```, once only.
- Then, each time you need to access a particular node, you can use ```dplyr:::filter``` to get the row for the relevent node.
- You could also construct a function that then arranges the node's row of data into a nice-looking pander table for your Rmarkdown file.

### Rationale for this workflow:

Having a central csv ensures two things:
1. All your descriptions are easily findable and editable because it is centralised -- there is no duplication across other Rmd files.
2. Your work can be version-controlled -- commit any changes as you work.
