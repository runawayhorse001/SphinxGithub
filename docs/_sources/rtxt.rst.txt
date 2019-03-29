.. _rtext:

=======================
reStructuredText Markup
=======================

.. admonition:: Chinese proverb

	Making full preparation will not delay your job but quicken the process. – old Chinese proverb


reStructuredText Primer
+++++++++++++++++++++++

I would refer the reader to [Sphinx2019]_ and [Georg2018]_ for more details.

Sections
--------

Sections are identified through their titles, which are marked up with adornment: "underlines" below the title text, or underlines and matching "overlines" above the title. More details can be found at: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#sections

reStructuredText:

.. code-block:: rst

	===============
	 Section Title
	===============

	Subsection Title
	++++++++++++++++

	Subsubection Title
	------------------


Paragraphs
----------

The paragraph is the most basic block in a reST document. 
Paragraphs are simply chunks of text separated by one or 
more blank lines. As in Python, indentation is significant 
in reST, so all lines of the same paragraph must be 
left-aligned to the **same level of indentation**. More 
details can be found at: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#paragraphs

1. **General Paragraphs**

reStructuredText:

.. code-block:: rst

	This is the first demo paragraph. The blank line above 
	the first line is required; The blank line below the last
	line is required. 

	This is the second demo paragraph. The blank line above 
	the first line is required; The blank line below the last
	line is required. 

Syntax diagram:

.. code-block:: rst

	+------------------------------+
	| paragraph                    |
	|                              |
	+------------------------------+

	+------------------------------+
	| paragraph                    |
	|                              |
	+------------------------------+


Result:

This is the first demo paragraph. The blank line above the first 
line is required; The blank line below the last line is required. 

This is the second demo paragraph. The blank line above the first 
line is required; The blank line below the last line is required. 

2. **Bullet Lists Paragraphs**


reStructuredText:

.. code-block:: rst

	- This is the first bullet list item.  The blank line above the
	  first list item is required; blank lines between list items
	  (such as below this paragraph) are optional.

	- This is the first paragraph in the second item in the list.

	  This is the second paragraph in the second item in the list.
	  The blank line above this paragraph is required.  The left edge
	  of this paragraph lines up with the paragraph above, both
	  indented relative to the bullet.

	  - This is a sublist.  The bullet lines up with the left edge of
	    the text blocks above.  A sublist is a new list so requires a
	    blank line above and below.

	  - This is a sublist.  The bullet lines up with the left edge of
        the text blocks above.  A sublist is a new list so requires a
        blank line above and below.    

	- This is the third item of the main list.

	This paragraph is not part of the list.

Syntax diagram:

.. code-block:: rst

	+------+-----------------------+
	| "- " | list item             |
	+------| (body elements)+      |
	       +-----------------------+

Result:

- This is the first bullet list item.  The blank line above the
  first list item is required; blank lines between list items
  (such as below this paragraph) are optional.

- This is the first paragraph in the second item in the list.

  This is the second paragraph in the second item in the list.
  The blank line above this paragraph is required.  The left edge
  of this paragraph lines up with the paragraph above, both
  indented relative to the bullet.

  - This is a sublist.  The bullet lines up with the left edge of
    the text blocks above.  A sublist is a new list so requires a
    blank line above and below.

  - This is a sublist.  The bullet lines up with the left edge of
    the text blocks above.  A sublist is a new list so requires a
    blank line above and below.    

- This is the third item of the main list.

This paragraph is not part of the list.


3. **Bullet Lists Paragraphs**


reStructuredText:

.. code-block:: rst

	1. This is the first bullet list item.  The blank line above the
	   first list item is required; blank lines between list items
	   (such as below this paragraph) are optional.

	2. This is the first paragraph in the second item in the list.

	   This is the second paragraph in the second item in the list.
	   The blank line above this paragraph is required.  The left edge
	   of this paragraph lines up with the paragraph above, both
	   indented relative to the bullet.

	   a. This is a sublist.  The bullet lines up with the left edge of
	      the text blocks above.  A sublist is a new list so requires a
	      blank line above and below.

	   b. This is a sublist.  The bullet lines up with the left edge of
	      the text blocks above.  A sublist is a new list so requires a
	      blank line above and below.


	3. This is the third item of the main list.

Result:

1. This is the first bullet list item.  The blank line above the
   first list item is required; blank lines between list items
   (such as below this paragraph) are optional.

