# 2023 ACS Athens Incubator Summit - C2C Demonistration

## Introduction

The **ACS Athens Incubator Innovation Summit**  is an event where student representatives of other schools come together to share their passion expressed through engaging workshop presentations to existing ACS Athens students.

As an ACS Athens student representative, I had the opportunity to 𝗱𝗲𝘀𝗶𝗴𝗻 𝗮𝗻𝗱 𝗽𝗿𝗲𝘀𝗲𝗻𝘁 an interactive workshop on the **importance of cybersecurity** in today’s digital world.

To make the session engaging for a younger audience, I developed:
- ▶️ A **slideshow presentation** introducing key cybersecurity concepts and their impact in today's digital world.
- 💻 A **custom built command-and-control (C2) server and client** that allowed students to experience the dynamics between an attacker and a victim in a controlled, educational environment.

During the activity, one of the students pretended to be the victim, needing to complete computer-based tasks. The other student used the C2 client, acting as the attacker and took part in disrupting the progress of the victim. The exercise gave students hands-on insight into how cyberattacks work, and why cybersecurity awareness is crucial.


## Architecture

The command and control server is based on the client-server architecture. For client-server communication, TCP is used, as it allows for the creation of a single, persistent connection between the server and client, which is all that is required for demonstration purposes.

In the case of this C2 system, the server runs on the victim's machine, while the client runs on the attacker's machine. As this is a controlled environment, the firewall on the victim's machine can be configured in such a way that it allows connections from any client.


## Programming Languages Used

The language of choice for the server is Go. This is because it can be compiled into a single executable for any platform, and it is relatively easy to implement TCP networking, start processes, and use the Windows API for certain functionality without the requirement of boilerplate code.

For the client, The Electron JavaScript framework was used, due to the simplicity of creating graphical user interfaces using HTML, JavaScript and CSS. In addition, the backend logic for handling socket communication can easily interface with the frontend through RPC.
