[[Packet]]-switching allows for data transmission without a circuit being established. 

Data cannot be sent in a continuous stream. Instead, data is partitioned into packets. 

Nodes that transmit packets will have extended functionality compared to that of a circuit-switched data transmission.

![[Circuit Switching 2022-11-14 19.57.27.excalidraw]]
This illustration is appropriate to describe packet-switching. However, the links across the network are not defined at the time that a packet is sent by a sender.

# Connectionless Service
A network provides a connectionless service when:
- A packet is dispatched with no knowledge of whether or not the receiver is ready to accept the packet.
- The sender has no way of finding out whether the transmission succeeded or not.

# Connection-Oriented Service
A network provides a connection-oriented service when:
- An initial packet, including a request of acknowledgement is sent.
- If the acknowledgement is received, further packets are sent. 
- If no acknowledgement is received, the sender send a second packet containing a request of acknowledgement.