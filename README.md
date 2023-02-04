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

### Procedure

- The procedure is defined by the way the attacker implements the different techniques and sub-techniques to carry out his attack against the victim. 
- A procedure can be concerned one or more techniques and sub-techniques.

### The ATT&CK Matrix

- The ATT&CK is a Matrix that allows to have an overview of the different tactics and techniques that concern them.

- This matrix shows in its headers the 14 tactics seen above. Below these headers there are columns containing the different techniques, which in turn when the user clicks on them, they branch out into more sub-techniques.

- We can access to the matrix using clicking [here](https://attack.mitre.org/matrices/enterprise/)

### The ATT&CK Navigator

- It is a tool that allows the visualization of an attacker's modus operandi. It also allows the generation of security exercises using this [web site](https://mitre-attack.github.io/attack-navigator/).

- Cet outil nous permet de créer autant de couche que l'on souhaite. De plus nous pouvons combiner les couches afin d'étudier les outils ou les acteurs de la menaces.

