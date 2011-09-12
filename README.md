# Description

The patches have been grouped into directories corresponding to each
patch series that was sent to the mailing list.

The date and message-id for the cover letter email are provided here,
for posterity's sake; it should be trivial to find the thread and/or the
other emailed patches in the series on most common online mailing list
archive.

# Content listing

pre-v1: A preliminary patch series.

  Contents:
    0000-cover-letter.patch
      Date: Wed,  6 Jul 2011 14:15:42 +0800
      Message-Id: <1309932945-5048-1-git-send-email-rctay89@gmail.com>
    0001-xdiff-xprepare-use-memset.patch
    0002-xdiff-xpatience-factor-out-fall-back-diff-function.patch
    0003-t4033-diff-patience-factor-out-tests.patch

pre-v2: v2 of the preliminary series.
  
  Contents:
    0000-cover-letter.patch
      Date: Thu,  7 Jul 2011 00:38:53 +0800
      Message-Id: <1309970337-6016-1-git-send-email-rctay89@gmail.com>
    0001-xdiff-xprepare-use-memset.patch
    0002-xdiff-xprepare-refactor-abort-cleanups.patch
    0003-xdiff-xpatience-factor-out-fall-back-diff-function.patch
    0004-t4033-diff-patience-factor-out-tests.patch

pre-v3: v3 of the preliminary series.
  
  Contents:
    0000-cover-letter.patch
      Date: Thu,  7 Jul 2011 12:23:54 +0800
      Message-Id: <1310012638-3668-1-git-send-email-rctay89@gmail.com>
    0001-xdiff-xprepare-use-memset.patch
    0002-xdiff-xprepare-refactor-abort-cleanups.patch
    0003-xdiff-xpatience-factor-out-fall-back-diff-function.patch
    0004-t4033-diff-patience-factor-out-tests.patch

v1: The actual histogram diff implementation.
  
  Contents:
    v1/0000-cover-letter.patch
      Date: Tue, 12 Jul 2011 14:10:24 +0800
      Message-Id: <1310451027-15148-1-git-send-email-rctay89@gmail.com>
    
    v1/0001-teach-histogram-to-diff.patch
    v1/0002-xdiff-xprepare-skip-classification.patch
    v1/0003-xdiff-xprepare-use-a-smaller-sample-size-for-histogr.patch

v2: v2 of the implementation.

  Contents:
    v2/0000-cover-letter.patch
      Date: Mon,  1 Aug 2011 11:16:40 +0800
      Message-Id: <1312168608-10828-1-git-send-email-rctay89@gmail.com>
    v2/0001-xdiff-xprepare-use-memset.patch
    v2/0002-do-away-with-xdl_mmfile_next.patch
    v2/0003-xdiff-xprepare-refactor-abort-cleanups.patch
    v2/0004-xdiff-xpatience-factor-out-fall-back-diff-function.patch
    v2/0005-t4033-diff-patience-factor-out-tests.patch
    v2/0006-teach-histogram-to-diff.patch
    v2/0007-xdiff-xprepare-skip-classification.patch
    v2/0008-xdiff-xprepare-use-a-smaller-sample-size-for-histogr.patch

v2-rebased: The 'v2' series rebased on 'next'. To integrate 'v2' would
require re-rolling the series, but it already graduated to 'next', so
this series was sent in to make the maintainer's life easier.

  Contents:
    v2-rebased/0000-cover-letter.patch
      Date: Mon,  1 Aug 2011 12:20:06 +0800
      Message-Id: <1312172410-4380-1-git-send-email-rctay89@gmail.com>
    v2-rebased/0001-xdiff-do-away-with-xdl_mmfile_next.patch
    v2-rebased/0002-xdiff-xhistogram-rework-handling-of-recursed-results.patch
    v2-rebased/0003-xdiff-xhistogram-rely-on-xdl_trim_ends.patch
    v2-rebased/0004-xdiff-xhistogram-drop-need-for-additional-variable.patch
