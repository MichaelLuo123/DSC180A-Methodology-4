---
layout: default
title: DSC 180A Methodology Assignment 4
---

# DSC 180A Methodology Assignment 4

**Name:** Michael Luo  
**UCSD Email:** m6luo@ucsd.edu  
**Section:** D33 - Safe Agentic AI  
**Mentor:** Babak Salimi

## Quarter 2 Project Reflection

**1. What is the most interesting topic covered in your domain this quarter?**

The most interesting topic to me has been how prompt injection can cause problems across several steps instead of one obvious bad command. A coding agent might read an untrusted file, change a setting, and later run something that depends on that setting. Looking at each step on its own can make the behavior seem normal. I like this topic because it gives us a way to trace how an attack actually works, rather than just looking at the final result.

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

I'd like to test whether an AI monitor can tell the difference between a dangerous change that stays in place and a temporary change made for testing and then reversed. I could build a few small Python projects with matched examples of both situations and see how often a monitor catches real problems versus flags harmless ones. I think this would be useful because a monitor that raises an alarm for everything would be hard to trust, even if it catches most attacks.

**3. What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

One thing I'd change is how we evaluate the monitor. In our current work, we've seen cases where it identifies what the code does correctly but still reaches the wrong conclusion about whether that behavior violates a policy. Instead of grading only its final decision, I'd check the facts it found, the evidence it used, and its policy judgment separately. That would help us figure out whether a mistake came from missing information or from the monitor's reasoning.

**4. What other techniques would you be interested in using in your project?**

I'd be interested in using static analysis to track which functions and settings affect a security-sensitive operation, along with small tests to check what the code actually executes. I also want to try giving the monitor shorter summaries instead of full action logs to see what information it really needs. I'd measure false alarms as well as missed attacks, since both would matter if a monitor were used on a real project.
