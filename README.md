# h3 Attaaack

## Chapter 4: Mapping the Adversary

### Introduction

- You can't hunt down threats without first having information about what you are tracking.

- ATT&CK is a Framework. This descriptive model is mainly used to first analyze an attacker capable of breaking into a system and then label the attacker's procedure. 

- ATT&CK has become a standard that both defensive and offensive researchers use to understand each other and also to explain and communicate with people outside the cybersecurity field.

- Framework users can freely create their own set of tactics, techniques and procedures and submit them to the ATT&CK team.

### Tactics

- Each tactic represents the reasoning that led the attacker to use a specific behavior towards the intrusion.

- Currently 14 tactics are defined and used to encompass a group of techniques.

- **Reconnaissance**: Gather as much information about the victim as possible.

- **Resource Development**: This tactic aims to evaluate the enemy's resources. Resources used by the opponent can be bought, stolen or developed.

- **Initial Access**: Descriptions of the attacker's first actions in the victim's environment. 

- **Execution**: Tactics that echo the execution of the malware in the victim.

- **Persistence**: The attacker is able to remain present in the system even after the environment it attacked has been shut down or restarted.

- **Privilege Escalation**: A tactic that consists of entering a system via an account with a low level of privilege and then the attacker tries to obtain higher levels of permission in order to carry out further attacks. 

- **Defense Evasion**: All actions taken by the attacker to avoid detection by the victim. 

- **Credential Access** : Tactic that consists in stealing a user's information (password, login, etc.) from the targeted environment and then impersonating the user. 

- **Discovery** : All the activities that the attacker does to find out as much as possible about the victim.

- **Lateral Movement** : Tactic of analysis of the network configuration by the attacker in order to reach his target.

- **Collection**: Collection of data from the target in order to retrieve it.

- **Command and Control** : Description of all the techniques used by the attacker to communicate with the system.

- **Exfiltration**: Set of techniques used by the attacker to steal the victim's data.

- **Impact**: All the techniques and attempts to prevent the user from accessing and using the data.

- At the time of writing, the author says that there are 183 techniques and more or less 372 sub-techniques.

### The ATT&CK Matrix

- The ATT&CK is a Matrix that allows to have an overview of the different tactics and techniques that concern them.

- This matrix shows in its headers the 14 tactics seen above. Below these headers there are columns containing the different techniques, which in turn when the user clicks on them, they branch out into more sub-techniques.

- We can access to the matrix using clicking [here](https://attack.mitre.org/matrices/enterprise/)

### The ATT&CK Navigator

- It is a tool that allows the visualization of an attacker's modus operandi. It also allows the generation of security exercises using this [web site](https://mitre-attack.github.io/attack-navigator/).

- This tool allows us to create as many layers as we want. Moreover, we can combine the layers in order to study the tools or the actors of the threat.

### Mapping with ATT&CK

- Formbook is an infostealer that was first mentioned in 2016 on a hacking forum. It has been found in attacks against South Korea and the United States. 

- Formbook is used by attackers like SWEED and Cobalt.

- According to researcher Gabriela Nicolao, Forbook is more than just a keylogger. She calls it "browser logger software". This tool can steal information before it reaches the server by bypassing HTTPS encryption. It remains effective even if the user uses a numeric keypad, an autofill system or uses copy and paste.

- Formbook has a monitor that allows its owner to see the victim's stolen information, screenshots and selfie information.

When mapping an attack using the Formbook tool, we can illustrate it as follows :

1. Credential Acess : Steals autification data
- Credentials from Password Stores
- Credentials from Web Browsers
- Input Capture
- Keylogging

2. Collection : Keylog of the victim's information (copy and paste, automatic filling, physical or virtual keyboard)
- Input Capture
- Keylogging

3. Collection : Obtaining information from the victim by taking screenshots
- Screen Capture

## Sources

[Chapter 4: Mapping the Adversary](https://www.oreilly.com/library/view/practical-threat-intelligence/9781838556372/B13376_04_Final_SK_ePub.xhtml#_idParaDest-75)

------------

## MITRE | ATT&CK

### Define tactic and give an example

A tactic represents the set of thoughts and techniques, which the perpetrator of the aggression has implemented to achieve his objective. As mentioned above, there are 14 tactics in the model proposed by the ATT&CK Framework. Each of these tactics is linked to an objective. 

#### Exfiltration

This tactic brings together all the techniques used by attackers to extract data from the victim's environment.

Once the attacker has collected the victim's data, in order not to get caught, he will package/process the data by matching or encrypting it. Often they go as far as deleting stolen data from the victim's environment. After concealing his intrusion, the attacker will focus on extracting this data. To do this, the attacker usually uses a command and control (C2) channel that they have set up between themselves and the infected machines to extract the data stolen from them. They can also use an alternate channel.

### Define technique and subtechnique, and give an example of each

Remaining in the field of information exfiltration, the attacker can implement a technique to automate the exfiltration of data as he collects them.

The attacker can implement sub-techniques in order to optimize his chances of success. Such as using a traffic duplication sub technique. Some network devices have a native feature that is Traffic mirroring. This feature is usually used for network analysis. It can also be used to duplicate data traffic to one or more destinations. 

Therefore, attackers can use this feature to duplicate the network and redirect it to their infrastructures to get the information contained in the flow. This contributes to the automation of data extraction.

### Define procedure, and give an example of each

The procedure is defined by the way the attacker implements the different techniques and sub-techniques to carry out his attack against the victim. A procedure can be concerned one or more techniques and sub-techniques.

If we take the example of an attacker who wants to exfiltrate the data he has collected, he can set up a technique to automate the data transfer in parallel to his collection. To do this, he will set up a traffic duplication in order to redirect the duplicated victim's traffic to his environment by using the Traffic mirroring feature that some network devices have.

## Sources

[MITRE | ATT&CK](https://attack.mitre.org/)

[Exfiltration](https://attack.mitre.org/tactics/TA0010/)

[Automated Exfiltration](https://attack.mitre.org/techniques/T1020/)

[Automated Exfiltration: Traffic Duplication](https://attack.mitre.org/techniques/T1020/001/)
