we get a pcap file full of dns packets

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/d0a7b2a4-fa6a-41bf-b6cd-ed6cef268c5e)

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/826c5c6c-19de-42d9-b378-7a6a0f3ad894)

as we can see there is some base64.somedomain.com
so obvious we need the subdomain of each , we have like 50 + domains , and i tried someof them and all were like troll pictures , so i went and toke the biggest domain
in size and it was microsoftonline , so with this tshark command

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/629a9094-0438-4091-a60b-2b69b317bc61)

removing all the domains and leaving only the subdomains
![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/2e62fd0c-14ce-4b4a-96cc-ec6f8b51ffd6)


no we take it to cyberchef

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/21de0970-2578-4212-bba6-a1c24b49b7d1)

