---
toc: true
comments: true
layout: post
title: Computers and Networks (Unit 4)
description: Add Definitions from Unit 4 Computer Systems and Networks
---
## Requirements
> Work through College Board Unit 4... blog, add definitions, and pictures.  Be creative, for instance make a story of Computing and Networks that is related to your PBL experiences this year.


### How a Computer Works
> As we have learned, a computer needs aa program to do something smart.  The sequence of a program initiates a series of actions with the computers Central Processing Unit (CPU). This component is essentially a binary machine focussing on program instructions provided.  The CPU retrieives and stores the data it acts upon in Random Access Memory (RAM). Between the CPU, RAM, and Storage Devices a computer can work with many programs and large amounts of data.

List specification of your Computer, or Computers if working as Pair/Trio
- Processor GHz: Processor	Intel(R) Core(TM) i7-3517U CPU @ 1.90GHz, 2401 Mhz, 2 Core(s), 4 Logical Processor(s)
- Memory in GB: 8.00 GB
- Storage in GB: 237 GB
- OS: OS Name	Microsoft Windows 10 Pro

Define or describe usage of Computer using Computer Programs. Pictures are preferred over a lot of text.  Use your experience.
- Input devices
- Output devices
- Program File
- Program Code
- Processes
- Ports
- Data File
- Inspect Running Code
- Inspect Variables

