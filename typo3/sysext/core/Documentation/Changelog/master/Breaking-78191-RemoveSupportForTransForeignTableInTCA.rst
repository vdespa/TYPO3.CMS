.. include:: ../../Includes.txt

==============================================================
Breaking: #78191 - Remove support for transForeignTable in TCA
==============================================================

See :issue:`78191`

Description
===========

TCA allowed the definition of separate tables to hold localized and translated records.
The property names used for that were ``transForeignTable`` (basically pointed to
table ``pages_language_overlay``) and ``transOrigPointerTable`` (basically
pointed back to table ``pages``). The mentioned two pages tables are the only
tables that make use of this feature in the TYPO3 core.

To overcome special handling and to combine ``pages_language_overlay`` with
``pages`` at a later step, the configured table names are replaced with
hardcoded table names.


Impact
======

Modifications concerning the following two TCA control properties won't have
any effect anymore:

+ ``$TCA[<tableName>]['ctrl']['transForeignTable']``
+ ``$TCA[<tableName>]['ctrl']['transOrigPointerTable']``


Affected Installations
======================

All sites using localizations and translations for page hierarchies.


Migration
=========

No special actions are required if just the core defaults are used. Special
adjustments concerning the mentioned TCA properties should be verified and
hard-coded for the time being.

+ ``$TCA['pages']['ctrl']['transForeignTable']``, use value ``pages_language_overlay`` directly
+ ``$TCA['pages_language_overlay']['ctrl']['transOrigPointerTable']``, use value ``pages`` directly

.. index:: TCA
