# How to SSH Into Your VM


### The following are steps to start the ssh service and use it to get into your VM

---

1. Open your VM and run the command: 

```
netstat -natp
``` 

- This is to see what ports, if any, are open

---

2. If port 22 is not listed, run: 

```
sudo systemctl status ssh.service
```

- This will validate whether ssh is running or disabled

---

3. If ssh is  disabled, run: 

```
sudo systemctl start ssh.service
```

---

4. To check the command worked, run: 

```
sudo systemctl status ssh.service 
```

- You should see that ssh is **active (running)**

---

5. With ssh running, go to your command prompt on your local host and ssh into your VM using the command: 

```
ssh username@IPaddress
```

- You will be prompted for your password

---

And that's it! You should now have successfully ssh'd into your VM!

#### Happy Hacking
