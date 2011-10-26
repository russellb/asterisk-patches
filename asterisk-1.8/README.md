# Patches for Asterisk 1.8

# ```queue_wrapup_blocker.txt```

This patch was written for a particular deployment of Asterisk that uses queues
on multiple servers as well as the distributed device state functionality.  They
wanted to ensure that wrapuptime for an agent was honored across the cluster of
servers.  Once an agent has taken a call on one server, no other Asterisk server
will send that agent a call until the wrapuptime has expired.