2. This is the first paragraph in the second item in the list.

   This is the second paragraph in the second item in the list.
   The blank line above this paragraph is required.  The left edge
   of this paragraph lines up with the paragraph above, both
   indented relative to the bullet.

   a. This is a sublist.  The bullet lines up with the left edge of
	  the text blocks above.  A sublist is a new list so requires a
	  blank line above and below.

   b. This is a sublist.  The bullet lines up with the left edge of
	  the text blocks above.  A sublist is a new list so requires a
	  blank line above and below.

3. This is the third item of the main list.

Syntax diagram:

.. code-block:: rst

	+-------+----------------------+
	| "1. " | list item            |
	+-------| (body elements)+     |
	        +----------------------+

Result:

1. This is the first bullet list item.  The blank line above the
   first list item is required; blank lines between list items
   (such as below this paragraph) are optional.

2. This is the first paragraph in the second item in the list.

   This is the second paragraph in the second item in the list.
   The blank line above this paragraph is required.  The left edge
   of this paragraph lines up with the paragraph above, both
   indented relative to the bullet.

   a. This is a sublist.  The bullet lines up with the left edge of
      the text blocks above.  A sublist is a new list so requires a
      blank line above and below.

   b. This is a sublist.  The bullet lines up with the left edge of
      the text blocks above.  A sublist is a new list so requires a
      blank line above and below.


3. This is the third item of the main list.

4. **Blocked Paragraphs**

a. **Line Blocks**

reStructuredText:

.. code-block:: rst

	Take it away, Eric the Orchestra Leader!

	    | A one, two, a one two three four
	    |
	    | Half a bee, philosophically,
	    |     must, *ipso facto*, half not be.
	    | But half the bee has got to be,
	    |     *vis a vis* its entity.  D'you see?
	    |
	    | But can a bee be said to be
	    |     or not to be an entire bee,
	    |         when half the bee is not a bee,
	    |             due to some ancient injury?
	    |
	    | Singing...

Syntax diagram:

.. code-block:: rst

	+------+-----------------------+
	| "| " | line                  |
	+------| continuation line     |
	       +-----------------------+

Result:

Take it away, Eric the Orchestra Leader!

    | A one, two, a one two three four
    |
    | Half a bee, philosophically,
    |     must, *ipso facto*, half not be.
    | But half the bee has got to be,
    |     *vis a vis* its entity.  D'you see?
    |
    | But can a bee be said to be
    |     or not to be an entire bee,
    |         when half the bee is not a bee,
    |             due to some ancient injury?
    |
    | Singing...

5. **Doctest Blocks**

reStructuredText:

.. code-block:: rst

	This is an ordinary paragraph.

	>>> print 'this is a Doctest block'
	this is a Doctest block

	The following is a literal block::

	    >>> This is not recognized as a doctest block by
	    reStructuredText.  It *will* be recognized by the doctest
	    module, though!

Result:

This is an ordinary paragraph.

>>> print 'this is a Doctest block'
this is a Doctest block

The following is a literal block::

    >>> This is not recognized as a doctest block by
    reStructuredText.  It *will* be recognized by the doctest
    module, though!

3. **Field Lists**

reStructuredText:

.. code-block:: rst

	:Date: 2001-08-16
	:Version: 1
	:Authors: - Me
	          - Myself
	          - I
	:Indentation: Since the field marker may be quite long, the second
	   and subsequent lines of the field body do not have to line up
	   with the first line, but they must be indented relative to the
	   field name marker, and they must line up with each other.
	:Parameter i: integer

Result:

:Date: 2001-08-16
:Version: 1
:Authors: - Me
          - Myself
          - I
:Indentation: Since the field marker may be quite long, the second
   and subsequent lines of the field body do not have to line up
   with the first line, but they must be indented relative to the
   field name marker, and they must line up with each other.
:Parameter i: integer


Table
-----

More details can be found at: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#grid-tables

1. **Grid Tables**


reStructuredText:

.. code-block:: rst

	+------------------------+------------+----------+----------+
	| Header row, column 1   | Header 2   | Header 3 | Header 4 |
	| (header rows optional) |            |          |          |
	+========================+============+==========+==========+
	| body row 1, column 1   | column 2   | column 3 | column 4 |
	+------------------------+------------+----------+----------+
	| body row 2             | Cells may span columns.          |
	+------------------------+------------+---------------------+
	| body row 3             | Cells may  | - Table cells       |
	+------------------------+ span rows. | - contain           |
	| body row 4             |            | - body elements.    |
	+------------------------+------------+---------------------+

Result:

