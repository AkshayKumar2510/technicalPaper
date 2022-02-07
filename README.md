# Firewall

### What is a firewall?

A **firewall** is a software or firmware that prevents unauthorized access to a network. It inspects incoming
and outgoing traffic using a set of rules to identify and block threats.

Firewalls are used in both personal and enterprise settings, and many devices come with one built-in,
including Mac, Windows, and Linux computers. They are widely considered an essential component of network
security.

### Why are firewalls important?
Firewalls are primarily used to prevent malware and network-based attacks. Additionally, they can help in blocking application-layer attacks.
These firewalls act as a gatekeeper or a barrier. They monitor every attempt between our computer and another network. They do not allow data
packets to be transferred through them unless the data is coming or going from a user-specified trusted source.

Firewalls are designed in such a way that they can react quickly to detect and counter-attacks throughout the network. They can work with rules
configured to protect the network and perform quick assessments to find any suspicious activity i.e, firewall acts as a **traffic controller**.

### How does a firewall work?
A firewall establishes a border between an external network and the network it guards. It is inserted inline across a network connection and inspects all packets entering and leaving the guarded network.
As it inspects, it uses a set of pre-configured rules to distinguish between harmless and malicious packets.

The term 'packets' refers to pieces of data that are formatted for internet transfer. Packets contain the
data itself, as well as information about the data, such as where it came from. Firewalls can use this
packet information to determine whether a given packet abides by the rule set. If it does not, the packet
will be barred from entering the guarded network.

Rule sets can be based on several things indicated by packet data, including:
Their source.
Their destination.
Their content.
These characteristics may be represented differently at different levels of the network. As packet travels through the network, it is reformatted several times to tell the protocol where to send it.
Different types of firewalls exist to read packets at different network levels.

### Types of firewalls
There are mainly three types of firewalls, such as **software firewalls**, **hardware firewalls**, or **both**, depending on their structure.

Each type of firewall has different functionality but the same purpose. However, it is best practice to have **both** to achieve maximum possible protection.

A **hardware firewall** is a physical device that attaches between a computer network and a gateway. For example- a broadband router. A hardware firewall is sometimes referred to as an **Appliance Firewall**.

On the other hand, a **software firewall** is a simple program installed on a computer that works through port numbers and other installed software. This type of firewall is also called a **Host Firewall**.

Firewalls are either categorized by the way they **filter data**, or by **the system they protect**.

>When categorizing by what they protect, the two types are: **network-based** that guard entire networks and are often hardware

>and **host-based**, firewalls guard individual devices – known as hosts – and are often software.

When categorizing by **filtering method**, the main types are:

>- A **packet-filtering** firewall examines packets in isolation and does not know the packet's context.

>- A **stateful inspection** firewall examines network traffic to determine whether one packet is related to
another packet.

>- A **proxy firewall** (aka **application-level gateway**) inspects packets at the application layer of the Open
Systems Interconnection (OSI) reference model.

>- A **Next Generation Firewall (NGFW)** uses a multilayered approach to integrate enterprise firewall
capabilities with an intrusion prevention system (IPS) and application control.

Each type in the list examines traffic with higher level of context than the one before – ie, stateful
has more context than packet-filtering.

#### Packet-filtering firewalls
When a packet passes through a packet-filtering firewall, its source and destination address, protocol and destination port number are checked. The packet is dropped – meaning not forwarded to its destination – if it does not comply with the firewall's rule set. 

A packet-filtering firewall works mainly on the network layer of the OSI reference model, although the transport layer is used to obtain the source and destination port numbers. It examines each packet
independently and does not know whether any given packet is part of an existing stream of traffic.

The packet-filtering firewall is effective, but because it processes each packet in isolation, it can be vulnerable to IP spoofing attacks and has largely been replaced by stateful inspection firewalls.

#### Stateful inspection firewalls
Also known as dynamic packet-filtering firewalls – monitor communication packets over time and examine both incoming and outgoing packets.

This type maintains a table that keeps track of all open connections. When new packets arrive, it compares information in the packet header to the state table – its list of valid connections – and determines whether the packet is part of an established connection. If it is, the packet is let through without further analysis. If the packet does not match an existing connection, it is evaluated according to the rule set for new connections.

