Splunk is a log management and monitoring tool.
It helps you collect, index, search, analyze, and visualize machine data (logs, metrics, events).


🔑 Splunk Components

Forwarder

Installed on client machines (Linux, Windows, servers).

Collects logs and sends them to the Indexer.

Types:

Universal Forwarder (UF) → lightweight agent (most common).

Heavy Forwarder (HF) → can parse/filter before sending.

Indexer

Stores and processes incoming data.

Breaks logs into events.

Creates indexes for fast search.

Example: Error logs → saved in index = error_index.

Search Head

User interface (web GUI on port 8000).

Where you run search queries, create dashboards, alerts.

Deployment Server (optional)

Manages multiple forwarders.

Pushes configurations.

Cluster Master / License Master (advanced)

Used in large enterprise setups for scaling & license management.

🏗 Splunk Architecture Diagram

Here’s a beginner-friendly architecture 👇

                +-------------------------+
                |     Search Head (UI)    |
                |  - Dashboards           |
                |  - Alerts               |
                |  - Reports              |
                +-----------+-------------+
                            |
                            v
+-------------------+   +---+-------------------+
| Universal Forwarder|  |      Indexer          |
| (on apps, servers) |->|  - Stores data        |
| - Collects logs    |  |  - Indexes events     |
+-------------------+   |  - Searchable storage |
                        +-----------------------+


Forwarder → Collects data

Indexer → Stores data, makes it searchable

Search Head → GUI for queries & dashboards

⚡ Example Flow

Linux server log → Forwarder

Forwarder → sends to Indexer

Indexer → stores in /opt/splunk/var/lib/splunk/

Search Head → User searches & builds charts

👉 In small setups (like your EC2 test):

All 3 (Forwarder + Indexer + Search Head) run on one machine.

That’s why you just installed Splunk Enterprise on your EC2.