+------------------------+------------+----------+----------+
| Header row, column 1   | Header 2   | Header 3 | Header 4 |
| (header rows optional) |            |          |          |
+========================+============+==========+==========+
| body row 1, column 1   | column 2   | column 3 | column 4 |
+------------------------+------------+----------+----------+
| body row 2             | Cells may span columns.          |
+------------------------+------------+---------------------+
| body row 3             | Cells may  | - Table cells       |
+------------------------+ span rows. | - contain           |
| body row 4             |            | - body elements.    |
+------------------------+------------+---------------------+


2. **Simple Tables**

reStructuredText:

.. code-block:: rst

	=====  =====  =======
	  A      B    A and B
	=====  =====  =======
	False  False  False
	True   False  False
	False  True   False
	True   True   True
	=====  =====  =======

Result:

=====  =====  =======
  A      B    A and B
=====  =====  =======
False  False  False
True   False  False
False  True   False
True   True   True
=====  =====  =======

reStructuredText:

.. code-block:: rst

	=====  =====
	col 1  col 2
	=====  =====
	1      Second column of row 1.
	2      Second column of row 2.
	       Second line of paragraph.
	3      - Second column of row 3.

	       - Second item in bullet
	         list (row 3, column 2).
	\      Row 4; column 1 will be empty.
	=====  =====

Result:

=====  =====
col 1  col 2
=====  =====
1      Second column of row 1.
2      Second column of row 2.
       Second line of paragraph.
3      - Second column of row 3.

       - Second item in bullet
         list (row 3, column 2).
\      Row 4; column 1 will be empty.
=====  =====

3. **CSV Tables**


reStructuredText:

.. code-block:: rst

	.. csv-table:: Frozen Delights!
	   :header: "Treat", "Quantity", "Description"
	   :widths: 15, 10, 30

	   "Albatross", 2.99, "On a stick!"
	   "Crunchy Frog", 1.49, "If we took the bones out, it wouldn't be
	   crunchy, now would it?"
	   "Gannet Ripple", 1.99, "On a stick!"


.. csv-table:: Frozen Delights!
   :header: "Treat", "Quantity", "Description"
   :widths: 15, 10, 30

   "Albatross", 2.99, "On a stick!"
   "Crunchy Frog", 1.49, "If we took the bones out, it wouldn't be
   crunchy, now would it?"
   "Gannet Ripple", 1.99, "On a stick!"


4. **List Tables**


reStructuredText:

.. code-block:: rst

	.. list-table:: Frozen Delights!
	   :widths: 15 10 30
	   :header-rows: 1

	   * - Treat
	     - Quantity
	     - Description
	   * - Albatross
	     - 2.99
	     - On a stick!
	   * - Crunchy Frog
	     - 1.49
	     - If we took the bones out, it wouldn't be
	       crunchy, now would it?
	   * - Gannet Ripple
	     - 1.99
	     - On a stick!


.. list-table:: Frozen Delights!
   :widths: 15 10 30
   :header-rows: 1

   * - Treat
     - Quantity
     - Description
   * - Albatross
     - 2.99
     - On a stick!
   * - Crunchy Frog
     - 1.49
     - If we took the bones out, it wouldn't be
       crunchy, now would it?
   * - Gannet Ripple
     - 1.99
     - On a stick!


Images and Figures
------------------

There are two image directives: ``imag`` and ``figure``. More details can be found at: http://docutils.sourceforge.net/docs/ref/rst/directives.html#image.

1. **Simple import**

reStructuredText:

.. code-block:: rst

	.. image:: images/boxp.png

.. image:: images/boxp.png

reStructuredText:

.. code-block:: rst

	.. figure:: images/avg_rating_mon.png
	   :scale: 50 %
	   :alt: map to buried treasure

	   This is the caption of the figure (a simple paragraph).

.. figure:: images/avg_rating_mon.png
   :scale: 50 %
   :alt: map to buried treasure

   This is the caption of the figure (a simple paragraph).


2. **Complex import**

reStructuredText:

.. code-block:: rst

	.. figure:: images/boxp.png
	   :height: 400 px
	   :width: 800 px
	   :scale: 50 %
	   :alt: alternate text
	   :align: right

	   This is the caption of the figure (a simple paragraph).

	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures

	.. figure:: images/boxp.png
	   :height: 400 px
	   :width: 800 px
	   :scale: 50 %
	   :alt: alternate text
	   :align: center

	   This is the caption of the figure (a simple paragraph).

	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures


	.. figure:: images/boxp.png
	   :height: 400 px
	   :width: 800 px
	   :scale: 50 %
	   :alt: alternate text
	   :align: left

	   This is the caption of the figure (a simple paragraph).

	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
	Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures

