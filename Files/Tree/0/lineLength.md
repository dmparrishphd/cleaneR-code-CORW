Line Length
===========

Should there be a limit to the number of characters on a line? Consider:

    # Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Applying the 64-character limit to _Lorem ipsum_ results in:---

    # Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
    # do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    # Ut enim ad minim veniam, quis nostrud exercitation ullamco
    # laboris nisi ut aliquip ex ea commodo consequat. Duis aute
    # irure dolor in reprehenderit in voluptate velit esse cillum
    # dolore eu fugiat nulla pariatur. Excepteur sint occaecat
    # cupidatat non proident, sunt in culpa qui officia deserunt
    # mollit anim id est laborum.

The greater the line length,
the greater the risk that text will either wrap or run off the
edge of the display (monitor, smart phone display, paper).

One reason high-level languages, like R, were invented was so
that the programmer could read the code long after writing it
and be able to understand it.
But if the code is not even _visible_, there is little
opportunity to understand.
And if the code wraps, it will likely be more difficult to
interperet by the human reader, especially if leading
whitespace is assigned meaning (as in Python).

Typesetters have long known that the number of characters per
line impacts the speed with which the reader is able to
comprehend the writing.
The critical number seems to be about 66 characters.
As lines extend beyond about 66 characters, text is becomes
more and more difficult to comprehend.

Consider what your code would look like if someone were
to print it on A4 (8.268 inches wide) or letter-size paper
(8.5 inches wide)
If pica pitch is used, there is room for at most 82 or 85
characters.
If elite pitch is used, the is room for at most 99 or 102
characters.
Include reasonable margins, and the line width is limited
to about 62, 65, 75, or 78 characters.

Some text editors have special tools to enable you to control line
length.
Using even the most rudimentary editor, you can create a ruler
using ordinary characters:---

    #        1         2         3         4         5         6         7         8
    #234567890123456789012345678901234567890123456789012345678901234-----0--///////0

I recommend 64 characters as a soft line length limit, and
80 characters as a hard limit.
But consider 78 or 79 characters as a hard limit, since some
terminals will create a new line after writing the 80th
character, which can create a false double-space effect.

Use the characters between the soft and hard limits sparingly,
mainly for punctuation (e.g., a closing bracket).

Line Length in Markdown Flavors
-------------------------------

### Jupyter Notebooks

Try wrapping an entire Markdown cell in

    <div style="max-width:33em"> <!-- first line of Jupyter Notebooks Markdown cell -->
    </div> <!-- last line of Jupyter Notebooks Markdown cell -->
    
Acknowledgment:
[The Ultimate Markdown Guide (for Jupyter Notebook)](https://medium.com/analytics-vidhya/the-ultimate-markdown-guide-for-jupyter-notebook-d5e5abf728fd)

Further Reading
---------------

Friedman JM (2021-0714)
"Pitch (typewriter)" in
Wikipedia. The Wikimedia Foundation;
[https://en.wikipedia.org/wiki/Pitch_(typewriter)](https://en.wikipedia.org/wiki/Pitch_(typewriter))

Bricker D (2011-10-24)
"Book Design Basics Part 1: Margins and Leading" in
Book Design Basics;
[http://theworldsgreatestbook.com/book-design-part-1/](http://theworldsgreatestbook.com/book-design-part-1/)

CluBot NG et al. (2021-10-07) "Lorem ipsum" in
Wikipedia. The Wikimedia Foundation;
[https://en.wikipedia.org/wiki/Lorem_ipsum](https://en.wikipedia.org/wiki/Lorem_ipsum)

2605:A601:AADC:2100:C2FA:4802:5984:FA49 et al. (2021-05-24)
"Line length" in Wikipedia.
The Wikimedia Foundation; [https://en.wikipedia.org/wiki/Line_length](https://en.wikipedia.org/wiki/Line_length)

van Rossum G, Warsaw B, Coghlan N
(2001--2013)
Style Guide for Python Code, PEP 8.
[https://www.python.org/dev/peps/pep-0008/](https://www.python.org/dev/peps/pep-0008/)

Butterick M (2021) "line length" in Typography for Lawyers, 2 ed.
[https://typographyforlawyers.com/line-length.html](https://typographyforlawyers.com/line-length.html)

[https://www.humanfactors.com/newsletters/optimal_line_length.asp](https://www.humanfactors.com/newsletters/optimal_line_length.asp)

[https://www.usability.gov/get-involved/blog/2006/08/line-length-and-onscreen-reading.html](https://www.usability.gov/get-involved/blog/2006/08/line-length-and-onscreen-reading.html)
