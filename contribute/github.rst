GitHub Guide
============

By `Lex Li`_

This page shows you how to use DockPanel Suite repo on GitHub to collaborate. 

.. contents:: In this article:
  :local:
  :depth: 1

Submitting a Patch
------------------

An issue might be opened to discuss with the maintainers before creating the patch. This helps the 
maintainers track your progress, and provide guidance if needed.

#. Learn about GitHub via https://help.github.com/.
#. Create your own fork from the main repo at https://github.com/dockpanelsuite/dockpanelsuite.
#. Create a new branch with a meaningful name.
#. Make the changes on this new branch in your fork, and test it fully.
#. Create a pull request back (link the new branch in your fork to the master branch of main repo).
#. Document all your changes in details as part of the pull request, which is critical to better communicate with maintainers.

Patches will be reviewed and merged as early as possible. 

.. note:: If the patch is large, it might take several weeks to review and merge.

.. note:: To see what makes a good pull request, please follow `Suggestions on Creating Pull Requests`_ section.

Reviewing a Patch
-----------------

Maintainers should respond to new pull requests as early as possible by commenting like this,

* "Acknowledged. Will start review." 

which gives the contributors a hint that the process has begun.

Further responses can be like,

* "Comments have been left at **. Please revise your patch like this,"
* "Reviewed. ** will be merged, while ** will not. The reasons are,"

which will keep all discussions public to reveal all necessary technical information for future reference.

Reporting a Bug
---------------

.. note:: If you already have a patch for the bug, please follow `Submitting a Patch`_ section.

.. note:: If you are not sure whether it is a bug, please follow `Asking a Question`_ section.

#. Learn about GitHub via https://help.github.com/.
#. Review existing issues at https://github.com/dockpanelsuite/dockpanelsuite/issues that are marked as bug or enhancement to avoid duplicate.
#. Please also review all open bugs on `SF.net tracker <https://sourceforge.net/tracker/?group_id=110642>`_ before reporting. Existing bugs recorded on SF.net may be gradually fixed in this fork, so you don't need to create duplicate items on GitHub.
#. Create a new issue on https://github.com/dockpanelsuite/dockpanelsuite/issues and provide all information in details.

You are welcome to provide step by step instructions, as that can help other reproduce and investigate 
the issue. If you are willing to share a sample project, please use a service such as `DropBox <https://dropbox.com>`_ or `OneDrive <https://onedrive.com>`_.

Reviewing a Bug
---------------

Maintainers should respond to bug reports as early as possible by commenting like this,

* "Acknowledged. Will start review." 

which gives the contributors a hint that the process has begun.

Further responses can be like,

* "Could not reproduce it. Please provide more information to assist investigation such as **,"
* "Reviewed. ** is a bug that can be reproduced. Will perform further investigation on how to resolve it. This may take a long time."

which will keep all discussions public to reveal all necessary technical information for future reference.

Asking a Question
-----------------

Asking a Question on StackOverflow (Recommended)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Log into `StackOverflow <https://stackoverflow.com>`_.
#. Before starting asking a new question, please review all questions under tag ``dockpanel-suite`` in case yours has already been answered.
#. Click Ask Question to create a new question. 
#. Add tag ``dockpanel-suite`` to this question, and also include all information in details.

Then you can wait till users reply to your question.

Asking a Question on GitHub
^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Learn about GitHub via https://help.github.com/.
#. Before creating the issue, please review all existing issues especially our `FAQ <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=faq+candidate&milestone=&page=1&state=closed>`_ in case the issue has already been reported and resolved.
#. Create a new issue on https://github.com/dockpanelsuite/dockpanelsuite/issues and provide all information in details. 

Answering a Question
--------------------

Maintainers might join StackOverflow and monitor discussions under ``dockpanel-suite`` tag.

Maintainers should respond to questions on GitHub as early as possible by commenting like this,

* "Acknowledged. Will start review." 

which gives the contributors a hint that the process has begun.

Further responses can be like,

* "Could not reproduce it. Please provide more information to assist investigation such as **,"
* "Reviewed. ** is a bug that can be reproduced. Will perform further investigation on how to resolve it. This may take a long time."

which will keep all discussions public to reveal all necessary technical information for future reference.

Tag such an issue with question tag.

Close such issues once a meaningful answer is given.

Mark an issue as ``faq candidate`` if it should be considered as an FAQ.

Overview of Issue Tags
------------------------

