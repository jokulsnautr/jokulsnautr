The following are steps to start the ssh service and use it to get into your VM

..

Open you VM and run the command netstat -natp to see what ports, if any, are open

..

If port 22 is not listed, run sudo systemctl status ssh.service

..

This will validate whether ssh is running or disabled

..

If disabled, run sudo systemctl start ssh.service

..

To check the command worked, run sudo systemctl status ssh.service again and you should see that ssh is active (running)

..

With ssh running, go to your command prompt on your local host and ssh into your VM using the command ssh username@IPaddress

..

You will be prompted for your password

..

And that's it! You should now have successfully ssh'd into your VM

..

Happy Hacking