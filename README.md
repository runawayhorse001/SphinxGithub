# Sphinx Github Pages Tutorial	

 Website:  https://runawayhorse001.github.io/DatamingTutorial	


 This document is a summary of my Sphinx 


BTW, the ``sphinx-to-github`` function for github pages  can be easily solved by add  an empty file ``.nojekyll ``  to your docs folder.  I add the following piece of code to add it automatically: 


```
# add .nojekyll file to fix the github pages issues
nojekyll_path = os.path.join(outdir, '.nojekyll')
if not os.path.exists(nojekyll_path):
    os.makedirs(nojekyll_path)

```