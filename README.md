# putts - Probe Uptime by Tcp TimeStamps

putts sniffs for Tcp traffic of a remote host. If those Tcp packets contains
timestamps ([RFC 1323](https://www.ietf.org/rfc/rfc1323.txt)) this tool might
be used to get the systems uptime.

This script calls tcpdump(8) to get the Tcp timestamps of the target host.
You have to make Tcp traffic to the remote host after starting putts. Terminate
putts by pressing C-C after a while. Putts will print the assumed uptime
if enough data has been collected.

The determined tick value of the target host gives hints on the targets
operating system. The TICKS file shows known values of some operating systems.
