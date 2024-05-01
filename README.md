### Deploy-a-VPS for free

Windows VPS:
- create a github repo
- create a github codespace inside your repo that has the default iamge and has 16gig of ram
- git clone this repo
- do "docker-compose up -d" in your terminal (Note this can work on other stuff, Not just github codespaces)



### How do I select the Windows version?

  By default, Windows Server 2022  will be installed. But you can add the `VERSION` environment variable to your compose file, in order to specify an alternative Windows version to be downloaded:
  Note that your problem is storage. Windows server 2022 is pertty small and useable

  ```yaml
  environment:
    VERSION: "win110
  ```

  Select from the values below:
  
  | **Value**  | **Version**  | **Size**  |
  |---|---|---|
  | `win11`   | Windows 11 Pro | 6.4 GB    |
  | `win11e`   | Windows 11 Enterprise | 5.8 GB    |
  | `win10`   | Windows 10 Pro | 5.8 GB    |
  | `ltsc10`  | Windows 10 LTSC       | 4.6 GB    |
  | `win10e`   | Windows 10 Enterprise | 5.2 GB    |
  | `win81`   | Windows 8.1 Pro | 4.2 GB    |
  | `win81e`   | Windows 8.1 Enterprise | 3.8 GB    |
  | `win7`    | Windows 7 Enterprise | 3.0 GB    |
  | `vista`   | Windows Vista Ultimate | 3.6 GB    |
  | `winxp`   | Windows XP Professional | 0.6 GB    |
  ||||
  | `2022`    | Windows Server 2022   | 4.7 GB    |
  | `2019`    | Windows Server 2019   | 5.3 GB    |
  | `2016`    | Windows Server 2016   | 6.5 GB    |
  | `2012`    | Windows Server 2012   | 4.3 GB    |
  | `2008`    | Windows Server 2008   | 3.0 GB    |
  ||||
  | `core11`  | Tiny 11 Core | 2.1 GB    |
  | `tiny11`  | Tiny 11            | 3.8 GB    |
  | `tiny10`  | Tiny 10            | 3.6 GB   |

### How do I connect using RDP?

  The web-viewer is mainly meant to be used during installation, as its picture quality is low, and it has no audio or clipboard for example.

  So for a better experience you can connect using any Microsoft Remote Desktop client to the IP of the container, using the username `docker` and by leaving the password empty.

  There is a good RDP client for [Android](https://play.google.com/store/apps/details?id=com.microsoft.rdc.androidx) available from the Play Store and one for [iOS](https://apps.apple.com/nl/app/microsoft-remote-desktop/id714464092?l=en-GB) in the Apple Store. For Linux you can use [FreeRDP](https://www.freerdp.com/) and on Windows just type `mstsc` in the search box.

### How do I change the size of the disk?

  To expand the default size of 24 GB, edit the `DISK_SIZE` in your compose file and set it to your preferred capacity:

  ```yaml
  environment:
    DISK_SIZE: "32G"
  ```
  
  This can also be used to resize the existing disk to a larger capacity without any data loss.

  Ubuntu VPS: 
  - create a github repo
  - create a github codespace inside your repo that has the default iamge and has 16gig of ram
  - Run this in your terminal: `sudo docker run -it ubuntu:22.04`. and if you want systemctl run `sudo apt install systemd` and this will install systemd and systemctl, make sure to reboot the ubuntu vps after installing systemd/systemctl. Also you can create mutilable ubuntu vps(s) by running the command again for another one.
