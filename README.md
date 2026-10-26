## AWS Cloud Engineer

**Greetings! We'll be going over the tasks for Week 7 - Project 3 of the Cloud Engineering program. Lets get started!**

## Week 7 - Project 3: Discussion Topics
* Problem 1: Data Source Variability
* Problem 2: Proactive Monitoring and Observability
* Problem 3: Resource Constraints
* Problem 4: Lack of Documentation and Guidance
* Problem 5: Integration of CI/CD Practices

________________________

## Problem 1: Data Source Variability

1. **Research and Think:**
- Having different data formats can cause issues by making data cleaning and pulling the data more difficult. You can have multiple ways to list a date: 07/22/1993, July 22nd, 1993, 07-22-1993, 07.22.93. All of these are different formats and if you have applications or systems that are accepting one specific format, it will break those systems. From my networking experience, you see this often with MAC address as they'll be listed in the xx:yy:zz, xx-yy-xx, xxyy.zz formats. Some Cisco systems are smart enough to pull the data but others aren't (like the WLCs). By standardizing the format, you can make the data cleaning and pulling process acceptable for multiple systems. Think of it like defining a protocol. 

2. **Create a Common Data Format:**
- Lets reuse the date format. To make it globally acceptable, lets standardize the format to be DD-MM-YYYY. In America, we usually do month, date and year but the rest of the world does date, month, and year. Lets be fair here. I personally don't think this is a big change to present to other teams. I believe they would gladly accept it. Worse case scenario, I could create a simple AI script with a button that will take their preferred date description and change it to the acceptable format. 

3. **Communication Plan:**
- We would have a meeting with the other teams to present this game plan. I'd take feedback from them to see what issues or concerns they have to refine my own plan. Lastly, I would document our process so everyone has a good reference point on how the procedures should be done. This doesn't have to be the end-all-be-all for the data format. We can allow time in the next 6 months to revisit the plan to see if it works for everybody as well. 


## Problem 2: Proactive Monitoring and Observability


1. **Identify Important Metrics:**
    - The general metrics for most computer systems are the hardware resources such as CPU, RAM, and disk space. If we're talking about networking, important metrics are high bandwidth utilizations, neighbor down alerts, failed backup jobs, etc. For the cloud, one of the most important metrics are costs. All of these are problems you want to catch early because it will show that your virtual environment is about to collapse if the hardware resources are overused, the network may fail if a neighbor is down, and you can run your company out of business if cloud costs skyrocket out of budget. 
2. **Suggest Monitoring Strategies:**
    - The easiest way to be proactive about monitoring is having dedicated systems in place to monitor these resources. For Linux machines which most environments run on, you can use a tool like Zabbix that will send email alerts when hardware resources are overutilized. For networking, there are plenty of systems that can show you which network nodes are up, down, circuit information, APs, etc. I'm personally familiar with Solarwinds and PTRG. It takes a lot to configure it upfront but once you're established, you can see alerting very quickly. Lastly, for the cloud, there are security policies and cost guardrails that you can put in place to make sure the spending doesn't balloon. 
3. **Feedback Process:**
    - Once you know which metrics to track, the next biggest concern is how quickly the alerts are happening and whether they're true or false alarms. Some systems report faster than others so the quicker the service can capture an issue, the better the monitoring is working. There should also be a process to address alerts as they come in. There should be formal reviews to measure the effectiveness of the monitoring system as well. 

## Problem 3: Resource Constraints

**Explanation:** The team is small, so members often have to do many tasks. This can lead to stress and gaps in coverage.

**Action Steps:**

1. **Assess Team Roles:**
    - Think about the current roles and responsibilities in a small team. Identify areas where team members might be overwhelmed and write a brief analysis.
2. **Resource Management Ideas:**
    - Suggest ways to better manage resources, like prioritizing tasks or sharing responsibilities. Consider how cross-training team members could help.
3. **Automation Opportunities:**
    - Think about simple tasks that could be automated to save time. Write a proposal for tools or processes that could make work easier.
  
