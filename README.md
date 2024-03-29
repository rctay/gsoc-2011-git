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

## ptr-v*

These patches provided an implementation of the histogram diff algorithm
based on structs, instead of bitmasks. This reduced the complexity of
reading/writing of different fields and made code more readable.
However, there was a noticeable performance penalty, which held me back
from submitting these series. After running the code through a profiler,
I managed to pin the problem down to excessive `malloc()`s.

This implementation is the one that was submitted for inclusion.

## xd-v*

These patches were an attempt at improving the C histogram diff
implementation by reducing the calls to scanA() (the step that builds
the occurrence table) for each recursive sub-diff. This, of course,
ramped up the complexity of the code, but the performance gains were
minimal, so I junked this in the end.

## ptr2-v1

Like xd-v*; this was an initial try at reducing scanA() calls.

## guilt/master

Behind the scenes, I used [guilt] [guilt] to manage changes to my
patches. The folder contains a dump of my .git/patches/ repo (also
available in this repo at the [guilt/master branch] [guilt master].

## guilt/trim-ends

I toyed with the idea of skipping hashing of common head and tail lines
for a performance gain. However, as I worked on another diff-related
issue (see 'Related'), I began to doubt the correctness of this.

This series is still a work-in-progress and has not been submitted for
inclusion.

## gists/gist-*

* [gist: 1063164 [gsoc-diff] numbers] (https://gist.github.com/1063164)
* [gist: 1063175 [gsoc-diff] more numbers] (https://gist.github.com/1063175)
* [gist: 1066703 [gsoc-diff] alternate hashing ("golden ratio")] (https://gist.github.com/1066703)
* [gist: 1066773 [gsoc-diff] try_lcs: skip chains] (https://gist.github.com/1066773)
* [gist: 1066906 [gsoc-diff] diff --assume-text] (https://gist.github.com/1066906)
* [gist: 1068912 [gsoc-diff] malloc()/free() once] (https://gist.github.com/1068912)
* [gist: 1069099 [gsoc-diff] reduce number of rec accesses] (https://gist.github.com/1069099)
* [gist: 1074709 [gsoc-diff] reduce number of mallocs for gd-ptr] (https://gist.github.com/1074709)
* [gist: 1098863 [gsoc-diff] make trim tail support context] (https://gist.github.com/1098863)
* [gist: 1099236 [gsoc-diff] skip hashing of common leading lines] (https://gist.github.com/1099236)
* [gist: 1099515 [gsoc-diff] xdl_trim_head()] (https://gist.github.com/1099515)

# Related

Towards the close of the gsoc coding period, there was [a thread] [1] on
the git mailing list regarding performance issues with git-diff. With
the knowledge I had gained of git diff's machinery over the course of
gsoc, I managed to diagnose the problem and [submitted a patch] [2].

[1]: http://mid.gmane.org/loom.20110809T093124-847@post.gmane.org
[2]: http://mid.gmane.org/1313464312-5132-1-git-send-email-rctay89@gmail.com
[guilt]: http://www.kernel.org/pub/linux/kernel/people/jsipek/guilt/
[guilt master]: https://github.com/rctay/gsoc-2011-git/tree/guilt/master
