
How to run
git clone https://github.com/Sachin70115053/Peer_to_peer_torrent
go get .
Download the required torrent file in 'torrents' folder
go run . "torrent file name"
Eg :- go run . movie1.torrent

20-04-2023
Till Now
The bittorrent client supports single-file and multi-file downloads with efficient distribution capabilities.
The client utilizes UDP and HTTP trackers and modern internet protocols to communicate with peers in the network.
Network scanning for peer discovery is periodically performed to maintain up-to-date peer lists.
Automatic reconnection to previously closed connections is implemented to maximize download success rates.
Data is written directly to disk upon receipt of a piece to optimize performance and prevent memory bloat.
Support for upload and bad peer detection is included in the client.
The client avoids redundant resource usage by skipping pieces that have already been downloaded (A Naive Pause/Resume Functionality).
Peer rating system implementation to identify and avoid bad peers.
Todo
Explore DHT.
Explore Magnet Links.
NAT traversal implementation for improved peer connectivity behind firewalls.
Error Handling
04-03-2023
Till Now
The bittorrent client supports both single-file and multi-file downloads, allowing users to efficiently download large files in a distributed manner.
The client leverages UDP trackers for efficient and reliable communication with peers in the bittorrent network, using the latest internet protocols and technologies.
The client utilizes a smart, yet simple algorithm for mapping pieces to connections, providing a seamless and fast experience for users.
The client periodically scans the network for new peers to connect with, ensuring that the latest and most up-to-date peer lists are being used.
The client establishes new connections with peers via handshakes in set intervals, and can automatically reconnect to connections that previously closed, maximizing the chance of successful downloads.
The client writes files directly to disk as soon as data for a piece is received, preventing memory bloat and ensuring optimal performance.
Todo
(DONE) Work on adding support for additional trackers beyond UDP, such as HTTP to provide more options for users to connect with peers.
(DONE) Work on improving the file resuming functionality, ensuring that only the missing pieces are downloaded, and the existing pieces are not re-downloaded, optimizing file downloads.
(DONE) Implement an estimated time left feature to display the time remaining for download completion, improving user satisfaction and experience.
(DONE) Work on implementing uploads to ensure efficient sharing of files in the bittorrent network, optimizing the upload/download ratio for improved performance.
(DONE) Design a performance evaluation algorithm for peers, which takes into account factors such as download/upload pieces, latency, and connectivity, to determine optimal upload/download ratios and tradeoffs, providing a smooth and reliable user experience.
Add support for magnet links, a popular and efficient way to share files in the bittorrent network, allowing for easy downloads and sharing of content.
Implement DHT support to enable peer discovery and connectivity beyond the tracker, improving overall network efficiency and reliability.
Work on implementing NAT traversal to enable connectivity between peers behind NAT firewalls, improving the reach and accessibility of the client.
02-03-2023
Till Now
The bittorrent client currently supports the download of a single file using the bittorrent protocol.
The client currently only supports the use of UDP trackers for communication and coordination between peers.
The client uses a naive (brute force) algorithm for mapping pieces to connections between peers.
Todo
(DONE) Implement support for multi-file downloads, enabling users to download multiple files in a torrent simultaneously.
Enhance the client's functionality by incorporating additional tracker protocols such as HTTP, TCP, and WebSockets, in order to broaden the range of supported tracker types.
(DONE) Develop a robust upload feature that allows users to share data with other clients in the swarm, and prioritize uploads to maximize overall download speed.
(DONE) Implement a re-handshaking mechanism to automatically re-establish TCP connections that have failed after a successful handshake, thereby ensuring the client can continue to participate in the swarm.
(DONE) Periodically scan for and connect to new peers to maintain a healthy swarm with high availability and fast download speeds.