1. **Assess Team Roles:**
    - Most teams (at least when they're contractors) have a scope of work regarding the responsbilities and boundaries for what the employee should be handling. The manager and directors should know this like the back of their hand. As far as the cloud and networking sides are related, this typically comes down to handling alerts first, tickets from end users, large projects to fix and refresh the environment, and future designing activities which the architect usually handles. People can easily get overwhelmed by tickets and alerts if the environment isn't very stable which requires high availibility, redundancy, simple, efficient topology designs, and proper training to handle issues. 
2. **Resource Management Ideas:**
    - The junior level engineers should handle as many tickets as they can and work on smaller projects. The senior engineers should work on the main projects to uphold stakeholder deliverables. The architect should be making environment design choices as they're usually the most senior and understands every part of the network. There should be biweekly training for everyone on the team by the team or additional resources so that there are no silos of information on the team. 
3. **Automation Opportunities:**
    - Automation comes in many forms but here are few things that would make some environments easier. You can create an automatically messaging system that sends ticket cases to ISPs when a network neighbor goes down so the ISP can immediately fix the circuit on their end. You can create scripts for device configurations so engineers can copy and paste the configuration instead of writing the syntax from scratch. There should be clear documentation with all procedures and stored in a logical way where people can find the documentation. That way, the junior engineers can review these documents and solve problems before reaching out to the more senior engineers. This is very environment specific but those are a few things I could automate. 


## Problem 4: Lack of Documentation and Guidance

**Explanation:** Not having enough documentation can make it hard for new members to onboard and slow down the work process.


1. **Evaluate Documentation:**
    - Look at the current state of documentation in a team. Write a brief analysis of how poor documentation affects team performance.
2. **Improvement Plan:**
    - Suggest simple strategies for creating and keeping documentation up to date. This could include assigning responsibilities or setting regular review times.
3. **Encourage Knowledge Sharing:**
    - Think of ways to encourage team members to share what they know. Propose ideas like lunch-and-learn sessions or regular meetings to share knowledge.
  

1. **Evaluate Documentation:**
    - Documentation is one of those huge factors that people overlook all the time until things become very hectic. Also, what's the best way to document a process? People aren't really holding seminars on how to do this. Consider a senior engineer who has been with the company since the day it started. They know parts of the environment that you may never run across. When they disappear and an issue arises, it becomes extremely difficult to fix certain issues which can cost the company money, future business, or overall destroy the company. This is a very real reality so people should have processes documented to avoid catastrophes. 
2. **Improvement Plan:**
    - One of the best ways to create documentation is when you're starting a new process or task, take as many notes as you can with screenshots of the process while you're going through it. When you revist the issue, it's easy to forget about the small buttons and commands you put in while getting to the solution and you may not even run into that issue again so you'll forget about all of these small steps. Write all of it down as you go through it so the next person will have even more information and will be able to follow along. Visual information helps tremendously. If you can, always try to create diagrams for workflows whether that's a logical workflow, traffic workflow, or operational workflow. This can literally save the day when people run into issues with applications. Documentation should be stored in a place where people can easily search for it. At the very least, the engineer who wrote the documentation should be able to show the location of the document quickly. 
3. **Encourage Knowledge Sharing:**
    - Documentation should be updated regularly because GUIs for a many tools change slightly but constantly. A screenshot from a documentation 7 months ago may no longer be relevant in today's procedure since the screen looks different. There should be meetings once a month for team members to show other team members their documentation and make sure no one has any questions about it. You can encourage this behavior because it will remind all the engineers that if they want less work or less people to reach out to them for a specific issue, they should create the documentation for it so other engineers can handle it without assistance. Bonus points if the engineer is so great at documentation that they can hand this to an end user the and end user fix it themselves. 



## Problem 5: Integration of CI/CD Practices

Welcome to our demonstration of Project 2: Deploying Microservices on Amazon EKS! This will be a compilation of all the skills we've recently developed so lets put in into action. So what is a microservice? A microservice is more of a design approach for breaking very large services into smaller, separated services that add back up to the larger service. Netflix is an "application" but it's really a large application (streaming TV media) that is comprised of a bunch of smaller services (DBs, cloud services, storage, etc). 
