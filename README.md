# Flack

Flack is a slack-like system.

1) The top-level description of the proposed architecture (figure 1):

Flack implements a client-server architecture where clients (mobile, desktop, web and apps) communicate with two backend systems:
 - web servers that handle HTTP request/response cycles and interact with other systems such as underlying databases and job queues.
 - messaging servers that send messages, profile changes, user activity updates and other events.
 
This is implemented as a Three-tier Client Server Architecture.
 
 Figure 1
 
 ![Figure 1](https://github.com/JulianaYo/Flack/blob/main/system.png?raw=true)

Client-server architecture is an architecture of a computer network in which many clients (remote processors) request and receive service from a centralized server (host computer). Client computers provide an interface to allow a computer user to request services of the server and to display the results the server returns. Servers wait for requests to arrive from clients and then respond to them. Ideally, a server provides a standardized transparent interface to clients so that clients need not be aware of the specifics of the system (i.e., the hardware and software) that is providing the service. Clients are often situated at workstations or on personal computers, while servers are located elsewhere on the network, usually on more powerful machines. This computing model is especially effective when clients and the server each have distinct tasks that they routinely perform. In hospital data processing, for example, a client computer can be running an application program for entering patient information while the server computer is running another program that manages the database in which the information is permanently stored. Many clients can access the server’s information simultaneously, and, at the same time, a client computer can perform other tasks, such as sending e-mail. 

2) The detailed description of each architecture element.

When a new message posted in a group it is sent via an API call to the web servers, where it is sent to the message servers and is stored in the database. The messaging servers receive these new messages and send them to connected clients over web sockets to all users in the group.

In Flack system the client is the layer which interacts with the user. It is a web interface which has a GUI. On the image Figure 1 it is green icon with people. It can be implemented as mobile, desktop or web application. 

In the Three-tier Client Server Architecture concept it is a presentation layer.

The Web Application Backend is a layer which is called App Tier (Tier 2) and it is responsible for business logic of the application. The first tier Client communicate with the this secont layer via Web Api.

The third Tier layer is a message server and database. It is a resource manager that stores data. The Web Application Backend interacts directly with the Database  when it need to add/remove new users, channels, groups. When users send messages it goes through the message server which makes sql queries to the database.
