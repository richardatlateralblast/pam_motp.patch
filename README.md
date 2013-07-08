pam_motp.patch
==============

PAM Mobile OTP Patch for Solaris

http://motp.sourceforge.net/

Fixes
=====

Makefile: 

Fixes compilation and install directories on Solaris 10.

pam_mobile_otp.c:

Without this patch on Solaris 10 the GMT offset in /etc/security/motp.conf is the number of hours the client is offset from the server, ie if its in the same timezone it's 0. With this patch the offset is the actual GMT offset of the client, eg in Australia it would be 10.
