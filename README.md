# DVWA-CSRF-ATTACK-DEMO
CSRF attack demo on DVWA(Damn Vulnerable Web App ) which is coded in PHP/MYSQL and is intentionally made vulnerable to learn how an application can be compromised using different techniques

![Application Home page](https://github.com/Prachal80/DVWA-CSRF-ATTACK-DEMO/blob/master/img/DVWA.png)


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


    Part 2 : Medium security mode
    
  **Does your attack work in “Medium” security level?**
  
After changing the password, the security mode was set to medium and this was the output when the request was made: The reason why it didn’t work was that the medium level checks whether the request came from trusted source. Thus the previous method wont work on medium level.

![Request failed](https://github.com/Prachal80/DVWA-CSRF-ATTACK-DEMO/blob/master/img/medium.png)

The reason why it didn’t work was that the medium level checks whether the request came from trusted source. Thus the previous method wont work on medium level.
![Medium level code ](https://github.com/Prachal80/DVWA-CSRF-ATTACK-DEMO/blob/master/img/medium%20level.png)

 Part 3 : High security mode

**Set the security mode to “Low” and examine the code that is vulnerable, and then set the security mode to “High” and reexamine the same code. What changed? How do the changes prevent the attack from succeeding?**

In high security mode, tokens are used so we it prevented the CSRF attack from happening. In low mode, there are no checks that can prevent the attack from happening.
![High level code](https://github.com/Prachal80/DVWA-CSRF-ATTACK-DEMO/blob/master/img/High%20level.png)

![Low level code](https://github.com/Prachal80/DVWA-CSRF-ATTACK-DEMO/blob/master/img/low%20level.png)
