<p align="center">
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


<br />
  
<img width="1051" height="731" alt="Screenshot (126))" src="https://github.com/user-attachments/assets/ef525414-7eca-45b4-bf32-bbda03bea1f3" />

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<br />
  
<img width="1051" height="731" alt="Screenshot (126))" src="https://github.com/user-attachments/assets/ef525414-7eca-45b4-bf32-bbda03bea1f3" />

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
