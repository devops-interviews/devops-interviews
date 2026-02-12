# Inspecting HTTP Traffic Flow

> **Company:** Airbnb | **Difficulty:** Medium

---

#### **Scenario**

You suspect the web service isn't receiving HTTP requests, and you need to confirm network traffic to port 80.

#### **Task**

Capture network packets destined for or originating from **port 80** (HTTP traffic), limit the capture to the first 10 packets to avoid large files, save the captured packets to `/tmp/http_traffic.pcap` in pcap format, read the capture file and extract key information (source IP, destination IP with port, TCP flags), create a human-readable summary showing packet flow and TCP handshake details, and save the summary to `/tmp/http_summary.txt` in the format `SOURCE_IP -> DEST_IP:PORT [FLAGS]`.

*You may use `tcpdump` to capture and inspect packets.*

#### **Important**
You can run script below to save http_summary.txt instead of manually filling the file since main goal is test troubleshooting.
```sh
cat <http_traffic_file> | awk '/Flags/ && /IP/ {
    # Skip IPv6 packets, only process IPv4
    if ($0 ~ /IP6/) next

    # Extract source and destination IPs WITH ports
    # Pattern: IP source.port > dest.port
    if (match($0, /IP ([0-9]+\.[0-9]+\.[0-9]+\.[0-9]+)\.([0-9]+) > ([0-9]+\.[0-9]+\.[0-9]+\.[0-9]+)\.([0-9]+)/, parts)) {
        src_ip = parts[1]
        src_port = parts[2]
        dst_ip = parts[3]
        dst_port = parts[4]

        # Extract flags
        if (match($0, /Flags (\[[^\]]+\])/, flags)) {
            print src_ip ":" src_port " -> " dst_ip ":" dst_port " " flags[1]
        }
    }
}' > /tmp/http_summary.txt
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/inspecting-http-traffic-flow)
