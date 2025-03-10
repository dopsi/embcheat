Lessons learned
===============

Make sure CI builds are clean
-----------------------------

In a environment where developers on Windows and Linux collaborate, some files where checked into git with CRLF line terminators.
This caused git to checkout the file with LF terminators only and caused the git description (``git describe``) to be marked as dirty.

This was caught when `reproducible builds <./fw.html#reproducible-builds>`_ were put in place.