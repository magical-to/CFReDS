# **CFReDS 문제 풀이**

## **Data Leakage Case**  
**The purpose of this work is to learn various types of data leakage, and practice its investigation techniques.**

---

### **Scenario Overview**  

‘Iaman Informant’ was working as a manager of the technology development division at a famous international company OOO that developed state-of-the-art technologies and gadgets.

One day, at a place which ‘Mr. Informant’ visited on business, he received an offer from ‘Spy Conspirator’ to leak sensitive information related to the newest technology. Actually, ‘Mr. Conspirator’ was an employee of a rival company, and ‘Mr. Informant’ decided to accept the offer for large amounts of money and began establishing a detailed leakage plan.

‘Mr. Informant’ made a deliberate effort to hide the leakage plan. He discussed it with ‘Mr. Conspirator’ using an e-mail service like a business relationship. He also sent samples of confidential information through personal cloud storage.

After receiving the sample data, ‘Mr. Conspirator’ asked for the direct delivery of storage devices that stored the remaining (large amounts of) data. Eventually, ‘Mr. Informant’ tried to take his storage devices away, but he and his devices were detected at the security checkpoint of the company. And he was suspected of leaking the company data.

At the security checkpoint, although his devices (a USB memory stick and a CD) were briefly checked (protected with portable write blockers), there was no evidence of any leakage. And then, they were immediately transferred to the digital forensics laboratory for further analysis.

### **Company Information Security Policies**
- Confidential electronic files should be stored and kept in the authorized external storage devices and the secured network drives.
- Confidential paper documents and electronic files can be accessed only within the allowed time range from **10:00 AM to 16:00 PM** with the appropriate permissions.
- **Non-authorized electronic devices** such as laptops, portable storages, and smart devices **cannot be carried** onto the company.
- All employees are required to pass through the **‘Security Checkpoint’ system**.
- All storage devices such as HDD, SSD, USB memory stick, and CD/DVD are **forbidden** under the **‘Security Checkpoint’ rules**.

In addition, although the company managed **separate internal and external networks** and used **DRM (Digital Rights Management) / DLP (Data Loss Prevention) solutions** for their information security, **‘Mr. Informant’ had sufficient authority to bypass them.** He was also very interested in IT (Information Technology) and had a slight knowledge of digital forensics.

**In this scenario, find any evidence of the data leakage, and any data that might have been generated from the suspect’s electronic devices.**

---

## **Hacking Case**  
**Find any hacking software, evidence of their use, and any data that might have been generated. Attempt to tie the computer to the suspect, G=r=e=g S=c=h=a=r=d=t.**

---

### **Scenario**  

On **09/20/04**, a **Dell CPi notebook computer**, serial # **VLQLW**, was found abandoned along with a **wireless PCMCIA card** and an **external homemade 802.11b antenna**. It is suspected that this computer was used for **hacking purposes**, although it cannot be tied to a hacking suspect, **G=r=e=g S=c=h=a=r=d=t**. (The equal signs are just to prevent web crawlers from indexing this name; there are no equal signs in the image files.)  

**Schardt also goes by the online nickname of “Mr. Evil”** and some of his associates have said that he would **park his vehicle within range of Wireless Access Points** (like Starbucks and other T-Mobile Hotspots), where he would then **intercept internet traffic**, attempting to **get credit card numbers, usernames & passwords.**

### **Objectives**
- **Find any hacking software**
- **Identify evidence of their use**
- **Recover any data that might have been generated**
- **Attempt to tie the computer to the suspect, G=r=e=g S=c=h=a=r=d=t**

A **DD image** (in seven parts: **1, 2, 3, 4, 5, 6, 7, 8, and notes**) and an **EnCase image** (second part) of the abandoned computer have already been made.
