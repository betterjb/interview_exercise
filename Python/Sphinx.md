##  Sphinx

- 테스트 환경
	+ Window 7 
	+ Python 3.6.0
	+ Django 1.10.5
	+ Pycharm -> Tool -> Sphinx Quickstart

- Linux의 경우 
	$ pip install Sphinx
	$ sphinx-quickstart

- Sphinx Quickstart
	Welcome to the Sphinx 1.6.6 quickstart utility.
	Please enter values for the following settings (just press Enter to
	accept a default value, if one is given in brackets).

	Enter the root path for documentation.
	> Root path for the documentation [.]: docs/
	위와 같이 물어봅니다. root 경로 설정입니다. 기본은 현재 폴더입니다.

	You have two options for placing the build directory for Sphinx output.
	Either, you use a directory "_build" within the root path, or you separate
	"source" and "build" directories within the root path.
	> Separate source and build directories (y/n) [n]: 
	Inside the root directory, two more directories will be created; "_templates"
	for custom HTML templates and "_static" for custom stylesheets and other static
	files. You can enter another prefix (such as ".") to replace the underscore.
	> Name prefix for templates and static dir [_]:
	The project name will occur in several places in the built documentation.
	> Project name: my_package
	> Author name(s): kei
	Sphinx has the notion of a "version" and a "release" for the
	software. Each version can have multiple releases. For example, for
	Python the version is something like 2.5 or 3.0, while the release is
	something like 2.5.1 or 3.0a1.  If you don't need this dual structure,
	just set both to the same value.
	> Project version []: 1.0
	> Project release [1.0]:
	문서 버전과 릴리즈 버전 정보 입력.

	If the documents are to be written in a language other than English,
	you can select a language here by its language code. Sphinx will then
	translate text that it generates into that language.

	For a list of supported codes, see
	http://sphinx-doc.org/config.html#confval-language.
	> Project language [en]:
	문서의 언어지원 입력. 기본은 영어.

	한국어를 원할 경우 ko를 입력한다.

	그러나 여기서는 테스트니까 default값으로 하자.

	The file name suffix for source files. Commonly, this is either ".txt"
	or ".rst".  Only files with this suffix are considered documents.
	> Source file suffix [.rst]:
	파일 포멧 설정 기본 rst확장자를 사용.

	One document is special in that it is considered the top node of the
	"contents tree", that is, it is the root of the hierarchical structure
	of the documents. Normally, this is "index", but if your "index"
	document is a custom template, you can also set this to another filename.
	> Name of your master document (without suffix) [index]:
	Sphinx can also add configuration for epub output:
	> Do you want to use the epub builder (y/n) [n]:
	Please indicate if you want to use one of the following Sphinx extensions:
	> autodoc: automatically insert docstrings from modules (y/n) [n]: y
	> doctest: automatically test code snippets in doctest blocks (y/n) [n]:
	> intersphinx: link between Sphinx documentation of different projects (y/n) [n]: y
	> todo: write "todo" entries that can be shown or hidden on build (y/n) [n]: y
	> coverage: checks for documentation coverage (y/n) [n]:
	> imgmath: include math, rendered as PNG or SVG images (y/n) [n]:
	> mathjax: include math, rendered in the browser by MathJax (y/n) [n]:
	> ifconfig: conditional inclusion of content based on config values (y/n) [n]:
	> viewcode: include links to the source code of documented Python objects (y/n) [n]:
	> githubpages: create .nojekyll file to publish the document on GitHub pages (y/n) [n]:
	A Makefile and a Windows command file can be generated for you so that you
	only have to run e.g. `make html' instead of invoking sphinx-build
	directly.
	> Create Makefile? (y/n) [y]:
	> Create Windows command file? (y/n) [y]:

	Creating file docs/conf.py.
	Creating file docs/index.rst.
	Creating file docs/Makefile.
	Creating file docs/make.bat.

	Finished: An initial directory structure has been created.

	You should now populate your master file docs/index.rst and create other documentation
	source files. Use the Makefile to build the docs, like so:
	   make builder
	where "builder" is one of the supported builders, e.g. html, latex or linkcheck.
	초기설정 완료.

