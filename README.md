# Flack

Flack is a slack-like system.

The top-level description of the proposed architecture (figure 1):

Flack implements a client-server architecture where clients (mobile, desktop, web and apps) communicate with two backend systems:
 - web servers that handle HTTP request/response cycles and interact with other systems such as underlying databases and job queues.
 - messaging servers that send messages, profile changes, user activity updates and other events.
 
 Figure 1

Client-server architecture is an architecture of a computer network in which many clients (remote processors) request and receive service from a centralized server (host computer). Client computers provide an interface to allow a computer user to request services of the server and to display the results the server returns. Servers wait for requests to arrive from clients and then respond to them. Ideally, a server provides a standardized transparent interface to clients so that clients need not be aware of the specifics of the system (i.e., the hardware and software) that is providing the service. Clients are often situated at workstations or on personal computers, while servers are located elsewhere on the network, usually on more powerful machines. This computing model is especially effective when clients and the server each have distinct tasks that they routinely perform. In hospital data processing, for example, a client computer can be running an application program for entering patient information while the server computer is running another program that manages the database in which the information is permanently stored. Many clients can access the server’s information simultaneously, and, at the same time, a client computer can perform other tasks, such as sending e-mail. 

