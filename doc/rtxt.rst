.. _rtext:

=======================
reStructuredText Markup
=======================

.. admonition:: Chinese proverb

	Making full preparation will not delay your job but quicken the process. – old Chinese proverb


TODO ......

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

* **caution**

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