![](https://github.com/kayleehou/myproject/blob/master/images/cpu_usage_mindmap.PNG?raw=true)

![Computer Hardware]({{site.baseurl}}/images/cpu.jpeg)


### The Internet
> Watch/review College Board Daily Video for 4.1.1

- Essential Knowledge
    - A computing device is a physical artifact that can run a program. Some examples include computers, tablets, servers, routers, and smart sensors.
    - A computing system is a group of computing devices and programs working together for a common purpose.
    - A computer network is a group of interconnected computing devices capable of sending or receiving data.
    - A computer network is a type of computing system. 
    - A path between two computing devices on a computer network (a sender and a receiver) is a sequence of directly connected computing devices that begins at the sender and ends at the receiver.
    - Routing is the process of finding a path from sender to receiver.
    - The bandwidth of a computer network is the maximum amount of data that can be sent in a fixed amount of time.
    - Bandwidth is usually measured in bits per second

- Complete Vocabulary Matching Activity.  Incorporate this into your learnings from year.  To analyze measure path and latency use `traceroute` and `ping` commands from Linux Terminal.  
    - Path - a
    - Route - e
    - Computer System - b
    - Computer Device - c
    - Bandwidth - d
    - Computer Network - f

> Watch/review College Board Daily Video 4.1.2

- Complete True of False Questions

1. T
2. F
3. F
4. T
5. F
6. T  correct answer: F
7. T

- Essential Knowledge
    - The internet is a computer network consisting of interconnected networks that use standardized, open (nonproprierary) communication protocols.
    - Access to the internet depends on the ability to connect a computing device to an internet connected device.
    - A protocol is an agreed-upon set of rules that specify the behavior of a system.
    - The protocols used in the internet are open, which allows users to easily connect additional computing devices to the internet.
    - Routing on the internet is usually dynamic; it is not specified in advance
    - The scalability of a system is the capacity for the system to change in size and scale to meet new demands.
    - The internet was designed to be scalable
    - Information is passed through the internet as a data stream. Data streams contain chunks of data, which are encapsulated in packets. 
    - Packets contain a chunk of data and metadata used for routing the packet between the origin and the destination on the internet, as well as for data reassembly.
    - Packets may arrive at the destination in order, out of order, or not at all
    - IP, TCP and UDP are common protocols used on the internet.
    - The world wide web is a system of linked pages, programs, and files.
    - HTTP is a protocol used by the world wide web
    - The world wide web uses the internet

- Go over AP videos, vocabulary, and essential knowledge.  Draw a diagram showing the internet and its many levels. A preferred diagram would using your knowledge of frontend, backend, deployment, etc.  Picture would highligh vocabulary by illustration. The below illustration have some ideas

![Full Stack]({{site.baseurl}}/images/fullstack.png)

![network topology](https://github.com/kayleehou/myproject/blob/master/images/network_topology.PNG?raw=true)

![internet layers](https://github.com/kayleehou/myproject/blob/master/images/internet_layers.PNG?raw=true)

- Often we draw pictures of machines communicating over the Internet with arrows.  However, the real communication goes through protocol layers and the machine and then is trasported of the network.   For College Board and future Computer Knowledge you should become familiar with the following ...

```
     User Machine  <---> Frontend Server <---> Backend Server
    +-----------+         +-----------+         +-----------+
    |  Browser  |         |  GH Page  |         |   Flask   |
    +-----------+    ^    +-----------+    ^    +-----------+
    |    HTTP   |    |    |    HTTP   |    |    |    HTTP   |
    +-----------+    |    +-----------+    |    +-----------+
    |    TCP    |    |    |    TCP    |    |    |    TCP    |   
    +-----------+    |    +-----------+    |    +-----------+
    |     IP    |    V    |     IP    |    V    |     IP    |
    +-----------+         +-----------+         +-----------+
    |  Network  |  <--->  |  Network  |  <--->  |  Network  |
    +-----------+         +-----------+         +-----------+
```

The "http" layer is an application layer protocol in the TCP/IP stack, used for ***communication between web browsers and web servers***. It is the protocol used for transmitting data over the World Wide Web.

The "transport" layer (TCP) is responsible for providing reliable data transfer between applications running on different hosts.  The TCP protocol segments the data into smaller ***chunks called "segments"***. Each segment contains a sequence number that identifies its position in the original stream of data, as well as other control information such as source and destination port numbers, and checksums for error detection.

The "ip" layer is responsible for packetizing data received from the TCP layer of the protocol stack, and then ***encapsulating the data into IP packets***. The IP packets are then sent to the lower layers of the protocol stack for transmission over the network.

The "network" layer is responsible for ***routing data packets between networks*** using the Internet Protocol (IP). This layer handles tasks such as packet addressing and routing, fragmentation and reassembly, and ***network congestion*** control.


### Fault Tolerance
> Watch both Daily videos for 4.2

- Complete the network activity, summarize your understanding of fault tolerance.
1. yes, it is fault tolerant, even if one path goes down, you can communicate with the other ones 
2. no, only one path to F, so if one wire goes down, F is also cut off 
3. no, only one wire connecting A and G 

4.2 video 2 practice: 
1. C
2. A 

- the internet is fault tolerant 
Network where devices can communicate with one another even if one path goes down. It's important to have redundancy in your network, so that if one wire goes down, the other devices can still function because there is more than one path between connected devices. 

### Parallel and Distributed Computing
> Review previous lecture on Parallel Computing and watch Daily video 4.3. Think of ways to make something in you team project to utilize Cores more effectively.  Here are some thoughts to add to your story of Computers and Networks...
- load balancing with an API 

- What is naturally Distributed in Frontend/Backend architecture?  
The backend is naturally distributed as it typically consists of multiple servers, each responsible for handling different tasks or services. By distributing the backend, the application can handle a large number of requests, improve performance and reliability, and provide fault tolerance and high availability. The frontend, on the other hand, is typically executed on a single client device, such as a web browser or mobile app, and is responsible for displaying the user interface and interacting with the user.

- Analyze this command in Docker: ```ENV GUNICORN_CMD_ARGS="--workers=1 --bind=0.0.0.0:8086"```.   Determine if there is options are options in this command for parallel computing within the server that runs python/gunicorn.  Here is an [article](https://medium.com/building-the-system/gunicorn-3-means-of-concurrency-efbb547674b7)

In the context of a Docker image that runs a Python/Gunicorn web application, this command is used to configure the Gunicorn web server. The --workers option specifies the number of worker processes that Gunicorn should spawn to handle incoming requests. In this case, the value is set to 1, which means that Gunicorn will use a single worker process to handle all requests. The --bind option specifies the IP address and port number that Gunicorn should bind to, in this case, 0.0.0.0:8086, which means that Gunicorn will listen on all network interfaces on port 8086.

To enable parallel computing in Python/Gunicorn web application, you can adjust the --workers option to a higher value, which will spawn multiple worker processes to handle incoming requests concurrently. However, increasing the number of worker processes may also increase the memory usage and CPU load of the server.

- CHALLENGE: seek how many workers I have set up on gunicorn and set up more
I think there are currently 4 workers on gunicorn, I can run gunicorn myapp:app -w 8
to set up more. 

> Last week we discussed parallel computing on local machine.  There are many options.  Here is something to get parallel computing work with a tool called Ray.
- Review this [article](https://www.anyscale.com/blog/writing-your-first-distributed-python-application-with-ray)...  Can you get parallel code on images to work more effectively?  I have not tried Ray.
Ray is a distributed computing system that makes it easy to write parallel and distributed Python applications. It is designed to be efficient and scalable, and can help you parallelize your code across multiple CPU cores, GPUs, or even multiple machines.

- Code example from ChatGPT using squares.  This might be more interesting if nums we generated to be a lot bigger.

```python
import ray

# define a simple function that takes a number and returns its square
def square(x):
    return x * x

# initialize Ray
ray.init()

# create a remote function that squares a list of numbers in parallel
@ray.remote
def square_list(nums):
    return [square(num) for num in nums]

# define a list of numbers to square
nums = [1, 2, 3, 4, 5]

# split the list into two parts
split_idx = len(nums) // 2
part1, part2 = nums[:split_idx], nums[split_idx:]

# call the remote function in parallel on the two parts
part1_result = square_list.remote(part1)
part2_result = square_list.remote(part2)

# get the results and combine them
result = ray.get(part1_result) + ray.get(part2_result)

# print the result
print(result)

```
