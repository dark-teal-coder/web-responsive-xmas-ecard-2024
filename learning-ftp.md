---
description: Course Summary Notes
---

# Learning FTP

Video: Welcome

* FTP: File Transfer Protocol
* FTP is a common way of moving files around across networks and the internet
* Popular for managing files on host services

Video: What You Should Know

* Be familiar with using your operating system
* Be comfortable installing applications
* This course is built around the idea of working with files on a web host

Video: Using the Exercise Files

* Access to your own server to follow along with this course
* Or, download these files on the course homepage

Video: What Is FTP?

* FTP: File Transfer Protocol
* Sending and receiving or uploading and downloading files across a network
* Many web hosts offer FTP servers for customers to upload and download files
* Many companies host software update files, drivers and the like
* FTP servers for open-source projects are common
* Many Linux distributions have a wide network of FTP sites/mirrors
* Mirrors contain the same information where installation disc images can be downloaded
* Public FTP access generally discouraged outside a network firewall
* FTP servers: 1) login credentials 2) anonymous access
* FTP security:
* Credentials as plain text
* Best practice: unique credentials for access
* Alternatives include FTP-SSL & SFTP
* FTP connection URL:
* Structure: {protocol} + {username} + \[:] + {password} + \[@] + {hostname/address} + \[:] + {port} + \[/] + {file path}
* E.g., ftp://mary:abc123@example.com:21/file.zip
* The credential (username & password) can be omitted but it will be prompted if so
* FTP usually listens for commands on transmission control protocol (TCP) port 21
* The client and server will open other ports for data transfer automatically if the firewall allows
* FTP URL can be viewed in:
* A browser window, similar to a hyperlink
* A folder using a client application
* FTP modes:
* Active mode: server sends data to the client in response to a request from the client
* Passive mode: client requests data
* Better with network address translation (NAT)
* Common file transfer modes:
* Text: file sent as ASCII characters
* Binary: file sent as byte stream
* Automatic: mode auto-selected
* Home folder: landing place in the file system after login
* Able to be shared on a web host

Video: Connecting to An FTP Server Using Client Software

* To connect to an FTP server:
* Client software/client
* E.g., FileZilla
* Built-in FTP client
* E.g., web design tools, IDE’s and developer text editors, etc.
* Browser
* Operating system itself
* FileZilla:
* Download: [https://filezilla-project.org/](https://filezilla-project.org)
* Site connection information at top: host, username, password & port
* Site manager: commonly used sites
* Click \[File] > click \[Site Manager] > click \[New Site] > name a site > enter \[Host] > set \[Port] as 21 > choose \[FTP] for \[Protocol] > enter \[User] > enter \[Password] > click \[OK]
* Transfer files between local site and remote site:
* Local site on the left: your file system
* Remote site on the right: home folder on the FTP site
* \[Toggle directory comparison] feature in the toolbar: compare files between local and remote folders
* To disconnect: click \[Cancels the current operation] button in the toolbar

Video: Connecting to An FTP Server with A Web Browser

* FTP server’s URL into the browser to see a representation of the folders on the server
* Able to download
* Unable to upload, change or delete information

Video: Connecting to An FTP Server with Windows Explorer

* Windows Explorer can connect directly to FTP servers
* To open: press \[Windows logo key] + \[E]
* Address bar: type {FTP connection URL}
* Enter credentials
* Transfer take place in plain text
* Option to log on anonymously
* To add a network location: click \[Add a network location] in the ribbon > click \[Next] > choose \[Choose a custom network location] > click \[Next] > enter {FTP connection URL} into \[Internet or network address] > uncheck \[Log on anonymously] > enter \[User name] > click \[Next] > enter \[Type a name for this network location] > click \[Next] > check \[Open this network location when I click Finish] > click \[Finish] > enter credentials > click \[Log On]
* Handy shortcut to the FTP server at \[This PC] under \[Network locations]

Video: Connecting to An FTP Server from Linux

* File manager of a Linux GUI is able to connect to FTP servers
* Gnome environment: click \[Files] on menu > choose \[Connect to Server] > enter FTP path into \[Server Address] > choose \[Registered User] > enter credentials > click \[Connect]
* To end: click \[Eject] on the network in the sidebar

Video: Connecting to FTP from The Command Line

* Command line application in the terminal window:
* To log onto FTP: type \[ftp] > type \[open] + {server’s name} > press \[Enter]
* E.g., open rouxacademy.com
* Send commands to FTP application when the prompt changes to \[ftp>]
* Enter credentials for authentication
* To see what is in the directory: type \[ls] or \[dir]
* E.g., drwxr-xr-x        1 ldcsites         ldcsites        4096        Apr 25        2012        \_css
* Output 1st column:
* E.g., drwxr-xr-x
* 1st character: directory/file
* \[d] for directory
* \[-] for file
* Next 3 characters: file permissions for the user
* \[r] for read
* \[w] for write
* \[x] for execute
* Next 3 characters: file permissions for the group&#x20;
* \[r] for read
* \[w] for write
* \[x] for execute
* Next 3 characters: file permissions for everyone
* \[r] for read
* \[w] for write
* \[x] for execute
* Output 2nd & 3rd columns: user & group for each file
* E.g., ldcsites        ldcsites
* Output 4th column: size
* E.g., 4096
* Output 5th column: modification date
* E.g., Apr 25        2012
* Output last column: file name
* E.g., \_css
* To change directory: type \[cd] + {directory name}
* E.g., cd folder\_name
* To print current working directory: type \[pwd]
* To go back a level: type \[cd] + \[..]
* i.e., cd ..
* To download a file to your working directory: type \[get] + {file name}
* E.g., get index.htm
* To change the local directory: type \[lcd] + {path}
* To download multiple files to your working directory: type \[mget] + {a list of files/wildcard pattern}
* E.g., mget \*
* Choose which file to download one by one or use \[prompt] command to toggle the interactive mode off to get all the files at once
* Unable to download folders
* To jump out of the FTP command line: type \[!]
* To go back to FTP: type \[exit]
* To delete a file on the server: type \[delete] + {file path}
* E.g., delete index.htm
* To delete multiple files on the server: type \[mdelete] + {a list of files/wildcard pattern}
* To upload a file to the server: type \[put] + {file path}
* E.g., put index.htm
* To upload multiple files to the server: type \[mput] + {a list of files/wildcard pattern}
* To make directories: type \[mkdir] + {folder name}
* E.g. mkdir folder1
* To remove directories: type \[rmdir] + {folder name}
* E.g. rmdir folder1
* To see a list of commands available: type \[?]
* To exit FTP: type \[bye]

Video: Exploring SFTP

* SFTP: SSH file transfer protocol
* SSH connection instead of FTP
* Encrypted
* Just required to open one port to the outside world
* SFTP routes through one port (default 22)
* Easier to control
* More resilient to different network environments
* To connect:
* Type \[sftp] + {username} + \[@] + {domain}
* E.g., sftp preesa@example.com
* To specify a port: type \[sftp] + \[-oPort=] + {option} + {username} + \[@] + {domain}
* E.g., sftp -oPort=2222 preesa@example.com
* In case @ sign in the username: type \[sftp] + \[-oUser=] + {username} + \[@] + {domain in the username} + {server’s domain}
* E.g., sftp -oUser=preesa@webhost.com example.com

URL: [https://www.linkedin.com/learning/learning-ftp](https://www.linkedin.com/learning/learning-ftp)

### Post navigation
