# pwin2lin
Tool to convert exported windows putty sessions to linux putty sessions

Export the PuTTY registry settings from Windows:
 Start->Run->regedit
 HKEY_CURRENT_USER\\Software\\9bis.com\\
 Right click PuTTY and choose 'Export'. Save the registry file to your Linux machine and run this script from a shell (chmod 755 first):
 ./pwin2lin.pl

 Examples:
  Running the script alone:
    foo\@bar:~\$ ./pwin2lin.pl

  Specify files from the command line:
    foo\@bar:~\$ ./pwin2lin.pl myPuttySessions.reg /home/foo/.putty

Also, if using certs for auth, you will need to open the saved sessions and repoint them to your cert on the new system. I'll fix this at some point.
