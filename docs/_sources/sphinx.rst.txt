.. _sphinx:

=====================
Sphinx Configuration
=====================

.. warning::

	I heavily borrowed, modified and used the configuration in ``conf.py`` and ``docgen.py`` of `Theano package project`_. I will keep all the comments from Theano team and the coryrights of those files belong to Theano team. 


General HTML Configuration
++++++++++++++++++++++++++

General Evironment Infomation
-----------------------------

1. Sphinx extension

.. code-block:: python

	# Add any Sphinx extension module names here, as strings. They can be
	# extensions coming with Sphinx (named 'sphinx.ext.*') or your custom ones.
	extensions = ['sphinx.ext.autodoc',
	              'sphinx.ext.todo',
	              'sphinx.ext.doctest',
	              'sphinx.ext.napoleon',
	              'sphinx.ext.linkcode']

	todo_include_todos = True
	napoleon_google_docstring = False
	napoleon_include_special_with_doc = False

2. Math formula support 

.. code-block:: python

	# We do it like this to support multiple sphinx version without having warning.
	# Our buildbot consider warning as error.
	try:
	    from sphinx.ext import imgmath
	    extensions.append('sphinx.ext.imgmath')
	except ImportError:
	    try:
	        from sphinx.ext import pngmath
	        extensions.append('sphinx.ext.pngmath')
	    except ImportError:
	        pass

3. Included and excluded folders options 

.. code-block:: python

	# Add any paths that contain templates here, relative to this directory.
	templates_path = ['.templates']

	# List of directories, relative to source directories, that shouldn't be
	# searched for source files.
	exclude_dirs = ['images', 'scripts', 'sandbox']

4. Image math formula preamble

.. code-block:: python

	# If false, no module index is generated.
	#latex_use_modindex = True

	default_role = 'math'
	pngmath_divpng_args = ['-gamma 1.5','-D 110']
	#pngmath_divpng_args = ['-gamma', '1.5', '-D', '110', '-bg', 'Transparent'] 
	imgmath_latex_preamble =  '\\usepackage{amsmath}\n'+\
	                          '\\usepackage{mathtools}\n'+\
	                          '\\usepackage{amsfonts}\n'+\
	                          '\\usepackage{amssymb}\n'+\
	                          '\\usepackage{dsfont}\n'+\
	                          '\\def\\Z{\\mathbb{Z}}\n'+\
	                          '\\def\\R{\\mathbb{R}}\n'+\
	                          '\\def\\bX{\\mathbf{X}}\n'+\
	                          '\\def\\X{\\mathbf{X}}\n'+\
	                          '\\def\\By{\\mathbf{y}}\n'+\
	                          '\\def\\Bbeta{\\boldsymbol{\\beta}}\n'+\
	                          '\\def\\U{\\mathbf{U}}\n'+\
	                          '\\def\\V{\\mathbf{V}}\n'+\
	                          '\\def\\V1{\\mathds{1}}\n'+\
	                          '\\def\\hU{\\mathbf{\hat{U}}}\n'+\
	                          '\\def\\hS{\\mathbf{\hat{\Sigma}}}\n'+\
	                          '\\def\\hV{\\mathbf{\hat{V}}}\n'+\
	                          '\\def\\E{\\mathbf{E}}\n'+\
	                          '\\def\\F{\\mathbf{F}}\n'+\
	                          '\\def\\x{\\mathbf{x}}\n'+\
	                          '\\def\\h{\\mathbf{h}}\n'+\
	                          '\\def\\v{\\mathbf{v}}\n'+\
	                          '\\def\\nv{\\mathbf{v^{{\bf -}}}}\n'+\
	                          '\\def\\nh{\\mathbf{h^{{\bf -}}}}\n'+\
	                          '\\def\\s{\\mathbf{s}}\n'+\
	                          '\\def\\b{\\mathbf{b}}\n'+\
	                          '\\def\\c{\\mathbf{c}}\n'+\
	                          '\\def\\W{\\mathbf{W}}\n'+\
	                          '\\def\\C{\\mathbf{C}}\n'+\
	                          '\\def\\P{\\mathbf{P}}\n'+\
	                          '\\def\\T{{\\bf \\mathcal T}}\n'+\
	                          '\\def\\B{{\\bf \\mathcal B}}\n'


General Project Infomation
--------------------------

