**Hello everyone**,

Welcome to my Research Repository. For the past semester (2023 Spring), I had the fantastic opportunity to do research with Professor Srinivas Narayana Ganapathy on "Designing Fast Internet Services." If you want you can skip to the end for the conclusion for a quick TLDR.

In this repository, I sorted my work into "days" where each folder contains a specific task to learn more about the inner workings of certain technologies (like Docker) and more. The assignments were sometimes one week, but some spanned a few weeks. It is noted that I also worked/learned more than what is shown in this repository.

Another thing to note is that some of the files are in .rtf form, which Github does not process as nicely, so I apologize in advance.

In the first one to two weeks, I was asked to read some articles and some research papers.
Kubernetes vs Docker: https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/kubernetes-vs-docker/
Borg, Omega, and Kubernetes by BRENDAN BURNS, BRIAN GRANT, DAVID OPPENHEIMER, ERIC BREWER, AND JOHN WILKES
An Open-Source Benchmark Suite for Microservices and Their Hardware-Software Implications for Cloud & Edge Systems by Cornell University
In these papers, I learned a great deal about the differences between Kubernetes and Docker, a bit of backstory of containers, and some of the network implications of specific technologies. Professor and I discussed these readings, and Professor answered all my questions about them.

One day1, I was tasked to run an NGINX server locally and then run an NGINX server within a container. After some config issues with VirtualBox, I could download Linux on my machine and did this task in a few days. In this case, I learned some fundamental commands used in Linux and Docker. It was my first time using Docker, which is a milestone.

On day2, I was asked to do two things: Start a Kubernetes cluster with a pod running with an NGINX container running inside (part 1) and then another (client) container within the same pod to communicate with the NGINX container (part 2). In total, there should be two containers with the pod, and they should be able to communicate. This task was a bit hard because I faced many issues in getting the pod (in part 1) to start. I used Kind, a tool for running local Kubernetes clusters using Docker container "nodes," and it was the only tool that would work on my machine. My pod status would always showcase an error such as "ImagePullBackOff," which, to this day, still haunts me. After much time trying to figure it out alone, I contacted one of the grad students, who graciously pointed me in the right direction on how to fix this issue. To resolve this issue, I tinkered with my .yaml files and dug deep into what a .yaml file truly is. On top of this, I learned about Kind through documentation which, combined with my new knowledge of yaml files, I could start my pod successfully. I could only finish this after my weekly meeting with my Professor for this assignment; however, through our meeting, Professor Narayana guided me on what I needed to complete this task. By the end of this meeting, I was able to complete this task.

On day3, I watched and studied two videos (I also read some documentation and websites listed in day3 .rtf), created two pods within the same node, and understood the inner workings of these two pods that can talk to each other. Jérôme Petazzoni gave the two videos (found in day3) that I watched, and he discussed some of the concepts of Kubernetes/docker and Linux. I had a tough time understanding Linux in things such as cgroups and namespaces, so I especially spent much time learning about the fundamentals of Linux.

Next, on day5 I took my knowledge from day3 into practice. Analogous to day2 but slightly different, I was asked to create two pods within the same node, an NGINX server and a Client of my choosing, and allow them to communicate. Specifically, I learned about Services and tinkered with the .yaml files in the process. Soon, after some trial and error, I was able to complete this task.

For the next task (day6), I was assigned to do the same thing as day5, but the pods would be on different nodes. I faced huge issues with Kind, making this task difficult. Because I could not do too much, I stuck to learning more about Pod-Pod communication on different nodes using online resources and through my meetings with Professor. In the following assignment (day7), I performed the same task on day 6 but used MiniKube rather than Kind. Instead of using VirtualBox, I downloaded Docker and Minikube on my machine and performed the tests needed for this assignment. Everything worked very smoothly.

Finally, on day8-9, I was assigned the biggest assignment yet. I would the same thing as day5 and day6, but I would have to do it "manually", in the sense that I would be using kubeadm. My first few attempts were not working correctly as I unknowingly missed many crucial steps such as commands regarding the IP tables. As a result, I researched a lot about the inner workings of Kubernetes/Docker and watched videos regarding kubeadm. Therefore, after many failures, I finally completed this assignment using Kubeadm and CloudLabs (2 seperate machines for each node).

In conclusion, research with Professor Narayana was an exhilarating experience. I learned extensive information about Kubernetes/Docker and their underlying components! I'm very thankful to Professor Narayana for supporting me on this adventure by helping me when I would get stuck and, of course, I am grateful for this wonderful opportunity.

THANK YOU FOR STOPPING BY!
