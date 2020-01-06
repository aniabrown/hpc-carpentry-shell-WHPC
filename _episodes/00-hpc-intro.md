---
title: "Why Use a Cluster?"
teaching: 15
exercises: 5
questions:
- "Why would I be interested in High Performance Computing (HPC)?"
- "What can I expect to learn from this course?"
objectives:
- "Be able to describe what an HPC system is"
- "Identify how an HPC system could benefit you."  
keypoints:
- "High Performance Computing (HPC) typically involves connecting to very large computing systems
  elsewhere in the world."
- "These other systems can be used to do work that would either be impossible or much slower or
  smaller systems."
- "The standard method of interacting with such systems is via a command line interface called
  Bash."
---



{% include figure.html url="" max-width="20%" 
file="/fig/serverrack-openclipartorg-psteinb-basedon-ericlemerdy.svg" alt="A rack with servers"
caption="" %}

The methodology of providing the input data, communicating options and flags as well as retrieving
the results is quite opposite to using a plain laptop. Moreover, using a GUI style interface is 
often discarded in favor of using the command line. This imposes a double paradigm shift for 
prospect users:

1. they work with the command line (not a GUI style user interface)
2. they work with a distributed set of computers (called nodes)

> ## I've never used a server, have I?
> 
> Take a minute and think about which of your daily interactions with a computer may require a 
> remote server or even cluster to provide you with results. 
{: .challenge }
