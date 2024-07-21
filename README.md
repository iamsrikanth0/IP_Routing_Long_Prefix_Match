# IP_Routing_Long_Prefix_Match
When you type a search query, for example- "API," into the Google search bar and hit enter, here's what happens:

Converting to Binary and Data Transmission:
- Conversion to Binary: The text ("API") is converted into binary data by your computer. As Computers understand and process information in binary (a series of 0s and 1s).
- Packaging Data: This binary data is packaged into smaller units called packets. Each packet contains part of your query along with additional information, such as the destination address (Google's server).

Sending Data Over the Internet:
- Local Network: The packets first travel through our local network, typically starting with router.
- ISP (Internet Service Provider): Your router sends these packets to your ISP, which routes them onto the broader internet.

"IP Routing"
IP Addresses: Each device on the internet has a unique IP address (like a home address for computers). For example, Google's server might have an IP address like 172.217.6.46.
Routing Tables: Routers use routing tables to determine the best path for each packet to reach its destination. This is where "IP routing" comes in.

What is IP Routing?
Routing Table: A routing table contains a list of IP address prefixes (like area codes in phone numbers) and the next hop (the next router in the path) to reach those addresses.
Longest Prefix Match: When a router receives a packet, it looks at the destination IP address and searches its routing table for the longest matching prefix to determine where to send the packet next. This process is repeated at each router until the packet reaches its destination.

How Tries Help in IP Routing?
Trie DS: A trie (prefix tree) is an efficient way to store and search IP prefixes. Each node in the trie represents a bit (0 or 1) of an IP address.
Efficiency: Using a trie, routers can quickly find the longest matching prefix for the destination IP address, making routing fast and efficient.

Reaching Google's Server:
Routing Through the Internet: The packets travel through several routers and networks, using the IP routing process, until they reach Google's server.
Server Processing: Once the packets reach Google's server, Google processes our search query, finds the relevant search results, and sends them back to us.

Returning the Data to You
Reverse Path: The search results are packaged into packets and sent back through the internet, following a similar routing process in reverse.
Local Network: The packets arrive at your router, which sends them to your computer.
Displaying Results: Your computer assembles the packets and converts the binary data back into the text and images you see as search results on your screen.

Visual Analogy:
Imagine mailing a letter:
- *Typing the query*: Writing the letter.
- *Conversion and packaging*: Putting the letter in an envelope with an address.
- *Sending over the internet*: The postal system delivering your letter through various post offices.
- *IP routing*: Each post office looks at the address and decides the best route to send the letter.
- *Receiving the response*: The recipient reads your letter and sends a reply, which follows a similar path back to you.

**Where Tries Fit
- Router's Routing Table: Each router has a trie-based routing table.
- Longest Prefix Matching: The trie helps the router find the longest matching prefix quickly to determine the best next hop for each packet.
- Efficiency: This ensures your query and the response travel efficiently through the network, reaching their destinations quickly.

  Consider the following prefixes and their corresponding next hops:
- 192.168.0.0/16 -> Next hop A
- 192.168.1.0/24 -> Next hop B
- 192.168.1.128/25 -> Next hop C

Detailed Steps:

1. Class TrieNode:
   - Represents a node in the trie.
   - Uses a Map to store child nodes.
   - Stores the next hop information.

2. Class RoutingTrie:
   - Manages the root of the trie.
   - Contains methods to insert prefixes and perform longest prefix matching.
   - ipToBinaryString: Converts an IP address to a binary string for easy manipulation.
   - insert: Inserts a prefix into the trie. Converts the IP to binary and inserts bit by bit.
   - findLongestPrefixMatch: Traverses the trie to find the longest matching prefix for the given IP address.

3. Main Method:
   - Demonstrates how to insert prefixes into the trie and find the longest prefix match for a given IP address.