Result:

.. figure:: images/boxp.png
   :height: 400 px
   :width: 800 px
   :scale: 50 %
   :alt: alternate text
   :align: right

   This is the caption of the figure (a simple paragraph).

Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures

.. figure:: images/boxp.png
   :height: 400 px
   :width: 800 px
   :scale: 50 %
   :alt: alternate text
   :align: center

   This is the caption of the figure (a simple paragraph).

Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures



.. figure:: images/boxp.png
   :height: 400 px
   :width: 800 px
   :scale: 50 %
   :alt: alternate text
   :align: left

   This is the caption of the figure (a simple paragraph).

Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures
Images and Figures Images and Figures Images and Figures Images and Figures Images and Figures


3. **Figures in table**

reStructuredText:

.. code-block:: rst

   +------------------------------+-----------------------+
   | Figures                      | Description           |
   +==============================+=======================+
   | .. figure:: images/corr.png  | Figure 1: test        |
   |    :scale: 20 %              |                       |
   +------------------------------+-----------------------+
   | .. image:: images/corr.png   | Figure 2: test        |
   |    :scale: 20 %              |                       |
   +------------------------------+-----------------------+
   | .. image:: images/corr.png   | Figure 3: test        |
   |    :scale: 20 %              |                       |
   +------------------------------+-----------------------+


Result:

   +------------------------------+-----------------------+
   | Figures                      | Description           |
   +==============================+=======================+
   | .. figure:: images/corr.png  | Figure 1: test        |
   |    :scale: 20 %              |                       |
   +------------------------------+-----------------------+
   | .. image:: images/corr.png   | Figure 2: test        |
   |    :scale: 20 %              |                       |
   +------------------------------+-----------------------+
   | .. image:: images/corr.png   | Figure 3: test        |
   |    :scale: 20 %              |                       |
   +------------------------------+-----------------------+

Math
----

The math role marks its content as mathematical notation (inline formula). More details can be found at: http://www.sphinx-doc.org/es/stable/ext/math.html.

The input language for mathematics is LaTeX markup. I will not do a LaTex tutorial as here. 

1. **Inline formula**

reStructuredText:

.. code-block:: rst

	The area of a circle is :math:`A_\text{c} = (\pi/4) d^2`.

RFesult:

The area of a circle is :math:`A_\text{c} = (\pi/4) d^2`.

2. **Equations**

reStructuredText:

.. code-block:: rst

	.. math::
	   :label: eq_lin_cost_func

	   \min _{\beta\in \mathbb {R} ^{p}}{\frac {1}{n}}\|{\hat {X}}\beta-{\hat {Y}}\|^{2}

    The equation :eq:`eq_lin_cost_func` is the cost function for linear regression.

Result:

.. math::
   :label: eq_cost_function

   \min _{\beta\in \mathbb {R} ^{p}}{\frac {1}{n}}\|{\hat {X}}\beta-{\hat {Y}}\|^{2}

The equation :eq:`eq_cost_function` is the cost function for linear regression.

3. **User defined symbol and equation**

Add your definitions to the ``latex_elements['preamble']`` and ``imgmath_latex_preamble``, then you can apply your own notations for symbol and equtions. 

my definitions for :math:`\B` symbol and :math:`\euler` equation: 

.. code-block:: latex

   '\\def\\B{{\\bf \\mathcal B}}\n'+ \
   '\\def\\euler{\ e^{i\pi} + 1 = 0}\n'


reStructuredText:

.. code-block:: rst


	The is a test for the user defined math symbol: :math:`\B`.

	The is a test for the user defined math equation: 

	.. math:: 

		\euler

The is a test for the user defined math symbol: :math:`\B`.

The is a test for the user defined math equation: 

.. math:: 

	\euler

4. **More examples** 

reStructuredText:

.. code-block:: rst

	.. math::

		f(x)
		=
		\Biggl \lbrace
		{
		0,\text{ if }
		   { x >0}
		\atop
		1 \text{ otherwise }
		}

	.. math::

	   (a + b)^2  &=  (a + b)(a + b) \\
	              &=  a^2 + 2ab + b^2
	              
	.. math::
	   :nowrap:

	   \begin{eqnarray}
	      y    & = & ax^2 + bx + c \nonumber\\
	      f(x) & = & x^2 + 2xy + y^2\nonumber
	   \end{eqnarray}
	   
	.. math:: e^{i\pi} + 1 = 0
	   :label: euler