1. The suffix of source filenames

.. code-block:: python

	# The suffix of source filenames.
	source_suffix = '.rst'

2. The master toctree document

.. code-block:: python

	# The master toctree document.
	master_doc = 'index'

3. General substitutions

.. code-block:: python

	# General substitutions.
	project = 'Sphinx with Github Webpages'
	copyright = '2019, Wenqiang Feng'

4. Version and date format

.. code-block:: python

	# We need this hokey-pokey because versioneer needs the current
	# directory to be the root of the project to work.
	# The short X.Y version.
	version = '1.00'
	# The full version, including alpha/beta/rc tags.
	release = '1.00'

	# There are two options for replacing |today|: either, you set today to some
	# non-false value, then it is used:
	#today = ''
	# Else, today_fmt is used as the format for a strftime call.
	today_fmt = '%B %d, %Y'

	# Add any paths that contain custom static files (such as style sheets) here,
	# relative to this directory. They are copied after the builtin static files,
	# so a file named "default.css" will overwrite the builtin "default.css".
	html_static_path = ['images']

	# If not '', a 'Last updated on:' timestamp is inserted at every page bottom,
	# using the given strftime format.
	html_last_updated_fmt = '%b %d, %Y'

	# If true, SmartyPants will be used to convert quotes and dashes to
	# typographically correct entities.
	html_use_smartypants = True

General LaTex Configuration
+++++++++++++++++++++++++++

General LaTeX Output Options
----------------------------

.. code-block:: python

	# Options for LaTeX output
	# ------------------------

	latex_elements = {
	    # The paper size ('letter' or 'a4').
	    #latex_paper_size = 'a4',

	    # The font size ('10pt', '11pt' or '12pt').
	    'pointsize': '12pt',

	    # Additional stuff for the LaTeX preamble.
	    #latex_preamble = '',
	}

	# Grouping the document tree into LaTeX files. List of tuples
	# (source start file, target name, title, author, document class
	# [howto/manual]).
	latex_documents = [
	  ('index', 'sphinxgithub.tex', 'Sphinx Github Webpage Tutorials',
	   'Wenqiang Feng', 'manual'),
	]
	# The name of an image file (relative to this directory) to place at the top of
	# the title page.
	latex_logo = 'images/logo.png'

LaTeX preamble definitions
--------------------------

.. code-block:: python

	#latex_elements['preamble'] = '\usepackage{xcolor}'
	# Additional stuff for the LaTeX preamble.
	#latex_preamble 
	latex_elements['preamble'] =  '\\usepackage{amsmath}\n'+\
	                          '\\usepackage{mathtools}\n'+\
	                          '\\usepackage{amsfonts}\n'+\
	                          '\\usepackage{amssymb}\n'+\
	                          '\\usepackage{dsfont}\n'+\
	                          '\\def\\Z{\\mathbb{Z}}\n'+\
	                          '\\def\\R{\\mathbb{R}}\n'+\
	                          '\\def\\bX{\\mathbf{X}}\n'+\
	                          '\\def\\X{\\mathbf{X}}\n'+\
	                          '\\def\\By{\\mathbf{y}}\n'+\
	                          '\\def\\Bbeta{\\boldsymbol{\\beta}}\n'+\
	                          '\\def\\bU{\\mathbf{U}}\n'+\
	                          '\\def\\bV{\\mathbf{V}}\n'+\
	                          '\\def\\V1{\\mathds{1}}\n'+\
	                          '\\def\\hU{\\mathbf{\hat{U}}}\n'+\
	                          '\\def\\hS{\\mathbf{\hat{\Sigma}}}\n'+\
	                          '\\def\\hV{\\mathbf{\hat{V}}}\n'+\
	                          '\\def\\E{\\mathbf{E}}\n'+\
	                          '\\def\\F{\\mathbf{F}}\n'+\
	                          '\\def\\x{\\mathbf{x}}\n'+\
	                          '\\def\\h{\\mathbf{h}}\n'+\
	                          '\\def\\v{\\mathbf{v}}\n'+\
	                          '\\def\\nv{\\mathbf{v^{{\bf -}}}}\n'+\
	                          '\\def\\nh{\\mathbf{h^{{\bf -}}}}\n'+\
	                          '\\def\\s{\\mathbf{s}}\n'+\
	                          '\\def\\b{\\mathbf{b}}\n'+\
	                          '\\def\\c{\\mathbf{c}}\n'+\
	                          '\\def\\W{\\mathbf{W}}\n'+\
	                          '\\def\\C{\\mathbf{C}}\n'+\
	                          '\\def\\P{\\mathbf{P}}\n'+\
	                          '\\def\\T{{\\bf \\mathcal T}}\n'+\
	                          '\\def\\B{{\\bf \\mathcal B}}\n'

