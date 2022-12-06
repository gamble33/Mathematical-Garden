A protocol suite designed for use in a [[Local Area Network]] (LAN).

This [[Local Area Network|LAN]] can function in an isolated environment, however it is often connected to the Internet.

The [[TCP-IP Protocol Suite]] isn't concerned with the functioning of the lower two layers ([[TCP-IP Protocol Suite#Data Link Layer|data link layer]] and [[TCP-IP Protocol Suite#Physical Layer|physical layer]]).

Thus, ethernet is a common protocol that is used to provide the functionality of these lowest two layers.

The ethernet suite, comprising the two sub-layers, can be illustrated as such:

![[Ethernet Protocol Stack 2022-11-16 21.51.23.excalidraw]]

# Logical Link Control (LCC)
- Responsible for interaction with the [[TCP-IP Protocol Suite#Network Layer|network layer]].
- Not responsible for checking that the transmission was successfully delivered.

# Medium Access Control (MAC)
- Responsible for assembling the Ethernet [[Packet]] which is consequently referred to as a [[Frame]].
	- The [[Frame]] consists of:
		- The address of the sender and receiver.
- Responsible for initiating [[Frame]] transmisison.
- Handles recovery from transmission failure due to a [[Networking Collision]].
	- It may recover, for example, by [[Carrier-Sense Multiple Access with Collision Detection]].

# Physical Coding Sublayer (PCS)
- Responsible for coding/decoding incoming and outgoing data.
	- It either sends or receives a [[Frame]] from/to the [[Ethernet Protocol Stack#Medium Access Control (MAC)|MAC]] protocol.

# Physical Medium Attachment (PMA)
- Responsible for signal transmission and receiving.