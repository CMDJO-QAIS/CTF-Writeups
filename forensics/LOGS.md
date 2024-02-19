the challenge gaved us sysmon logs and asked us about the suspicous behaviour for the attacker
![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/d8eb7907-cf08-4986-b496-f20699719504)

this was an easy and straight forward challenge if you know basics forensics , so the first thing i headed to was the security logs but i wasn't lucky with them
, then i thought suspicous behavior + event logs , it must be some persistence technique and there is one famous technique which is putting your script/command in the 
taskschedule but here we are not hunting an attacker , we are hunting a flag , so i opened the task schedule event logs

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/aff6934a-3d46-42a0-b70f-27f2c2e13907)

and as you can see our flag is the latest schedule task
