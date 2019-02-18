.. _rtext:

=======================
reStructuredText Markup
=======================

.. admonition:: Chinese proverb

	Making full preparation will not delay your job but quicken the process. – old Chinese proverb


reStructuredText Primer
+++++++++++++++++++++++

I would refer the reader to [Sphinx2019]_ for more details.

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

Roles
+++++

A role or “custom interpreted text role” is an inline piece of explicit markup. It signifies that that the enclosed text should be interpreted in a specific way. Sphinx uses this to provide semantic markup and cross-referencing of identifiers, as described in the appropriate section. More details can be found at: http://docutils.sourceforge.net/docs/ref/rst/roles.html#customization


Standard Roles
--------------

* **Line markup**

reStructuredText:

.. code-block:: rst

	emphasis – equivalent of *emphasis*

	strong – equivalent of **strong**

	literal – equivalent of ``literal``

	subscript – H\ :sub:`2`\ O

	superscript – E = mc\ :sup:`2`

	title-reference – for titles of books, periodicals, and other materials


emphasis – equivalent of *emphasis*

strong – equivalent of **strong**

literal – equivalent of ``literal``

subscript – H\ :sub:`2`\ O

superscript – E = mc\ :sup:`2`

title-reference – for titles of books, periodicals, and other materials



reStructuredText:

.. code-block:: rst



Result:	



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

Lorem ipsum [#f1]_ dolor sit amet ... [#f2]_


Lorem ipsum [Ref]_ dolor sit amet.

.. rubric:: Footnotes

.. [#f1] Text of the first footnote.
.. [#f2] Text of the second footnote.

.. [Ref] Book or article reference, URL or whatever.





.. _Admonitions: http://docutils.sourceforge.net/docs/ref/rst/directives.html#admonitions

