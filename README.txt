================================================================================
=== Asterisk 1.4 Backports
=== Russell Bryant <russell@digium.com
================================================================================

--------------------------------------------------------------------------------
File: func_devstate-1.4/func_devstate.c

Description: DEVSTATE dialplan function.  This function lets you create and
change custom device states from the dialplan.  It also lets you retrieve the
state of anything in Asterisk capable of providing device state.  This includes
all channel types, as well as some things like parking lots and MeetMe bridges.
--------------------------------------------------------------------------------

--------------------------------------------------------------------------------
File: chan_local_jitterbuffer.patch.txt

Description: This file adds jitterbuffer support to chan_local so that a
jitterbuffer can be used for IP calls to Asterisk applications.  Since the jb
only works between 2 bridged channels, this allows you to put a Local channel
in between the SIP channel and Voicemail, for example.  To enable the jb on a
Local channel, you use the 'j' option in addition with the 'n' option.

Example usage:
exten => 5551212,1,Dial(Local/1234@somecontext/nj)

[somecontext]
exten => 1234,1,MeetMe(1234)
--------------------------------------------------------------------------------

--------------------------------------------------------------------------------
File: dundiquery_dundiresponse_funcs.patch.txt

Description: DUNDIQUERY and DUNDIRESULT dialplan functions.  These functions
allow you to do a single DUNDi query from the dialplan, and then iterate through
all of the results.
--------------------------------------------------------------------------------

================================================================================
================================================================================
