---
layout: post
title: 'ImportError: No module named svn'
category: programming
---

Recently I moved my CVS and Subversion repositories to a VPS that is running the server edition of Ubuntu Hardy.  As part of the move I installed ViewCV enabling me to view my repositories via a web browser.  Problem was when I viewed a Subversion repository I got the following error message:<br /><br /><code><br />An Exception Has Occurred<br />Python Traceback<br />Traceback (most recent call last):<br />  File "/usr/local/viewcvs-1.0-dev/lib/viewcvs.py", line 3194, in main<br />    request.run_viewcvs()<br />  File "/usr/local/viewcvs-1.0-dev/lib/viewcvs.py", line 258, in run_viewcvs<br />    import vclib.svn<br />  File "/usr/local/viewcvs-1.0-dev/lib/vclib/svn/__init__.py", line 27, in ?<br />    from svn import fs, repos, core, delta<br />ImportError: No module named svn<br /></code><br /><br />I could view CVS repository just not Subversion repositories.  This left me scratching my head.  I did a couple of google searches but no solution found.  Then I thought to myself, "I wonder if there is anything Python specific for Subversion."  This prompted me to try searching for packages using the aptitude command.<br /><br />Sure enough the command <b>aptitude search subversion</b> returned a few items including <b>python-subversion</b>, which is the Python binding for Subversion.  Bingo!  I ran the command <b>aptitude install python-subversion</b> then checked ViewCV again in my browser.  Error gone.  I'm now able to view both CVS and SVN repositories.