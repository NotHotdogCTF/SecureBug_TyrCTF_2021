In this challenge we are given a pcap file

So, we open it in wireshark

If we view the TCP stream of requests we can see someone logging in to a localhost webpage and watching a video

We can get the admin credentials by looking at the requests but as this is a locally hosted server that won't help us

However, we do have the bytes of the video file

We can export this using wireshark to see what exactly the video they watched was

Exporting it gives us a video of someone stroking a duck... and our flag written across the top!

SBCTF{1n53cur3_commun1c471on}