Maintainers should use the tags as early as possible so as to help each other to easily track the progress. The decoration tags are most useful for items which are not yet assigned to milestones.

Tags for Item Categories
^^^^^^^^^^^^^^^^^^^^^^^^^^

The following are used to assign an item to a specific category,

* `bug <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=bug>`_ This item was reported as a bug of this product. The reporter expects a fix.
* `enhancement <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=enhancement>`_ This item was reported as an enhancement request. The reporter expects a certain feature to be enhanced or a new feature to be implemented.
* `task <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=task>`_ This item was reported as a task. The reporter expects a maintainer to perform a piece of work (usually not development).
* `idea <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=idea>`_ This item was reported as a new idea. The reporter expects some discussion on a feature request. Once discussed, this item might be upgraded to an enhancement.
* `question <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=question>`_ This item was reported as a question. The reporter expects some discussion on a problem met about this product. Once discussed, this item might be upgraded to a bug, an enhancement, or an idea.
* `tech debt <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=tech+debt>`_ This item was reported as bad smells detected in the code base. The reporter expects changes in the code base to remove the bad smells.
* `pull request <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=pull+request>`_ This item was used to handle a pull request.

Tags for Decoration
^^^^^^^^^^^^^^^^^^^^^
The following are used to decorate an item so as to make it easy to see its status and required actions,

* `dependency bug <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=dependency+bug>`_ This only applies to bug items. It means the bug was caused by a bug of one of the dependencies (such as bugs of .NET Framework/Mono bugs, or bugs of the operating systems).
* `not an issue <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=not+an+issue>`_ This means after discussion, there is nothing to be done further (usually for false positives).
* `wontfix <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=wontfix>`_ This means the item (usually bugs) won't be fixed due to a strong justification. An agreement must be achieved among the maintainers.
* `duplicate <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=duplicate>`_ This means the item is exactly the same as another existing item. The maintainers should explicitly point out which item will be the focus and mark all the rest as duplicate.
* `tentative <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=tentative>`_ This means based on the provided information it is not likely to move on. The reporter should provide more information and drive the discussion.
* `soon to close <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=soon+to+close>`_ This means there is little left to do on the item. The maintainers are going to close the item after a few more days (usually applied to tentative and cannot reproduce items).
* `cannot reproduce <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=cannot+reproduce>`_ This means the maintainers failed to reproduce the symptoms described in a bug report. The reporter should provide more information (process dumps, sample projects, screen shots, video clips and so on) and drive the investigation.
* `in progress <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=in+progress>`_ This means the item has been actively investigated by the maintainers.
* `up for grabs <https://github.com/dockpanelsuite/dockpanelsuite/issues?labels=up+for+grabs>`_ This means community contribution is welcome.

Suggestions on Creating Pull Requests
-------------------------------------
All pull requests are appreciated (even if some we cannot merge). The following can make the pull requests simpler for reviewers, so hope you can follow them.

* If possible, send multiple pull requests for individual tasks and avoid a pull request for multiple tasks. Properly isolating changes to meaningful batches makes it quicker to analyze and assert the changes.
* Fork and create a new branch with a meaningful name first before making the changes.
* Squash all commits on this new branch to only one or two before sending the pull request.
* Wait for comments from the reviewers. It usually takes weeks as the reviewers might not be able to finish quickly. Don't make further changes at this stage to avoid changes of this pull request.
* Revise the code based on feedbacks, and then make a second commit with necessary changes and push to the branch in your fork, where GitHub automatically appends it to the pull request for further review.

Then the reviewers will decide whether to accept or reject the pull request based on code quality.

One important notice is that some pull requests might not be accepted, but they are still valuable to the community,

* It contains a nice-to-have feature (such as options to enable/disable part of a theme, or a visual element) for some users but not all.
* It introduces a feature (such as new visual elements) that goes beyond Visual Studio look and feel.

Such pull requests are of great value of course. But since the primary goal of DPS is to simulate Visual Studio look and feel, and the code base is already huge to maintain, we try to avoid bringing in non-core features.

Suggestions on Reviewing Pull Requests
--------------------------------------
Please leave a message that you are going to review a pull request. That should let the submitter know it's been reviewed.

Leave all comments at a time, so that the submitter can revise them altogether to form a new commit.

Decide carefully whether to accept or reject a pull request. Leave explanation for future reference.

Related Resources
-----------------

- :doc:`/getting-started/installing-on-windows`
- :doc:`/tutorials/basics`
- :doc:`/themes/existing-themes`
