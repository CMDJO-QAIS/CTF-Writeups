![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/88ed6565-1498-4ccf-ab30-ad893a0b0e5f)

as we can see here the buffer is 64 bytes but we have an unbounded gets ,so we have an obvious buffer over flow

it's a RET2WIN challenge , but the canary is enabled 

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/33f1e988-e784-4505-ba1c-b8d80f296a9f)

we need to find a way to leak the canary so we can bufferover flow the binary and return to the win function , but how?

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/63db0f42-06f7-4924-9411-42a73c9afdc4)

as you can see in this line we have a 4 bytes leak , so you can guess it we can leak the canary from here

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/174381cf-9c43-48da-9b9b-dba48b7060d8)

we put 69 instead of 68 because of the null byte of the canary and the output is

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/4a885c0f-705f-4180-a65e-db86782082ae)

now we have the canary , then it's an easy RET2WIN challenge

this is the final payload 

![image](https://github.com/CMDJO-QAIS/CTF-Writeups/assets/160439920/8c582f12-509a-4893-8e6d-1969b64c5a83)

