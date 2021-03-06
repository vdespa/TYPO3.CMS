.. include:: ../../Includes.txt

=========================================================
Feature: #58637 - Purge language packs in language module
=========================================================

See :issue:`58637`

Description
===========

The language module in the backend offers the possibility to activate and deactivate language packs.
If deactivating a language pack that previously has been loaded, the data stays in typo3conf/l10n/<locale>/ .
A remove button is added to the actions. With the remove action the language is disabled and the data is removed from the typo3conf/l10n/<locale>/ directory.


Impact
======

The language data can now be removed from the installation.

.. index:: Backend