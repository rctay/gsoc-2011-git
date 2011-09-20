# Description

The patches have been grouped into directories corresponding to each
patch series that was sent to the mailing list.

The date and message-id for the cover letter email are provided here,
for posterity's sake; it should be trivial to find the thread and/or the
other emailed patches in the series on most common online mailing list
archive.

# Content listing

## pre-v1

A preliminary patch series.

* 0000-cover-letter.patch

    Date: Wed,  6 Jul 2011 14:15:42 +0800

    Message-Id: <1309932945-5048-1-git-send-email-rctay89@gmail.com>
* 0001-xdiff-xprepare-use-memset.patch
* 0002-xdiff-xpatience-factor-out-fall-back-diff-function.patch
* 0003-t4033-diff-patience-factor-out-tests.patch

## pre-v2

v2 of the preliminary series.

* 0000-cover-letter.patch

    Date: Thu,  7 Jul 2011 00:38:53 +0800

    Message-Id: <1309970337-6016-1-git-send-email-rctay89@gmail.com>
* 0001-xdiff-xprepare-use-memset.patch
* 0002-xdiff-xprepare-refactor-abort-cleanups.patch
* 0003-xdiff-xpatience-factor-out-fall-back-diff-function.patch
* 0004-t4033-diff-patience-factor-out-tests.patch

## pre-v3

v3 of the preliminary series.

* 0000-cover-letter.patch

    Date: Thu,  7 Jul 2011 12:23:54 +0800

    Message-Id: <1310012638-3668-1-git-send-email-rctay89@gmail.com>
* 0001-xdiff-xprepare-use-memset.patch
* 0002-xdiff-xprepare-refactor-abort-cleanups.patch
* 0003-xdiff-xpatience-factor-out-fall-back-diff-function.patch
* 0004-t4033-diff-patience-factor-out-tests.patch

## v1

The actual histogram diff implementation.

* 0000-cover-letter.patch

    Date: Tue, 12 Jul 2011 14:10:24 +0800

    Message-Id: <1310451027-15148-1-git-send-email-rctay89@gmail.com>
* 0001-teach-histogram-to-diff.patch
* 0002-xdiff-xprepare-skip-classification.patch
* 0003-xdiff-xprepare-use-a-smaller-sample-size-for-histogr.patch

## v2

v2 of the implementation.

* 0000-cover-letter.patch

    Date: Mon,  1 Aug 2011 11:16:40 +0800

    Message-Id: <1312168608-10828-1-git-send-email-rctay89@gmail.com>
* 0001-xdiff-xprepare-use-memset.patch
* 0002-do-away-with-xdl_mmfile_next.patch
* 0003-xdiff-xprepare-refactor-abort-cleanups.patch
* 0004-xdiff-xpatience-factor-out-fall-back-diff-function.patch
* 0005-t4033-diff-patience-factor-out-tests.patch
* 0006-teach-histogram-to-diff.patch
* 0007-xdiff-xprepare-skip-classification.patch
* 0008-xdiff-xprepare-use-a-smaller-sample-size-for-histogr.patch

## v2-rebased

The 'v2' series rebased on 'next'. To integrate 'v2' would require
re-rolling the series, but it already graduated to 'next', so this
series was sent in to make the maintainer's life easier.

* 0000-cover-letter.patch

    Date: Mon,  1 Aug 2011 12:20:06 +0800

    Message-Id: <1312172410-4380-1-git-send-email-rctay89@gmail.com>
* 0001-xdiff-do-away-with-xdl_mmfile_next.patch
* 0002-xdiff-xhistogram-rework-handling-of-recursed-results.patch
* 0003-xdiff-xhistogram-rely-on-xdl_trim_ends.patch
* 0004-xdiff-xhistogram-drop-need-for-additional-variable.patch

# Un-mailed patches

## raw-v*

These patches were a naive, line-to-line conversion of JGit's histogram
diff implementation. You can see that information is stored as an
integer bitmask, with shifts being used to read/write different fields.

## guilt

Behind the scenes, I used [guilt] [guilt] to manage changes to my
patches. The folder contains a dump of my .git/patches/ repo (also
available in this repo at the [guilt/gsoc-diff branch] [guilt branch].

# Related

Towards the close of the gsoc coding period, there was [a thread] [1] on
the git mailing list regarding performance issues with git-diff. With
the knowledge I had gained of git diff's machinery over the course of
gsoc, I managed to diagnose the problem and [submitted a patch] [2].

[1]: http://mid.gmane.org/loom.20110809T093124-847@post.gmane.org
[2]: http://mid.gmane.org/1313464312-5132-1-git-send-email-rctay89@gmail.com
[guilt]: http://www.kernel.org/pub/linux/kernel/people/jsipek/guilt/
[guilt branch]: https://github.com/rctay/gsoc-2011-git/tree/guilt/gsoc-diff
