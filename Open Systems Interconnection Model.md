#Web #Hardware #ClientServer #Protocols 

[[Computer endianness]]

Many different devices can interact with each other by this model. Standard has some separated modules that can interact with another module on same level (horizontal interaction) and higher or lower level by 1 (vertical interaction)

Each intermediate layer serves a class of functionality to the layer above it and is served by the layer below it. Classes of functionality are realized in software by standardized [communication protocols](https://en.wikipedia.org/wiki/Communication_protocol "Communication protocol").

This model has 7 layers:
1) **Application level** - High level APIs for application usage. Most known protocols are HTTP, HTTPS, FTP, RDP, etc
2) **Presentation level** - Data formatting, encryption, decryption, compression, ... Main function of level is to provide independence from data format
3) **Session level** - this level provides function to establish connections between devices. An example of a session-layer protocol is the OSI protocol suite session-layer protocol, also known as X.225 or ISO 8327. In case of a connection loss this protocol may try to recover the connection. If a connection is not used for a long period, the session-layer protocol may close it and re-open it. It provides [synchronization points](https://en.wikipedia.org/wiki/Synchronization_point "Synchronization point") in the stream of exchanged messages.
5) **Transport layer** - This layer controls reliability of given link, errors, segmentation, desegmentation (TCP/IP, UDP)
6) **Network layer** - This level provides functional and procedural meanings to transfer data between nodes. It responsible for package exchanging also through intermediate routes. 
7) **Data link layer** - Levels provides probability to transfer data between two directly connected nodes. It detects and possibly corrects errors that may occur in the physical layer. It defines the protocol to establish and terminate a connection between two connected devices. It also defines the protocol for flow control between them.
8) **Physical layer** - This level provides to transition raw data to electric signal or another physical signal. 

Processing example:
Data processing by two communicating OSI-compatible devices proceeds as follows:

1.  The data to be transmitted is composed at the topmost layer of the transmitting device (layer _N_) into a _[protocol data unit](https://en.wikipedia.org/wiki/Protocol_data_unit "Protocol data unit")_ (_PDU_).
2.  The _PDU_ is passed to layer _N-1_, where it is known as the _[service data unit](https://en.wikipedia.org/wiki/Service_data_unit "Service data unit")_ (_SDU_).
3.  At layer _N-1_ the _SDU_ is [concatenated](https://en.wikipedia.org/wiki/Concatenation "Concatenation") with a header, a footer, or both, producing a _layer N-1 PDU_. It is then passed to layer _N-2_.
4.  The process continues until reaching the lowermost level, from which the data is transmitted to the receiving device.
5.  At the receiving device the data is passed from the lowest to the highest layer as a series of _SDU_s while being successively stripped from each layer's header or footer until reaching the topmost layer, where the last of the data is consumed.