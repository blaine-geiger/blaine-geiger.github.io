---
layout: post
title: Hacking an Excel File For a Good Cause
date: 2024-04-05 15:01:35 +0300
image: '/images/excel.jpg'
---

A month after finishing my BSIT. I faced a real situation where my skills would be put to the test. 

A family I knew closely had recently lost a familly member who had passed away. We will call them Jenny. She was responsible, had plans in place, and took countless steps to make things easier for her family. This is not a discussion or criticism of anyone's security practices. 

Jenny did not use a password manager. All of her passwords were stored in an Excel spreadsheet. However, this Excel spreadsheet was password protected, and this password was not one of her commonly used passwords. After numerous attempts, the family was unable to brute-force the password by guessing.

They were at a loss and had no easily identifiable solution. <i>So here is what I did.</i>

I needed the file. I was a trusted person, so I was given access to the file. I would need the file on my device to perform the relevant work. I transferred the file to my laptop and spun up a Kali Linux VM.

* I researched methods and noted there were many <b>paid</b> options, <i>no thank you...</i>
* I inspected the file, which we will call `locked.xls` I noted its extension
* The file was a .xls extension and you may know where this is going, or maybe not
* I also noted the file type was a legacy Excel 97 - 2003 Excel file

Now I knew there was a possibility. The .xls file type has weaker encryption than the newer .xlsx type. Even though the file had been modified recently, it was created with an old version of the Excel application or had always been saved in legacy mode and never converted to the newer .xlsx format. To be fair, conversion of older .xls to .xlsx formats can cause data issues depending on many different factors, so be cautious.

* I did some more research and discovered the `office2john.py` tool

I knew exactly what I planned to do. The office2john tool was going to extract the hashed password from the file, but if you know what a hash is, you can't just reverse a hash into its original password. That is not how it works.

* I ran the office2john.py tool with `python3 office2john.py locked.xls > hash.txt`

Now I had the hash, but the work wasn't over. This was no guarantee. From here the research was over though. I just needed the hash.

* I unzipped the rockyou wordlist with `gunzip /usr/share/wordlists/rockyou.txt.gz`
* I ran the hash file into John The Ripper `john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt`

<i>I waited.....  </i>
  
I was honestly shocked when the result came back with a cracked hash. Like I said, none of this was guaranteed.

* Displaying the cracked password was simply `john --show hash.txt`

Still I did not celebrate. There it was in plaintext, but I held back my excitement.

* I double clicked the file on the Windows Desktop and it prompted me with a dialog box reading `file.xls is protected. Password:`
* I entered the plaintext password that I had cracked.
* The Excel sheet opened up and displayed hundreds of accounts, usernames, and passwords.

<i>.....then I celebrated.</i>

The file contained everything you can imagine, from frivilous accounts that were no longer important, to very serious government and financial accounts. The family was very grateful to have this information at such a difficult time in their lives. 

— Blaine Geiger, 4-16-2025