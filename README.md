EktoMM README
=============

Set Operations in the Shell:
http://www.catonmat.net/blog/set-operations-in-unix-shell/

ektomm-send
-----------

ektomm-send takes one argument and reads recipients from stdin, one per line.
Whenever a message was sent succefully the respective recipient is printed to
stdout, one per line.

Sending a Campaign
------------------
To send a campaign a configuration file and a list of recipients needs
to be provided. In the following example recipients for which the message was
sent are printed to the file sent.txt. In case ekotmm-send terminates before
the campaign was sent to all recipients the delivery can be resumed by using
the same command again.

comm -23 <(sort recipients.txt) <(sort sent.txt) | ektomm-send mycampaign.php 1>>sent.txt


