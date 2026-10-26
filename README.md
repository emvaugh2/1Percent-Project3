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

Welcome to our demonstration of Project 2: Deploying Microservices on Amazon EKS! This will be a compilation of all the skills we've recently developed so lets put in into action. So what is a microservice? A microservice is more of a design approach for breaking very large services into smaller, separated services that add back up to the larger service. Netflix is an "application" but it's really a large application (streaming TV media) that is comprised of a bunch of smaller services (DBs, cloud services, storage, etc). 


## Problem 4: Lack of Documentation and Guidance

Welcome to our demonstration of Project 2: Deploying Microservices on Amazon EKS! This will be a compilation of all the skills we've recently developed so lets put in into action. So what is a microservice? A microservice is more of a design approach for breaking very large services into smaller, separated services that add back up to the larger service. Netflix is an "application" but it's really a large application (streaming TV media) that is comprised of a bunch of smaller services (DBs, cloud services, storage, etc). 



## Problem 5: Integration of CI/CD Practices

Welcome to our demonstration of Project 2: Deploying Microservices on Amazon EKS! This will be a compilation of all the skills we've recently developed so lets put in into action. So what is a microservice? A microservice is more of a design approach for breaking very large services into smaller, separated services that add back up to the larger service. Netflix is an "application" but it's really a large application (streaming TV media) that is comprised of a bunch of smaller services (DBs, cloud services, storage, etc). 
