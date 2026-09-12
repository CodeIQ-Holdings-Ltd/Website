ContractIQ holding page
=======================

This page belongs on www.contractiqplatform.co.uk, NOT on this site. It is
kept in this repository only so it does not get lost, and the deploy workflow
is set to skip this folder — nothing in here ever reaches codeiqholdings.co.uk.

To put it live
--------------
Upload index.html to the document root of contractiqplatform.co.uk, named
index.html. It is a single self-contained file: the only external request is
the Google Fonts stylesheet. Rename any existing index.html first (for example
to index.live.html) so you can swap back in one move.

The two dates
-------------
Near the bottom of the file, in the <script> block, marked "EDIT THESE TWO
LINES":

  CLOCK_STARTS = "2026-09-14T09:00:00+01:00"   the countdown appears
  LAUNCH       = "2026-09-18T09:00:00+01:00"   the countdown ends

Before CLOCK_STARTS the page reads "The countdown starts Monday 14 September
at 9am". Between the two it shows a live ticking clock. After LAUNCH it
switches to "ContractIQ is open. Thanks for waiting." — so if the real site
goes up late, this page does not sit there claiming a launch that has not
happened.

The +01:00 is British Summer Time, which runs until 25 October 2026. After
that date use +00:00. The offset is written into the file deliberately so the
clock is right for a visitor in any time zone.

Taking it down
--------------
Delete or rename index.html on contractiqplatform.co.uk and put the real site
back. Keep this copy — reusing it for the next launch is two date edits and
one upload.

One thing to check before it goes live
--------------------------------------
The page carries <meta name="robots" content="noindex, follow">, so search
engines will not index a holding page and leave it ranking above the real
site. That line must be removed from the real site, not from this page.
