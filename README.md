<img width="2565" height="1455" alt="Screenshot (132))" src="https://github.com/user-attachments/assets/061381d5-e2db-4e45-b986-bdc4f5334a40" /><p align="center">
<img width="611" height="360" alt="image" src="https://github.com/user-attachments/assets/84286b7c-b517-4a8f-9ac5-73725e8ba0ca" /
/>
</p>

<h1>Active Directory - Congfiguring Account Lockouts and Resetting Passwords Using Group Policy</h1>
This tutorial teaches how to use Group Policy to configure account lockouts, as well as how to reset a locked accounts password.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory
- Group Policy 

<h2>Operating Systems Used </h2>

- Windows 10</b>



<h2> Steps</h2>

<p>
Within Windows Remote Desktop, attempt to log in to the account using an incorrect password. Do this 10+ times, you will notice that you will never get locked out of your account, you will see something like this! 
<img width="450" height="414" alt="Screenshot (123)" src="https://github.com/user-attachments/assets/f89d02fe-1127-4263-8007-baa93b3dee8a" />
</p>
<p>
In the Domain Controller, open group Policy management and select your Domain Policy (windows key, group policy management)
</p>
<br />
<p>
<img width="1054" height="725" alt="Screenshot (124)" src="https://github.com/user-attachments/assets/f6dca666-7e42-40b9-9d8e-a45372d68a08"
</p>
</p>

Go to Settings, then right click and select edit, select computer configuration > policies > windows settings > security settings > account policies > account lockout policy. You should then arrive to a screen that looks like this! 
<br />
<img width="1051" height="731" alt="Screenshot (126))" src="https://github.com/user-attachments/assets/ef525414-7eca-45b4-bf32-bbda03bea1f3" />
</p>
<p>

Configure the Policy Settings: (Set Account Lockout Threshold to 10 attempts)

    Account Lockout Duration: The amount of time, in minutes a lock out account remains locked before automatically unlocked. (Set to 10 Minutes)

    Account Lockout Threshold: The number of failed login attempts that will cause an account lockout. (Set to 10)
	
    Allow administer account lockout: Allows an administrator's account to become locked out.

    Reset account lockout counter after: The amount of time, in minutes, that must pass before the account's bad logon attempts resets to 0. (Set to 10 minutes)
</p>
<br />

Now attempt to Sign In as a client using an incorrect Password 10 times again. (Notice that you are now locked out)
<br />  
<img width="555" height="340" alt="Screenshot (128))" src="https://github.com/user-attachments/assets/5827f69a-fab9-4a8c-8fac-8c0dfb247e62" />
</p>
<p>
	
Back in the Domain Controller, open Active Directory Users and Computers (windows key, active directory users and computers) 
</p>
</p>
<img width="1266" height="824" alt="Screenshot (129))" src="https://github.com/user-attachments/assets/047b75db-2b6e-45e2-a0b4-b9a34bd74154" />
</p>
</p>

Find the locked out account, right click and select reset password. Type in the new password, and make sure to check the unlock user’s account button! 

</p>
</p>
<img width="1267" height="827" alt="Screenshot (130))" src="https://github.com/user-attachments/assets/09d6df31-8375-4a41-906b-332fac5772a0" />
</p>
</p>

Attempt to log back in on the account with the new password! (notice that you are now signed in!) 
</p>
</p>
<img width="2565" height="1455" alt="Screenshot (132))" src="https://github.com/user-attachments/assets/a02eefc7-edaf-4403-8d79-9ae310aaf464" />
</p>
</p>

<br />
  
<img width="1051" height="731" alt="Screenshot (126))" src="https://github.com/user-attachments/assets/ef525414-7eca-45b4-bf32-bbda03bea1f3" />

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
