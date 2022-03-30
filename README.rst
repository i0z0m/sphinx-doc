=====================================
make Bitbucket pages docs with Sphinx
=====================================

usage
=======

.. code:: sh

   $ pip install --user sphinx ghp-import

pipでインストールしたsphinxコマンドのパスを通すために

.. code:: sh

   $ vim .zshenv
   export PATH=$PATH:~/.local/bin

.. code:: sh

  $ sphinx-quickstart
  $ make html

change theme
============

.. code:: sh

  $ pip install --user sphinx_rtd_theme

edit source/conf.py

.. code:: sh

  html_theme = 'sphinx_rtd_theme'
  favicon = 'favicon.ico'
  pygments = 'monokai'

hosting to bitbucket pages
==========================

.. code:: sh

  $ git init
  $ git add *
  $ git commit -m "first commit"
  $ git remote add origin git@bitbucket.org:i0z0m/i0z0m.bitbucket.io.git
  $ ghp-import -m "○○の記事を更新" build/html
  $ git push origin gh-pages:master