Result:

.. math::

	f(x)
	=
	\Biggl \lbrace
	{
	0,\text{ if }
	   { x >0}
	\atop
	1 \text{ otherwise }
	}

.. math::

   (a + b)^2  &=  (a + b)(a + b) \\
              &=  a^2 + 2ab + b^2
              
.. math::
   :nowrap:

   \begin{eqnarray}
      y    & = & ax^2 + bx + c \nonumber\\
      f(x) & = & x^2 + 2xy + y^2\nonumber
   \end{eqnarray}
   
.. math:: e^{i\pi} + 1 = 0
   :label: euler

Source Codes
------------

1. **Source code block**

reStructuredText:

.. code-block:: rst


	.. code-block:: python

		'''
		This is a source Python code demo for Sphinx.
		@date:  Apr 25, 2016
		@author: Wenqiang Feng 
		'''
		import pandas as pd
		import numpy as np
		import matplotlib.pyplot as plt
		from pandas.tools.plotting import scatter_matrix
		from docutils.parsers.rst.directives import path


		if __name__ == '__main__':

		    print("This is a source Python code demo for Sphinx.")

Result:

.. code-block:: python

	'''
	This is a source Python code demo for Sphinx.
	@date:  Apr 25, 2016
	@author: Wenqiang Feng 
	'''
	import pandas as pd
	import numpy as np
	import matplotlib.pyplot as plt
	from pandas.tools.plotting import scatter_matrix
	from docutils.parsers.rst.directives import path


	if __name__ == '__main__':

	    print("This is a source Python code demo for Sphinx.")



reStructuredText:

.. code-block:: rst

	.. code-block:: r

		'''
		This is a source R code demo for Sphinx.
		@date:  Apr 25, 2016
		@author: Wenqiang Feng 
		'''

		library(reshape2)
		library(ggplot2)

		# import data 
		d <- melt(diamonds[,-c(2:4)])
		# plot histogram
		ggplot(d,aes(x = value)) + 
		  facet_wrap(~variable,scales = "free_x") + 
		  geom_histogram()

		print("This is a source R code demo for Sphinx.")


.. code-block:: r

	'''
	This is a source R code demo for Sphinx.
	@date:  Apr 25, 2016
	@author: Wenqiang Feng 
	'''

	library(reshape2)
	library(ggplot2)

	# import data 
	d <- melt(diamonds[,-c(2:4)])
	# plot histogram
	ggplot(d,aes(x = value)) + 
	  facet_wrap(~variable,scales = "free_x") + 
	  geom_histogram()

	print("This is a source R code demo for Sphinx.")



2. **Source code import**

* **Python Source code**

reStructuredText:

.. code-block:: rst

	.. literalinclude:: code/sourceCodePy.py
	     :language: python

Result:

.. literalinclude:: code/sourceCodePy.py
     :language: python

* **R Source code**

reStructuredText:

.. code-block:: rst

	.. literalinclude:: code/sourceCodeR.R
	     :language: r

Result:

.. literalinclude:: code/sourceCodeR.R
     :language: r

Reference
---------

1. **Paper reference**

reStructuredText:

.. code-block:: rst

	.. [Ref] Book or article reference, URL or whatever.

	Lorem ipsum [Ref]_ dolor sit amet.


Result:

.. [Ref] Book or article reference, URL or whatever.

Lorem ipsum [Ref]_ dolor sit amet.

I would refer the reader to [Sphinx2019]_ for more details.

2. **Equation reference**

reStructuredText:

.. code-block:: rst

	.. math::
	   :label: eq_condition

		f(x)
		=
		\Biggl \lbrace
		{
		0,\text{ if }
		   { x >0}
		\atop
		1 \text{ otherwise }
		}

	The Equation :eq:`eq_condition` is the definition of :math:`f(x)`.

Result:

.. math::
   :label: eq_condition

	f(x)
	=
	\Biggl \lbrace
	{
	0,\text{ if }
	   { x >0}
	\atop
	1 \text{ otherwise }
	}

The Equation :eq:`eq_condition` is the definition of :math:`f(x)`.

4. **Figure reference**

reStructuredText:

.. code-block:: rst

	.. _fig_hist_demo: 
	.. figure:: images/avg_rating_mon.png
	   :scale: 50 %
	   :alt: map to buried treasure

	   The histogram of the gouped dataset

	The Figure. :ref:`fig_hist_demo` is the histogram of the gouped dataset.


