Implementation Guide
====================

This will potentially use mixed cases if we re-implement the GUI with Qt.
Qt-based code should use ``lowerCamelCase``, while regular Python should be ``underscore_case``

Not every multi-word variable or function name needs to be broken up with underscores.
Example: ``batchsize``. It is short enough to have no word separators without impacting
readability adversely. Longer variable names like ``prominenttroughs`` should probably be
``prominent_troughs``, and any variable names consisting of 3 or more words should have
separators. However, note that these are guidelines rather than hard rules, so use your
best judgment when exceptions arise. The primary goal here is readability.