Although stateful inspection firewalls are quite effective, they can be vulnerable to denial-of-service(DoS) attacks. DoS attacks work by taking advantage of established connections that this type generally assumes are safe.

#### Application layer and proxy firewalls
This type may also be referred to as a proxy-based or reverse-proxy firewall. They provide application layer filtering and can examine the payload of a packet to distinguish valid requests from malicious code disguised as a valid request for data. As attacks against web servers became more common, it became apparent that there was a need for firewalls to protect networks from attacks at the application layer.
Packet-filtering and stateful inspection firewalls cannot do this at the application layer.

Since this type examines the payload's content, it gives security engineers more granular control over network traffic. For example, it can allow or deny a specific incoming Telnet command from a particular user, whereas other types can only control general incoming requests from a particular host.

When this type lives on a proxy server – making it a proxy firewall -- it makes it harder for an attacker to discover where the network actually is and creates yet another layer of security. Both the client and the server are forced to conduct the session through an intermediary -- the proxy server that hosts an application layer firewall. Each time an external client requests a connection to an internal server or vice versa, the client will open a connection with the proxy instead. If the connection request meets the criteria in the firewall rule base, the proxy firewall will open a connection to the requested server.

The key benefit of application layer filtering is the ability to block specific content, such as known malware or certain websites, and recognize when certain applications and protocols, such as Hypertext Transfer Protocol (HTTP), File Transfer Protocol (FTP) and domain name system (DNS), are being misused.
Application layer firewall rules can also be used to control the execution of files or the handling of data by specific applications.

#### Next generation firewalls (NGFW)
This type is a combination of the other types with additional security software and devices bundled in.
Each type has its own strengths and weaknesses, some protect networks at different layers of the OSI model.
The benefit of a NGFW is that it combines the strengths of each type cover each type's weakness. An NGFW is often a bundle of technologies under one name as opposed to a single component.

Modern network perimeters have so many entry points and different types of users that stronger access control and security at the host are required. This need for a multilayer approach has led to the emergence of NGFWs.

A NGFW integrates three key assets: traditional firewall capabilities, application awareness and an IPS.
Like the introduction of stateful inspection to first-generation firewalls, NGFWs bring additional context to the firewall's decision-making process.

NGFWs combine the capabilities of traditional enterprise firewalls -- including Network Address Translation (NAT), Uniform Resource Locator (URL) blocking and virtual private networks (VPNs) -- with quality of service (QoS) functionality and features not traditionally found in first-generation products.
NGFWs support intent-based networking by including Secure Sockets Layer (SSL) and Secure Shell (SSH) inspection, and reputation-based malware detection. NGFWs also use deep packet inspection (DPI) to check the contents of packets and prevent malware.

When a NGFW, or any firewall is used in conjunction with other devices, it is termed unified threat management (UTM).

### LIST OF FIREWALLS
A small list of Firewalls available is provided.

- CISCO
- Checkpoint
- Fortinet
- Watchguard
- Sophos
- Forcepoint
- Juniper
- D-Link
- Palo Alto
- Fortinet

#### Limitations of Firewall
When it comes to network security, firewalls are considered the first line of defense. But the question is whether these firewalls are strong enough to make our devices safe from cyber-attacks. The answer may be "no". The best practice is to use a firewall system when using the Internet.
However, it is important to use other defense systems to help protect the network and data stored on the computer. Because cyber threats are continually evolving, a firewall should not be the only consideration for protecting the home network.

The importance of using firewalls as a security system is obvious; however, firewalls have some limitations:

- Firewalls cannot stop users from accessing malicious websites, making it vulnerable to internal threats or attacks.

- Firewalls cannot protect against the transfer of virus-infected files or software.

- Firewalls cannot prevent misuse of passwords.

- Firewalls cannot protect if security rules are misconfigured.

- Firewalls cannot protect against non-technical security risks, such as social engineering.

- Firewalls cannot stop or prevent attackers with modems from dialing in to or out of the internal network.

- Firewalls cannot secure the system which is already infected.

Therefore, it is recommended to keep all Internet-enabled devices updated. This includes the latest operating systems, web browsers,
applications, and other security software (such as anti-virus). Besides, the security of wireless routers should be another practice.
The process of protecting a router may include options such as repeatedly changing the router's name and password, reviewing security
settings, and creating a guest network for visitors.
