checking the binary protections , we can see that pie and canary are enabled 
![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/53519a88-b3cf-4c79-9f37-d250e952bb2b)

and this is the win function so it's a RET2WIN challenge
![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/5ee00d2f-2b4e-42ea-be35-598e01b08f11)

and here is the bug of the challenge where we can leak pie and canary

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/c6eaba94-1d8d-4a96-a2ca-ce87cc49ae69)

so the binary ask for index in the card shuffle to leak but what if we gave it a negative number?
![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/ed61ff78-afe3-49a6-ad0b-8777cf4d2b4f)

as we can see we can leak vaules out of the cards boundaries

so we need to know the postion of pie and canary
![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/e16492bb-d338-4cd8-a2cf-4735ad261b42)

so this is how the canary looks like so we need to find what the postion in stack is it in

as you can see here we got the leak for a stack leak and the canary leak 

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/830e65db-3982-4c80-94da-e38a7800fc21)

now all we have to do is to write the solve script

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/ef868775-f5e9-432e-8211-adc6a7fa189e)
