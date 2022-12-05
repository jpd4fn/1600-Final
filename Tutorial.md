## Using Kali Linux to test and explore the security of a system.

In this tutorial I have two systems
 - System 1 (Kali) IP = 192.168.200.1
 - System 2 (Clone) IP = 192.168.200.2

In in the Kali system, I created a weak_password.txt file with some words that are commonly used as weak passwords. In the real-world text files like this can be found on the internet but they will contain hundreds of thousands of commonly used passwords. Hackers will even customize these files when targeting a specific company and add specific words from the company’s website or other related source to make the attack stronger. [Below]

![Password Text File](https://user-images.githubusercontent.com/60529599/205744565-e9b285a2-af52-4ced-9899-42f0cb227e4d.png)

Next, I used one of Kali Linux’s tools, Nmap. I used Nmap to scan the clone system and it returned that there was one port open, port 22, which is for the ssh service. [Below]

![image](https://user-images.githubusercontent.com/60529599/205745555-3871d195-960b-471c-8d76-59019aa9aeb0.png)

