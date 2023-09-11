# How to SSH Into Your VM


##The following are steps to start the ssh service and use it to get into your VM

---

1. Open you VM and run the command **_netstat -natp_** to see what ports, if any, are open

---

2. If port 22 is not listed, run **_sudo systemctl status ssh.service_**


- This will validate whether ssh is running or disabled

---

3. If ssh is  disabled, run **_sudo systemctl start ssh.service_**

---

4. To check the command worked, run **_sudo systemctl status ssh.service_** again and you should see that ssh is **active (running)**

---

5. With ssh running, go to your command prompt on your local host and ssh into your VM using the command **_ssh username@IPaddress_**


- You will be prompted for your password

---

And that's it! You should now have successfully ssh'd into your VM!

###Happy Hacking
