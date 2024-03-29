## Linux CLI, and HTTP

- [x] Learn the Command Line (Codeacademy)
- [x] HTTP: The Protocol Every Web Developer Must Know - Part 1
- [x] HTTP: The Protocol Every Web Developer Must Know - Part 2
- [x] Describe your impressions about learned materials.
- [x] Extra Materials
- [x] Optional

**CLI** - Command Line Interface
**GUI** - Graphic User Interface

**HTTP** stands for Hypertext Transfer Protocol. 
In-depth coverage -> RFC.
HTTP communication takes place over *TCP/IP*. The default port: **80** (Other ports could be used).
Communication between a host and a client occurs, via a **request/response pair**.
**URL** - Uniform resource locator.
```
http://www.domain.com:1234/path/to/resource?a=b&x=y
  |             |       |         |            |
protocol       host    port    resource      query
```
- GET: fetch an existing resource. The URL contains all the necessary information the server needs to locate and return the resource.
- POST: create a new resource. POST requests usually carry a payload that specifies the data for the new resource.
- PUT: update an existing resource. The payload may contain the updated data for the resource.
- DELETE: delete an existing resource.
Request -> URL + VERB (GET, POST, etc.)
Response -> Status Code + Message Body.

Content of response or request:
```
message = <start-line>
          *(<message-header>)
          CRLF
          [<message-body>]

<start-line> = Request-Line | Status-Line 
<message-header> = Field-Name ':' Field-Value
```
### Configuring Linux Web Servers (Udacity course)

#### Intro to Linux

*etc* - directory with configuration files.
*var* - variable files, files that might grow in the future.
*bin* - executable binaries stored.
*sbin* - similar to bin directory, but commands only for root user.
*lib* - libraries.

#### Linux Security

The Rule of Least Privilege - the program should have permission only for doing it's job, not more.

`sudo adduser ...` - add new user.
`sudo passwd -e [USER]` - make user password expired.

**Octal permissions:**

`r = 4, w = 2, x = 1`

### Networking for Web Developers (Udacity course)

**DNS** - Domain Name System.

host [-parameter] *website* - shows info about website (IPv4, IPv6, etc)
dig [-parameter] *website* - shows info about website for scripts(less human readable)

A *Canonical Name* or *CNAME* record is a type of DNS record that maps an alias name to a true or canonical domain name.
An *AAAA* (pronounced *quad A*) record is a DNS record that maps to an IPv6 address.
*NS* stands for ‘name server’ and this record indicates which DNS server is authoritative for that domain (which server contains the actual DNS records). 

TTL - time to live (DNS cache time to live).

IPv4 4 * 1 bytes long address.
Port = 16 bit. 

Layers:
- Hardware : Ethernet, WiFi
- Internet : IP
- Transport : TCP, UDP
- Application : HTTP, SSH, NTP

In low-level computer languages, a flag is a Boolean value — a true or false value — that is stored in memory as a single bit. If a flag bit is 1, we say the flag is set. If the flag bit is 0, the flag is cleared (or unset).

The original TCP packet format has six flags. Two more optional flags have since been standardized, but they are much less important to the basic functioning of TCP. For each packet, tcpdump will show you which flags are set on that packet.

- SYN (synchronize) [S] — This packet is opening a new TCP session and contains a new initial sequence number.
- FIN (finish) [F] — This packet is used to close a TCP session normally. The sender is saying that they are finished sending, but they can still receive data from the other endpoint.
- PSH (push) [P] — This packet is the end of a chunk of application data, such as an HTTP request.
- RST (reset) [R] — This packet is a TCP error message; the sender has a problem and wants to reset (abandon) the session.
- ACK (acknowledge) [.] — This packet acknowledges that its sender has received data from the other endpoint. Almost every packet except the first SYN will have the ACK flag set.
- URG (urgent) [U] — This packet contains data that needs to be delivered to the application out-of-order. Not used in HTTP or most other current applications.
Three-way handshake

**Firewalls** are devices that network operators can use to filter traffic that's coming into or leaving their network.

### (NEW!) Big amount of different codes.
- 1xx: Informational Messages
- 2xx: Successful
- 3xx: Redirection
- 4xx: Client Error
- 5xx: Server Error

*Ethernet* is a family of computer networking technologies commonly used in local area networks (LAN), metropolitan area networks (MAN) and wide area networks (WAN).

*Twisted pair* cabling is a type of wiring in which two conductors of a single circuit are twisted together for the purposes of improving electromagnetic compatibility.

### (SURPRISED!)
Custom headers can also be created and sent by the client; they will be treated as entity headers by the HTTP protocol.
*Everything is a file* describes one of the defining features of Unix.
`*nix` systems also contain:
**Hard Link** — additional name for existing file.
**Symbolic link** — something like label on Windows systems.
**Socket** — internal endpoint for sending or receiving data within a node on a computer network.

### (USE IN THE FUTURE!)
Tools for View HTTP Traffic:
- Chrome/Webkit inspector
- Fiddler (Windows)
- Charles Proxy (OSX)
Command line:
- curl 
- tshark
- tcpdump

ZHS is cool shell with many usefull features.

`take` - command for creating directory and diving into it.

*trash* plugin -> safer alternative to `rm`.

### Screenshots / Completed courses

![Command Line](../img/CommandLine[Codeacademy].png)
![Command Line](../img/CLI[Hexlet].png)
![Network](../img/Networking_for_Web_Developers[Udacity].png)