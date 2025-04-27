List of action to do a quick setup for a newly proxmox server 
#
- DO the setup from the dvd/cd boot usb, ensure that you keep every information you enter (root pass, IP). You will need them to log on into the server and/or on the web UI.
- Update the list of repo, where you can pull packages. In my environnement, im not using a subscription to proxmox repo. Since im not in a production environnement, it should be fine. 
  So we need to update our repo list. We will check that our debian repo are the ones we need, and add those for security update / proxmox repo. 
  Two ways of doing it : from a ssh access, or from the Proxmox UI on the webserver.
  If using ssh acces we can edit the main file or crea a repo file under /etc/apt/sources.list.d/ where info will be inside: 
    - Edit the following file sources.list who's located under /etc/apt/, and add the following line in the file 
      #Debian Repo 
      deb http://ftp.fr.debian.org/debian bookworm main contrib
      deb http://ftp.fr.debian.org/debian bookworm-updates main contrib
      # security updates
      deb http://security.debian.org bookworm-security main contrib
      # Proxmox repo
      deb http://download.proxmox.com/debian/pve bookworm pve-no-subscription

- 
      
