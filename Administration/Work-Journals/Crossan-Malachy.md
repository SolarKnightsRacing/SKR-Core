---
firstname: Malachy
lastname: Crossan
phone: 3213324383
email: malachycrossan@gmail.com
github: malachycrossan
discord: malachy_c
NID: ma378458
linkedin: www.linkedin.com/in/malachycrossan
---

# Crossan Malachy
## Todo
- [ ] I need to add DFM learning resources to the SKR-Resources repo 
## 2025-07-11
### Digital Ocean Virtual Machine (droplet)
- Marketplace image called "Docker on Ubuntu 22.04"
- Used a docker-compose.yaml file to set up gitlab
- This video explains how to use nginx: https://youtu.be/BeafoOFxIcI?si=XNlmpyMof_q3ZMyF


## 2025-07-10
### Cloudflare domain registration
I registered 'solarknightsracing.org' through cloudflare for 7.50 USD for one year. The price will increase to 10.25 USD for the years following. I chose cloudflare because it seemed like an established company to register through. I created the account with solarknightsracing@gmail.com.

I plan to temporarily set solarknightsracing.org and www.solarknightsracing.org to redirect to the wix or squarespace site that aaron made.

```
# Domain:     solarknightsracing.org.
# Exported:   2025-07-11 22:07:29
solarknightsracing.org	3600	IN	SOA	nadia.ns.cloudflare.com. dns.cloudflare.com. 2050393824 10000 2400 604800 3600

# NS Records
solarknightsracing.org.	86400	IN	NS	nadia.ns.cloudflare.com.
solarknightsracing.org.	86400	IN	NS	piotr.ns.cloudflare.com.

# A Records
finance.solarknightsracing.org.	1	IN	A	134.199.192.110 ; cf_tags=cf-proxied:true
git.solarknightsracing.org.	1	IN	A	134.199.192.110 ; cf_tags=cf-proxied:true
solarknightsracing.org.	1	IN	A	134.199.192.110 ; cf_tags=cf-proxied:true
www.solarknightsracing.org.	1	IN	A	134.199.192.110 ; cf_tags=cf-proxied:true
```

### Digital Ocean
Ubuntu droplet for GitLab server, big capital instance, Website, and cloud storage


## 2025-07-06
### Digital Ocean

## 2025-07-04
### PDM
I looked into a bunch of different PDM softwares and I have determined that they are a bit overkill. I think if I set up the GitLab well we will be chilling.

### Updated meeting Schedule (subject to change)
Design Meeting | Sunday    | 2:45pm - 7:00pm
Design Meeting | Monday    | 4:30pm - 7:30pm
Design Meeting | Tuesday   | 4:00pm - 8:30pm
General Body   | Wednesday | 4:30pm - 6:00pm
Design Meeting | Wednesday | 6:00pm - 8:30pm
Design Meeting | Thursday  | 4:00pm - 8:30pm

## 2025-06-27
- Drafted PVF and sent it to putnam
- Uploaded the empty form and template to SKR-Core

## 2025-06-26
- Messaged FSGP Coordinator
- joined the CECS RSO Leadership discord
- Talked to CECS about GitLab server. They said to go through advisor

### Email from QS Motor
- Email received from QS motor. Gave us engineering drawings and information about the motor.
- [ ] Reply email QS motor
  - Shipping information
  - Ask for spare rotors
  - talk to Adam about brakes

### PVF
I tried to get my Tuesday absence excused with my CS professor and I required a Program Verification Form (PVF). It is not that complicated. It just requires some information about the event and a signature from the faculty advisor (Dr. Putnam)

### Discussed BPS with Nick
Decided on using a micro-controller development board along with a custom pcb. The BPS should go within the battery enclosure. 

## 2025-06-25
- Design meeting
- Azure revoked

## 2025-06-24
- Communicated with Gail the IEF coordinator and requested emergency contact forms from team
- Added FSGP docs to Repo
- Edited Connors CECS announcement
- [ ] (Waiting on review from Connor) send CECS server announcement 

Omar spaghettafied the git history for 1_solaris last night so I need to fix that. We discussed making it more streamlined last night by implementing a feature that forces linear commit history, Auto-pull, and Auto-stage features somehow. I also told Naveen that the git feels like it is hurting more than it is helping right now so I will prioritize that in the next week.

## 2025-06-19
- [x] FSGP2025 announcement
- [x] FSGP Registration Begun
- [ ]  

## 2025-06-18

## 2025-06-13
Today Naveen and I worked on the CAD for the battery. I was trying to model the cell holding bracket in a way that was parametric and configurable but it proved to be not worth the time. Might just be a skill issue.

I want to self-manage our git repo next year. I'll try to do it through CECS. I opened an issue (#5) for it in SKR-Core.

I was messing around with the git-gui that ships with windows and you can add custom tools. These tools can take in arguments like text, revisions, or files (if you select the diff). They show up in a drop down in the top bar but I haven't found a way to download or upload a configuration yet. These tools might be able to fill the gap in the git workflows for terminal-phobic folks.

Double clicking on an path in the output window conveniently highlights the relative path needed for the lock and unlock commands. So, `[Show Locked / Show All] -> double click -> copy -> [Lock / Unlock]` is a pretty frictionless workflow.

```
Note: "Show Locked" command that displays all currently locked files. 
Name: Show Locked
Command: git lfs locks

Note: "Show all" command that displays all files that can be locked
Name: Show All
Command: git lfs ls-files

Note: "Lock" command that takes in a file path relative to the root directory (e.g. SKR-Core)
Name: Lock
Command: git lfs lock $ARGS

Note: "Unlock" command that takes in a file path relative to the root directory (e.g. SKR-Core)
Name: Unlock
Command: git lfs unlock $ARGS
```

I was wrong when I said that the best way to create a new version is by copying the file. The better way is to lock the original file with lfs then open it so that SolidWorks doesn't open in that weird read only state. Then do whatever work needs to be done before you can determine the significance of the change (MAJOR, MINOR, PATCH).
Then save that new version. commit and push the new file. then unlock the original.

- [ ] Finish ADR0008&9
- [ ] Help Jonah get started with MPPTs
- [X] Create READMEs for all parts

## 2025-06-12
Today was my first time using the new Part numbering, versioning, and naming schema. There was a bit of friction because I could only go off numbers rather than descriptions. I don't know if that was the best choice.

I ported all of Naveen's battery CAD to the new schema. Then, I fixed the dimensions on his 18650 Cell.

I think I am going to redo some of the battery CAD. Naveen did a great job but some of the modeling isn't quite idiomatic and the assemblies lack any mates.

CAD Idiomatic design notes:
- Parts should be centered about the origin
- Parts should be bisected by primitive planes (Front, Right, Top)
- Sketches should be fully defined
- Sketches, Part, and Assemblies should be parametrically designed if possible
- If parametric design isn't possible or practical should be designed in a way that is modifiable
- Design For Manufacture (DFM) should always be on your mind


- [x] Reorganize battery CAD
- [x] Create READMEs for each new part

## 2025-06-11
- [x] Meeting with Dr. Stark (RESCHEDULED)
- [x] Made work journals
- [x] Create master Bill of Materials
- [x] Reorganize battery CAD (WIP)
- [x] Decided on using 18650 Cells



The following is from before I started keeping this work journal.
## June
## May
## April
## March
## February
## January
