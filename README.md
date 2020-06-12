# DVWA-CSRF-ATTACK-DEMO
CSRF attack demo on DVWA(Damn Vulnerable Web App ) which is coded in PHP/MYSQL and is intentionally made vulnerable to learn how an application can be compromised using different techniques


# CSRF attack
***Note : Performed the attacks on virtual machine on Kali Linux OS. Performing the experiments in Virtual machine or Container is preferred for security purposes.***


    Part 1 : Low security mode
**Describe the attack you used. How did it work?**
Performed CSRF attack on DVWA application in low security mode.
Changed the password for the application by changing the script behind the
change button and setting the new password as root in hidden parameters behind the button.

The code looks like this:
![Code ](https://github.com/Prachal80/DVWA-CSRF-ATTACK-DEMO/blob/master/img/request%20.png)

The request that was made after clicking the button was:
![Success](https://github.com/Prachal80/DVWA-CSRF-ATTACK-DEMO/blob/master/img/success.png)

Upon the execution of the request, the password was set as root.
![enter image description here](https://github.com/Prachal80/DVWA-CSRF-ATTACK-DEMO/blob/master/img/low.png)
