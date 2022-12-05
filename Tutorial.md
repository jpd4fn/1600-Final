## Using Kali Linux to test and explore the security of a system.

In this tutorial I have two systems
 - System 1 (Kali) IP = 192.168.200.1
 - System 2 (Clone) IP = 192.168.200.2

 In in the Kali system, I created a weak_password.txt file with some words that are commonly used as weak passwords. In the real-world text files like this can be found on the internet but they will contain hundreds of thousands of commonly used passwords. Hackers will even customize these files when targeting a specific company and add specific words from the company’s website or other related source to make the attack stronger. [Below]

![Password Text File](https://user-images.githubusercontent.com/60529599/205744565-e9b285a2-af52-4ced-9899-42f0cb227e4d.png)

 Next, I used one of Kali Linux’s tools, Nmap. I used Nmap to scan the clone system and it returned that there was one port open, port 22, which is for the ssh service. [Below]

![NmapScan](https://user-images.githubusercontent.com/60529599/205745555-3871d195-960b-471c-8d76-59019aa9aeb0.png)

 I know that port 22 is open for the ssh service, therefore I can use the Medusa tool to execute a brute-force attack on my clone system. In the command I specified the IP of the target system, a user to execute the passwords with, the name of the module, and the file containing the passwords to test. The Medusa tool found success when using the username ‘user’ with the password ‘admin’. 

![MedusaTool](https://user-images.githubusercontent.com/60529599/205746317-a8ad5333-9903-4101-90c6-31f29312c39c.png)

 With the information gained from running the Medusa tool, I am then able to SSH into the clone system from the Kali system. I used the ‘admin’ password found from medusa and was able to gain access into the clone system.

![SSHIntoClone](https://user-images.githubusercontent.com/60529599/205746559-f8453d54-65c3-4833-a3e3-ef07e09cf87b.png)


[Back to Main](Main.md)
