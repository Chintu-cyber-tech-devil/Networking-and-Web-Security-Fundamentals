
# TCP vs UDP

## 1. What is TCP?

TCP stands for Transmission Control Protocol.

TCP is a connection-oriented protocol that provides reliable and ordered data delivery.

### Features of TCP

1. Connection-oriented — establishes a connection using a three-way handshake.
2. Reliable delivery — retransmits lost data when necessary.
3. Ordered delivery — delivers data to applications in the correct order.
4. Acknowledgment — confirms the receipt of data.
5. Flow control — prevents a sender from overwhelming a receiver.
6. Congestion control — helps manage network congestion.
7. Higher overhead — reliability mechanisms require additional processing.

### Common Uses of TCP

| Service | Port | Purpose                  |
|---      |---   |---                       |
| HTTP    | 80   | Web communication        |
| HTTPS   | 443  | Secure web communication |
| SSH     | 22   | Secure remote access     |
| FTP     | 21   | File transfer control    |
| SMTP    | 25   | Email transfer           |
| MySQL   | 3306 | Database communication   |
| RDP     | 3389 | Remote desktop access    |

Note: HTTP/3 uses QUIC over UDP instead of TCP.

## 2. What is UDP?

UDP stands for User Datagram Protocol.

UDP is a connectionless transport-layer protocol that sends data without providing built-in delivery guarantees.

### Features of UDP

1. Connectionless — does not require a TCP-style handshake.
2. No delivery guarantee — packets may be lost.
3. No ordering guarantee — packets may arrive out of order.
4. No built-in retransmission — applications must implement their own if needed.
5. Low overhead — has a smaller transport header than TCP.
6. Low latency — useful for applications that prioritize timely delivery.

### Common Uses of UDP

| Service       | Port         | Purpose 
|---            |---           |---
| DNS           | 53           | Domain name resolution 
| DHCP          | 67/68        | Automatic IP configuration 
| VoIP          | Varies       | Internet voice calls 
| Online Gaming | Varies       | Real-time communication 
| Live Streaming| Varies       | Real-time media delivery 
| QUIC / HTTP/3 | 443 commonly | Modern web communication 

Note: DNS can also use TCP, and the transport protocol used by an application depends on its design and configuration.

## 3. TCP vs UDP Comparison

| Feature            | TCP                           | UDP                        
|---                 |---                            |---                        
| Full Form          | Transmission Control Protocol | User Datagram Protocol 
| Connection         | Connection-oriented           | Connectionless 
| Handshake          | Three-way handshake           | No TCP-style handshake 
| Reliability        | Reliable delivery             | No built-in delivery guarantee 
| Data Order         | Preserves order               | May arrive out of order 
| Acknowledgment     | Supported                     | Not built in 
| Retransmission     | Supported                     | Not built in  
| Flow Control       | Yes                           | No built-in flow control 
| Congestion Control | Yes                           | No built-in congestion control 
| Header Size        | Minimum 20 bytes              | 8 bytes 
| Overhead           | Higher                        | Lower 
| Common Uses        | Web, SSH, file transfer       | DNS, VoIP, gaming 

## 4. Simple Real-World Example

### TCP — Sending a Tracked Parcel

Imagine sending a parcel with tracking.

- The receiver acknowledges delivery.
- Missing parcels can be investigated and resent.
- Delivery order can be maintained when required.

TCP provides similar reliability mechanisms for data transmission.

### UDP — Sending Quick Messages

Imagine announcing information without waiting for individual acknowledgments.

- Messages are sent without built-in delivery confirmation.
- Some messages may be lost.
- Communication can continue without waiting for retransmission.

UDP is useful when timely delivery matters more than retransmitting every lost packet.

## 5. Cybersecurity Relevance

Understanding TCP and UDP helps cybersecurity professionals:

1. Identify network services and their transport protocols.
2. Interpret packet captures in Wireshark.
3. Understand port-scanning results in Nmap.
4. Investigate suspicious network traffic.
5. Understand TCP SYN floods and UDP floods.
6. Configure firewall rules appropriately.

## 6. Common Network Attacks

### TCP SYN Flood
An attacker sends many TCP connection requests to exhaust server resources.

### UDP Flood
An attacker sends large amounts of UDP traffic to overwhelm a target.

These attacks can disrupt availability. Test detection and defenses only in an authorized lab.

## 7. Key Takeaway

- TCP prioritizes reliable, ordered delivery.
- UDP provides connectionless communication with lower protocol overhead.
- Neither protocol is automatically secure or encrypted.
- The correct choice depends on the application's requirements.




# TCP Three-Way Handshake

## 1. What is a TCP Three-Way Handshake?

The TCP three-way handshake is the process used to establish a TCP connection between a client and a server before normal data transfer begins.

It consists of three steps:

1. SYN
2. SYN-ACK
3. ACK

## 2. Steps of the TCP Handshake

### Step 1: SYN (Synchronize)

The client sends a SYN packet to the server to request a connection.

### Step 2: SYN-ACK (Synchronize-Acknowledge)

The server responds with a SYN-ACK packet. It acknowledges the client's request and sends its own initial sequence number.

### Step 3: ACK (Acknowledge)

The client sends an ACK packet to acknowledge the server's sequence number.

The TCP connection is now established.

## 3. TCP Three-Way Handshake Diagram

```text
Client                         Server
  |                               |
  | -------- SYN ----------------> |
  |                               |
  | <------ SYN-ACK -------------- |
  |                               |
  | -------- ACK ----------------> |
  |                               |
  |     Connection Established     |
```

## 4. Example with Sequence Numbers

Assume the client uses sequence number `1000` and the server uses sequence number `5000`.

```text
Step 1:
Client -> Server
SYN, Seq = 1000

Step 2:
Server -> Client
SYN-ACK, Seq = 5000, Ack = 1001

Step 3:
Client -> Server
ACK, Seq = 1001, Ack = 5001
```

### Why are the acknowledgment numbers 1001 and 5001?

A SYN consumes one sequence number.

- The server acknowledges the client's SYN with `Ack = 1001`.
- The client acknowledges the server's SYN with `Ack = 5001`.

## 5. Why Is the Handshake Important?

- Establishes a TCP connection.
- Synchronizes sequence numbers.
- Confirms that both endpoints can communicate.
- Prepares the connection for reliable data transfer.

## 6. TCP SYN Flood Attack

A TCP SYN flood is a denial-of-service attack in which an attacker sends many SYN requests and may leave connections incomplete.

The target server may use resources tracking these incomplete connections, affecting legitimate users.

### Possible Defenses

- SYN cookies
- Rate limiting
- Firewall filtering
- Network monitoring
- Denial-of-service protection

Only test attack detection and defenses in an authorized lab.

## 7. Cybersecurity Applications

Understanding the TCP handshake helps cybersecurity professionals:

- Analyze TCP connections in Wireshark.
- Understand Nmap scan results.
- Investigate incomplete or suspicious connections.
- Understand SYN flood detection.
- Troubleshoot network connectivity.

## 8. Key Takeaway

The TCP three-way handshake follows this sequence:

**SYN → SYN-ACK → ACK**

It establishes a TCP connection before normal data transfer begins.