Result:

.. _fig_hist_demo: 
.. figure:: images/avg_rating_mon.png
   :scale: 50 %
   :alt: map to buried treasure

   The histogram of the gouped dataset

The Figure. :ref:`fig_hist_demo` is the histogram of the gouped dataset.


5. **Table reference**

reStructuredText:

.. code-block:: rst

	.. _table_demo: 
	.. table:: The general table demo

		+------------------------+------------+----------+----------+
		| Header row, column 1   | Header 2   | Header 3 | Header 4 |
		| (header rows optional) |            |          |          |
		+========================+============+==========+==========+
		| body row 1, column 1   | column 2   | column 3 | column 4 |
		+------------------------+------------+----------+----------+
		| body row 2             | Cells may span columns.          |
		+------------------------+------------+---------------------+
		| body row 3             | Cells may  | - Table cells       |
		+------------------------+ span rows. | - contain           |
		| body row 4             |            | - body elements.    |
		+------------------------+------------+---------------------+

	Please see the above Table. :ref:`table_demo`.



Result:

.. _table_demo: 
.. table:: The general table demo

	+------------------------+------------+----------+----------+
	| Header row, column 1   | Header 2   | Header 3 | Header 4 |
	| (header rows optional) |            |          |          |
	+========================+============+==========+==========+
	| body row 1, column 1   | column 2   | column 3 | column 4 |
	+------------------------+------------+----------+----------+
	| body row 2             | Cells may span columns.          |
	+------------------------+------------+---------------------+
	| body row 3             | Cells may  | - Table cells       |
	+------------------------+ span rows. | - contain           |
	| body row 4             |            | - body elements.    |
	+------------------------+------------+---------------------+

Please see the above Table. :ref:`table_demo`.


6. **Footnotes**

reStructuredText:

