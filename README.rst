txt2mm
================

A simple text to freeplane conversion program


Overview
========

This program converts tab-indented UTF-8 text files into an XML format suitable
for display by FreePlane. It was written out of annoyance with the FreePlane user
interface, and the lack of 'merging' capabilities when collaborating with other
people.

Copyright  2006–2017  Wouter Bolsterlee <uws@xs4all.nl>
Copyright  2025       Richard Holbert <rholbert@gmail.com>

This revised program is distributed under the Apache license.


Usage
=====

To convert a single text file into a FreePlane file, use::

    $ txt2mm input-file.txt > output-file.mm

You can use it as a filter (using shell pipes) as well::

    $ cat some-text-data.txt | txt2mm > output-file.mm

A Makefile snippet is also included to convert all ``*.mm.txt`` files into their
``*.mm`` counterparts. First copy or symlink the makefile, than run make::

    $ cp /path/to/txt2mm/txt2mm.make Makefile
    $ make

Alternatively::

  $ ln -s /path/to/txt2mm/txt2mm.make Makefile
  $ make

Or execute the makefile directly if you don't want to copy files around::

  $ /path/to/txt2mm/txt2mm.make


Requirements
============

The conversion program is written in Python (tested with 3.10 and 3.12) and
requires an ElementTree implementation. Install python-elementtree or
python-celementtree (included in Python 3) if you run into programs.

The Makefile snippet obviously depends on the make utility. GNU/Make is known
to work.


Issues, problems, and feedback
==============================

This program is a quick hack, so don't expect too much of it. If you feel like
contacting me with problems or suggestions, please mail me. Thanks.

