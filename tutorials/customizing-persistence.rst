Customizing Persistence
=======================

By `Lex Li`_

This page shows you how to customize persistence. 

.. contents:: In this article:
  :local:
  :depth: 1

Overriding Persistent String
----------------------------
As the sample project shows, by default when current layout is saved to disk only class name is persisted. As a result, in delegate ``IDockContent DeserializeDockContent(string persistString)`` only class name is used to reconstruct the layout.

The current design gives you flexibility to control what other information about each dock items to be persisted, as the method ``DockContent.GetPersistString()`` can be overridden by derived classes. By properly overriding it, extra data (such as custom data about the internal components of a dock item) can be appended to the string. Thus, when the layout is reconstructed, the extended persist string can be analyzed and extra data can be extracted and used.