.. code-block:: rst

	Lorem ipsum [#f1]_ dolor sit amet ... [#f2]_

	.. rubric:: Footnotes

	.. [#f1] Text of the first footnote.
	.. [#f2] Text of the second footnote.

Result:

Lorem ipsum [#f1]_ dolor sit amet ... [#f2]_

.. rubric:: Footnotes

.. [#f1] Text of the first footnote.
.. [#f2] Text of the second footnote.

7. **Hyperlinks**

* General hyperlink

reStructuredText:

.. code-block:: rst

	You are more than welcome to visit my personal webpage: `Feng Website`_.

	.. _Feng Website: http://web.utk.edu/~wfeng1/

Result:

You are more than welcome to visit my personal webpage: `Feng Website`_.

.. _Feng Website: http://web.utk.edu/~wfeng1/

* Embeded Youtube link:

reStructuredText:

.. code-block:: rst

	.. raw:: html

	    <iframe width="700" height="315" 
	    src="https://www.youtube.com/embed/mrEee4bhc7Y" 
	    frameborder="0" allowfullscreen></iframe>

Result:

.. raw:: html

    <iframe width="700" height="315" 
    src="https://www.youtube.com/embed/mrEee4bhc7Y" 
    frameborder="0" allowfullscreen></iframe>

.. warning::

	You have to use the hyperlink: ``https://www.youtube.com/embed/`` + ``name``. 





Roles
+++++

A role or “custom interpreted text role” is an inline piece of explicit markup. It signifies that that the enclosed text should be interpreted in a specific way. Sphinx uses this to provide semantic markup and cross-referencing of identifiers, as described in the appropriate section. More details can be found at: http://docutils.sourceforge.net/docs/ref/rst/roles.html#customization


Standard Roles
--------------

* **Line markup**

reStructuredText:

.. code-block:: rst

	* emphasis – equivalent of *emphasis*

	* strong – equivalent of **strong**

	* literal – equivalent of ``literal``

	* subscript – H\ :sub:`2`\ O

	* superscript – E = mc\ :sup:`2`

	* title-reference – for titles of books, periodicals, and other materials

Result:

* emphasis – equivalent of *emphasis*

* strong – equivalent of **strong**

* literal – equivalent of ``literal``

* subscript – H\ :sub:`2`\ O

* superscript – E = mc\ :sup:`2`

* title-reference – for titles of books, periodicals, and other materials


Specialized Roles
-----------------

* **raw**

reStructuredText:

.. code-block:: rst

	.. raw:: html

	    <iframe width="700" height="315" 
	    src="https://www.youtube.com/embed/2Mg8QD0F1dQ" 
	    frameborder="0" allowfullscreen></iframe>

Result:

.. raw:: html

    <iframe width="700" height="315" 
    src="https://www.youtube.com/embed/2Mg8QD0F1dQ" 
    frameborder="0" allowfullscreen></iframe>

reStructuredText:

.. code-block:: rst

	.. role:: raw-html(raw)
	   :format: html

	If there just *has* to be a line break here,
	:raw-html:`<br />`
	it can be accomplished with a "raw"-derived role.
	But the line block syntax should be considered first.

Result:

.. role:: raw-html(raw)
   :format: html

If there just *has* to be a line break here,
:raw-html:`<br />`
it can be accomplished with a "raw"-derived role.
But the line block syntax should be considered first.

* **replace**

reStructuredText:

.. code-block:: rst

	.. |sphx| replace:: Sphinx 
	.. |reST| replace:: reStructuredText

	|reST| is awesome!

.. |sphx| replace:: Sphinx 
.. |reST| replace:: reStructuredText

|sphx| and |reST| are awesome!



Directives
++++++++++

A directive is a generic block of explicit markup. Along with roles, it is one of the extension mechanisms of reST, and Sphinx makes heavy use of it.

Admonitions
-----------

Admonitions: ``attention``, ``caution``, ``danger``, ``error``, ``hint``, ``important``, ``note``, ``tip``, ``warning``

* **attention**

reStructuredText:

.. code-block:: rst

	.. attention::

	   You neen to pay attention at here!

Result:

.. attention::

   You neen to pay attention at here!

* **caution**

reStructuredText:

.. code-block:: rst

	.. caution::

	   This is a caution alert!

Restlut:

.. caution::

	This is a caution alert!

* **important**

reStructuredText:

.. code-block:: rst

	.. important:: 

		This is important!

Result:

.. important:: 

	This is important!

*  **User defined admonition**

reStructuredText:

.. code-block:: rst

	.. admonition:: User defined name

	   You can make up your own admonition too.

Result:

.. admonition:: User defined name

   You can make up your own admonition too.

* **seealso**

reStructuredText:

.. code-block:: rst

	.. seealso::

	   The authoritative `reStructuredText User Documentation
	   <http://docutils.sourceforge.net/rst.html>`_.  The "ref" links in this
	   document link to the description of the individual constructs in the reST
	   reference.

Result:

.. seealso::

   The authoritative `reStructuredText User Documentation
   <http://docutils.sourceforge.net/rst.html>`_.  The "ref" links in this
   document link to the description of the individual constructs in the reST
   reference.


See more details at `Admonitions`_.


Hiddencode
----------

reference: https://sphinxcontrib-contentui.readthedocs.io/en/latest/index.html

reStructuredText:

.. code-block:: rst

	.. toggle-header::
	    :header: Example 1 **Show/Hide Code**

	    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
	    incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
	    nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
	    Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
	    fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
	    culpa qui officia deserunt mollit anim id est laborum


.. toggle-header::
    :header: Example 1 **Show/Hide Code**

    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
    incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
    nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
    Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
    fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
    culpa qui officia deserunt mollit anim id est laborum


Options
-------

reStructuredText:

.. code-block:: rst

	.. content-tabs:: 

	    .. tab-container:: ex1
	        :title: Example 1

	        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
	        incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
	        nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
	        Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
	        fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
	        culpa qui officia deserunt mollit anim id est laborum

	    .. tab-container:: ex2
	        :title: Example 2

	        Sed ut perspiciatis, unde omnis iste natus error sit voluptatem
	        accusantium doloremque laudantium, totam rem aperiam eaque ipsa, quae
	        ab illo inventore veritatis et quasi architecto beatae vitae dicta
	        sunt, explicabo. Nemo enim ipsam voluptatem, quia voluptas sit,
	        aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos,
	        qui ratione voluptatem sequi nesciunt, neque porro quisquam est, qui
	        dolorem ipsum, quia dolor sit, amet, consectetur, adipisci velit, sed
	        quia non numquam eius modi tempora incidunt, ut labore et dolore magnam
	        aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum
	        exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex
	        ea commodi consequatur? Quis autem vel eum iure reprehenderit, qui in
	        ea voluptate velit esse, quam nihil molestiae consequatur, vel illum,
	        qui dolorem eum fugiat, quo voluptas nulla pariatur? At vero eos et
	        accusamus et iusto odio dignissimos ducimus, qui blanditiis praesentium
	        voluptatum deleniti atque corrupti, quos dolores et quas molestias
	        excepturi sint, obcaecati cupiditate non provident, similique sunt in
	        culpa, qui officia deserunt mollitia animi, id est laborum et dolorum
	        fuga. Et harum quidem rerum facilis est et expedita distinctio. Nam
	        libero tempore, cum soluta nobis est eligendi optio, cumque nihil
	        impedit, quo minus id, quod maxime placeat, facere possimus, omnis
	        voluptas assumenda est, omnis dolor repellendus. Temporibus autem
	        quibusdam et aut officiis debitis aut rerum necessitatibus saepe
	        eveniet, ut et voluptates repudiandae sint et molestiae non recusandae.
	        Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis
	        voluptatibus maiores alias consequatur aut perferendis doloribus
	        asperiores repellat.


.. content-tabs:: 

    .. tab-container:: ex1
        :title: Example 1

        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
        incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
        nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
        fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
        culpa qui officia deserunt mollit anim id est laborum

    .. tab-container:: ex2
        :title: Example 2

        Sed ut perspiciatis, unde omnis iste natus error sit voluptatem
        accusantium doloremque laudantium, totam rem aperiam eaque ipsa, quae
        ab illo inventore veritatis et quasi architecto beatae vitae dicta
        sunt, explicabo. Nemo enim ipsam voluptatem, quia voluptas sit,
        aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos,
        qui ratione voluptatem sequi nesciunt, neque porro quisquam est, qui
        dolorem ipsum, quia dolor sit, amet, consectetur, adipisci velit, sed
        quia non numquam eius modi tempora incidunt, ut labore et dolore magnam
        aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum
        exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex
        ea commodi consequatur? Quis autem vel eum iure reprehenderit, qui in
        ea voluptate velit esse, quam nihil molestiae consequatur, vel illum,
        qui dolorem eum fugiat, quo voluptas nulla pariatur? At vero eos et
        accusamus et iusto odio dignissimos ducimus, qui blanditiis praesentium
        voluptatum deleniti atque corrupti, quos dolores et quas molestias
        excepturi sint, obcaecati cupiditate non provident, similique sunt in
        culpa, qui officia deserunt mollitia animi, id est laborum et dolorum
        fuga. Et harum quidem rerum facilis est et expedita distinctio. Nam
        libero tempore, cum soluta nobis est eligendi optio, cumque nihil
        impedit, quo minus id, quod maxime placeat, facere possimus, omnis
        voluptas assumenda est, omnis dolor repellendus. Temporibus autem
        quibusdam et aut officiis debitis aut rerum necessitatibus saepe
        eveniet, ut et voluptates repudiandae sint et molestiae non recusandae.
        Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis
        voluptatibus maiores alias consequatur aut perferendis doloribus
        asperiores repellat.



reStructuredText:

.. code-block:: rst

	.. content-tabs:: 


	    .. tab-container:: python
	        :title: Python

	        .. rubric:: Description for Python

	    .. tab-container:: php
	        :title: PHP

	        .. rubric:: Description for PHP

.. content-tabs:: 


    .. tab-container:: python
        :title: Python

        .. rubric:: Description for Python

    .. tab-container:: php
        :title: PHP

        .. rubric:: Description for PHP

reStructuredText:

.. code-block:: rst

	.. container:: content-tabs right-col

	    .. tab-container:: python
	        :title: Python

	        .. rubric:: import library

	        .. code-block:: python

	            import xgboost as xgb

	        .. rubric:: Example request

	        .. code-block:: python

	            bst = xgb.train(param, dtrain, num_round, evallist)

	    .. tab-container:: r
	        :title: r

	        .. rubric:: import library

	        .. code-block:: r

	            require(xgboost)

	        .. rubric:: Example request

	        .. code-block:: r 

	            bstSparse <- xgboost(data = train$data, label = train$label, max.depth = 2, eta = 1)


.. container:: content-tabs right-col

    .. tab-container:: python
        :title: Python

        .. rubric:: Import library

        .. code-block:: python

            import xgboost as xgb

        .. rubric:: Train model

        .. code-block:: python

            bst = xgb.train(param, dtrain, num_round, evallist)

    .. tab-container:: r
        :title: r

        .. rubric:: Import library

        .. code-block:: r

            require(xgboost)

        .. rubric:: Train model 

        .. code-block:: r 

            bstSparse <- xgboost(data = train$data, label = train$label, max.depth = 2, eta = 1)

.. _Admonitions: http://docutils.sourceforge.net/docs/ref/rst/directives.html#admonitions