Full ``conf.py`` Script
+++++++++++++++++++++++

.. literalinclude:: conf.py
     :language: python

General Documentation Generator Configuration
+++++++++++++++++++++++++++++++++++++++++++++

Output Options
--------------

.. code-block:: python

   throot = os.path.abspath(
        os.path.join(sys.path[0], os.pardir, os.pardir))

    options = defaultdict(bool)
    opts, args = getopt.getopt(
        sys.argv[1:],
        'o:f:',
        ['rst', 'help', 'nopdf', 'cache', 'check', 'test'])
    options.update(dict([x, y or True] for x, y in opts))
    if options['--help']:
        print('Usage: %s [OPTIONS] [files...]' % sys.argv[0])
        print('  -o <dir>: output the html files in the specified dir')
        print('  --cache: use the doctree cache')
        print('  --rst: only compile the doc (requires sphinx)')
        print('  --nopdf: do not produce a PDF file from the doc, only HTML')
        print('  --test: run all the code samples in the documentaton')
        print('  --check: treat warnings as errors')
        print('  --help: this help')
        print('If one or more files are specified after the options then only '
              'those files will be built. Otherwise the whole tree is '
              'processed. Specifying files will implies --cache.')
        sys.exit(0)

    if not(options['--rst'] or options['--test']):
        # Default is now rst
        options['--rst'] = True


Output Directory
----------------

.. code-block:: python

    def mkdir(path):
        try:
            os.mkdir(path)
        except OSError:
            pass

    # create the putput folder docs, since github page will use /docs folder for Github page.
    outdir = options['-o'] or (throot + '/docs')
    # create the output folder latex
    latexdir = options['-o'] or (throot + '/latex')

    files = None
    if len(args) != 0:
        files = [os.path.abspath(f) for f in args]
    currentdir = os.getcwd()
    mkdir(outdir)
    mkdir(latexdir)
    os.chdir(outdir)

.. code-block:: python


Documentation Compiler
----------------------

.. code-block:: python

   def call_sphinx(builder, workdir):
        import sphinx
        if options['--check']:
            extraopts = ['-W']
        else:
            extraopts = []
        if not options['--cache'] and files is None:
            extraopts.append('-E')
        docpath = os.path.join(throot, 'doc')
        inopt = [docpath, workdir]
        if files is not None:
            inopt.extend(files)
        ret = sphinx.build_main(['', '-b', builder] + extraopts + inopt)
        if ret != 0:
            sys.exit(ret)

    if options['--all'] or options['--rst']:
        mkdir("doc")
        sys.path[0:0] = [os.path.join(throot, 'doc')]
        call_sphinx('html', '.')

        if not options['--nopdf']:
            # Generate latex file in a temp directory
            import tempfile
            #workdir = tempfile.mkdtemp()
            workdir = latexdir
            call_sphinx('latex', workdir)
            # Compile to PDF
            os.chdir(workdir)
            os.system('make')
            try:
                shutil.copy(os.path.join(workdir, 'sphinxgithub.pdf'), outdir)
                os.chdir(outdir)
                # remove the workdir folder
                #shutil.rmtree(workdir)
            except OSError as e:
                print('OSError:', e)
            except IOError as e:
                print('IOError:', e)

    if options['--test']:
        mkdir("doc")
        sys.path[0:0] = [os.path.join(throot, 'doc')]
        call_sphinx('doctest', '.')

    # To go back to the original current directory.
    os.chdir(currentdir)

    # Reset THEANO_FLAGS
    # os.environ['THEANO_FLAGS'] = env_th_flags

``Makefile`` Wrapper
--------------------

.. code-block:: python

	all:
		python scripts/docgen.py


Full ``docgen.py`` Script
+++++++++++++++++++++++++


.. literalinclude:: scripts/docgen.py
     :language: python

.. _Theano package project: https://github.com/Theano/Theano
