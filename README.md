📡 Step 2: Capturing Network Traffic

Open Wireshark.

Select your active network interface (e.g., eth0).

Click the shark-fin icon (Start) to begin capturing packets.

🌐 Step 3: Generating Network Traffic

From your Windows/Linux target VM, generate traffic:

# Ping the Kali machine
ping 192.168.4.93

# Start SSH session
ssh user@192.168.4.93

# Or run FTP connection
ftp 192.168.4.93


Perform these activities for 2–3 minutes to collect packets.

⏹️ Step 4: Stop Capture and Save

Stop the capture:

Click the red square icon (Stop).

Save the capture file:

File > Save As > lab_capture.pcapng

🔍 Step 5: Analyzing Captured Traffic

Use display filters to isolate traffic:

# SSH traffic
ssh

# ICMP (Ping) traffic
icmp

# FTP traffic
ftp


Example IP mapping:

Kali Linux VM → 192.168.4.93

Windows VM → 192.168.4.94

🧩 Step 6: Inspecting Protocol Details

Click a packet to view its details:

The middle pane shows headers and fields.

The lower pane shows payload and protocol layers.

Example:

TCP packet using port 22 (SSH) with detailed headers and IP information.

🔁 Step 7: Follow TCP Streams

To see full conversations:

Right-click any TCP packet (e.g., FTP).

Choose Follow → TCP Stream.

Observe data exchanged in the session.

FTP is unencrypted — username and password appear in plain text.

📦 Step 8: Exporting Specific Packets

Filter and export specific packets:

File > Export Specified Packets > filtered_packets.pcapng

🧠 Step 9: Analysis Summary
Question	Answer
Captured Protocols	SSH, FTP, ICMP
Source IP	192.168.4.93
Destination IP	192.168.4.94
Inferred Info	Packet size, ports, protocols used
🔐 Reflection

Packet analysis is fundamental in cybersecurity because it allows you to:

Identify malicious or abnormal traffic.

Understand communication patterns.

Detect unencrypted credentials and vulnerabilities.

🧹 Cleanup

Close Wireshark.

Shut down all virtual machines.

✅ Completion

You have successfully conducted packet analysis and protocol identification using Wireshark.
