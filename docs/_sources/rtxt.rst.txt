.. _rtext:

=======================
reStructuredText Markup
=======================

.. admonition:: Chinese proverb

	Making full preparation will not delay your job but quicken the process. – old Chinese proverb


Sections
++++++++

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
++++++++++

The paragraph is the most basic block in a reST document. 
Paragraphs are simply chunks of text separated by one or 
more blank lines. As in Python, indentation is significant 
in reST, so all lines of the same paragraph must be 
left-aligned to the **same level of indentation**. More 
details can be found at: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#paragraphs

General Paragraphs
------------------

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

Bullet Lists Paragraphs
-----------------------

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


Bullet Lists Paragraphs
-----------------------

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

Blocked Paragraphs
------------------

1. **Line Blocks**

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

2. **Doctest Blocks**

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
+++++

More details can be found at: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#grid-tables

Grid Tables
-----------

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


Simple Tables
-------------

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

CSV Tables
----------

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


List Tables
-----------

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


Directives
++++++++++

Admonitions
-----------

#. attention
#. caution
#. danger
#. error
#. hint
#. important
#. note
#. tip
#. warning

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

