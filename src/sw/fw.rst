Firmware
========

Design and architecture considerations
--------------------------------------

Firmware identification
^^^^^^^^^^^^^^^^^^^^^^^

.. |source_date_epoch| replace:: the ``SOURCE_DATE_EPOCH`` variable
.. _source_date_epoch: https://reproducible-builds.org/docs/source-date-epoch/

Important information:

* firmware version (using a single source of truth)
* git description (``git describe --abbrev=10 --always --dirty``)
* build time (for :ref:`reproducible_builds`, use |source_date_epoch|_)
* `GNU build ID <https://interrupt.memfault.com/blog/gnu-build-id-for-firmware>`_

See also:

* `GNU build ID <https://interrupt.memfault.com/blog/gnu-build-id-for-firmware>`_
* `Release versioning <https://interrupt.memfault.com/blog/release-versioning>`_

.. _reproducible_builds:

Reproducible builds
^^^^^^^^^^^^^^^^^^^

`Reproducible builds <https://reproducible-builds.org/>`_ are an effort to make sure the output of a build process is independent from the environment.

Important sources of non-reproducibility:

* the ``__FILE__`` macro
* build dates and times

See also:

* `Memfault article <https://interrupt.memfault.com/blog/reproducible-firmware-builds>`_

