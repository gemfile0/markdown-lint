---
title: MD030 - Spaces after list markers
tags:  [ol, ul, whitespace]
alias: list-marker-space
---

Parameters: ul_single, ol_single, ul_multi, ol_multi (number, default 1)

This rule checks for the number of spaces between a list marker (e.g. '`-`',
'`*`', '`+`' or '`1.`') and the text of the list item.

The number of spaces checked for depends on the document style in use, but the
default is 1 space after any list marker:

    * Foo
    * Bar
    * Baz

    1. Foo
    1. Bar
    1. Baz

    1. Foo
       * Bar
    1. Baz

A document style may change the number of spaces after unordered list items
and ordered list items independently, as well as based on whether the content
of every item in the list consists of a single paragraph, or multiple
paragraphs (including sub-lists and code blocks).

For example, the style guide at
<http://www.cirosantilli.com/markdown-styleguide/#spaces-after-marker>
specifies that 1 space after the list marker should be used if every item in
the list fits within a single paragraph, but to use 2 or 3 spaces (for ordered
and unordered lists respectively) if there are multiple paragraphs of content
inside the list:

    * Foo
    * Bar
    * Baz

    vs.

    *   Foo

        Second paragraph

    *   Bar

    or

    1.  Foo

        Second paragraph

    1.  Bar

To fix this, ensure the correct number of spaces are used after list marker
for your selected document style.
