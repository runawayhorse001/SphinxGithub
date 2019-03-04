.. _github:

====================
Publishing on Github
====================

.. admonition:: Chinese proverb

	sharing your happiness is much better than enjoying your happiness by your own.
.. |reSTs| replace:: reStructuredTexts

Create |reSTs|
++++++++++++++

Create |reSTs|
--------------

Use the tips in :ref:`rtext` to create your |reSTs| and add them in one folder, for example ``doc``.

.. figure:: images/doc.png


Add them in ``index.rst``
-------------------------

.. code-block:: rst

	========
	Contents
	========

	.. toctree::
	   :maxdepth: 2

	   preface
	   intro
	   pkgs
	   sphinx
	   rtxt
	   github
	   reference


Compile the |reSTs| files
-------------------------

1. Change the directory to the folder 

.. code-block:: bash

	cd MyTutorial/SphinxGithub/doc

2. Compile

.. code-block:: bash

	make

Then you should get two more folders: ``docs`` and ``latex``.

.. figure:: images/compiled.png


Create Repository on Github
+++++++++++++++++++++++++++

.. figure:: images/newr.png


Commit |reSTs| folder to Repository
+++++++++++++++++++++++++++++++++++

Open Terminal and do the following steps:

.. code-block:: bash

	git init

	git add .
	# Adds the files in the local repository and stages them for commit. To unstage a file, use 'git reset HEAD YOUR-FILE'.

	git commit -m "First commit"
	# Commits the tracked changes and prepares them to be pushed to a remote repository. To remove this commit and modify the file, use 'git reset --soft HEAD~1' and commit and add the file again.

	git remote add origin remote repository URL
	# Sets the new remote
	git remote -v
	# Verifies the new remote URL

	git push -u origin master
	# Pushes the changes in your local repository up to the remote repository you specified as the origin

Setup Github Pages on Github
++++++++++++++++++++++++++++

Repository 
----------

Once you commited your repository to the Github, you will get: 

.. figure:: images/repository.png

Setup Github Pages
------------------

1. **Go to Settings button in your repository**

.. figure:: images/setting.png

2. **Set up the Github pages source**

.. figure:: images/githubpage.png

3. **Enjoy your Github Pages**

.. figure:: images/online.png


