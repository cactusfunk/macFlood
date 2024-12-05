# macFlood
exercise for chapter 2 of Ethical Hacking: A Hands on Introduction to breaking in

This is an attempt to write a python script that performs a MAC Flooding attack, which fills the CAM on a router/switch. This will cause a message/packet to be broadcast across all ports. I have run both versions of the script successfully but have either  
  a. Not set up my lab correctly  
  b. Don't realize that my firewall/router VM is not vulnerable to this attack  
  c. Am not looking in the correct place for results  
  d. Have not run the command long enough or with enough packets and it's working but the memory hasn't filled up yet.  

Included is a basic diagram of my internal LAN of vms that I am using for this lab. Be nice I'm a noob so if something is incorrectly used please tell me I want to learn.

Problem with version 1  
I am using the GUI to look at the ARP table because pfsense has a really nice one that I can log into from the kali vm's web browser. I did also go to shell on the pfsense machine and ran netstat -rn but according to what I read, the GUI is fine and much easier to read.
When I run the script from terminal on the kali vm, I see a ton of random mac addresses print, but the ARP table is not updating with any new entries as expected.  I included a screenshot of the error i got in terminal when I hit ctrl+c.

Problem with version 1.1     
This code works, and I sent 9999 packets twice. I then ran urlsnarf -i eth0 in a kali terminal, and then ran wget http://www.google.com/ on metasploitable, just to see if the packet was broadcast everywhere. It wasn't. I'm thinking about moving on because I feel confident in my understanding of what this attack is, but  I sure would like to figure out something that works where I can see the results.
