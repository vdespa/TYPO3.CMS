.. include:: ../../Includes.txt

=====================================================================
Breaking: #78525 - Remove unused configuration options for JavaScript
=====================================================================

See :issue:`78525`

Description
===========

Remove all options that are not used anymore from TYPO3.configuration in JavaScript context.

:js:`TYPO3.configuration.moduleMenuWidth`
:js:`TYPO3.configuration.topBarHeight`


Impact
======

Both settings are not available anymore in JavaScript under :js:`TYPO3.configuration`.


Affected Installations
======================

Any installation that uses one of the mentioned options.


Migration
=========

No migration.

.. index:: Backend, JavaScript
