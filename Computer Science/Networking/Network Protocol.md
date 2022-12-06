#CompSci

# Network Protocol
A set of rules for data transmission which are agreed upon by the sender and receiver.

> [!Note] 
> Often 'protocol suite' is used interchangeably with 'protocol'. It is important to note the difference. A protocol suite contains more than one protocol. The complexity of networking requires many individual protocols.

> [!Note]
> A simple example of a protocol could be one that defines:
> - positive voltage represents a bit value of $1$.
> - a transmission speed that the sender should not exceed.
> - the format of the messages transmitted.
> 	- the first $40$ bytes of a packet could be defined to represent some information such as header information.

# Protocol Stack
The protocols can be seen as **layers** that make up the protocol stack.

![[Network Protocol 2022-11-16 17.17.24.excalidraw]]

- Each layer can only accept input from *adjacent* layers.
- There is a defined **interface** between adjacent layers.
	- The only way the layers can communicate is via this interface.
- A layer may comprise *sub-layers*.
- **User-interaction** takes place via the **highest layer** in the stack.
- Direct-access to *hardware* is confined within the *lowest layer* in the stack.

# Handshaking
A protocol is established between a sender and receiver by handshaking. This is the process of negotiation between the parties by an exchange of messages.

Once handshaking is complete, data packets travel from sender to receiver through various routers.

#Todo move this into its own IP Address notes
# [[IP Address]] & [[MAC Address]]
- A MAC address is the address provided by the manufacturer that uniquely identifies the network interface card.
- IP addresses are provided by a network administrator and define the connection between network and device.

# Port Numbers
![[Pasted image 20221108113133.png]]

