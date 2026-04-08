# Kafka-Project
This project demonstrates the use of Apache Kafka as a distributed streaming platform for building real-time data pipelines and event-driven applications. It showcases how to produce, consume, and process streaming data efficiently using Kafka’s high-throughput and fault-tolerant architecture.

# Scalable Backend with Python & Kafka

## Overview
This project demonstrates a scalable backend architecture using **Python** and **Apache Kafka** for real-time data processing. The system handles a food ordering workflow with multiple services interacting through Kafka as the central data pipeline.

---

## Architecture

![Architecture](Capture d'écran 2026-02-26 225922.png)

The system includes:

1. **Food Ordering Client (Frontend)**  
   - The interface where users place orders.

2. **Orders Backend**  
   - Receives orders from the client.  
   - Writes order details to Kafka.

3. **Kafka (Data Pipeline)**  
   - Acts as the messaging backbone.  
   - Handles all event streaming between services.

4. **Email Backend**  
   - Reads confirmed orders from Kafka.  
   - Sends order confirmation emails.

5. **Analytics Backend**  
   - Reads order details from Kafka.  
   - Performs analytics and writes order confirmation events back to Kafka.

6. **Transactions Backend**  
   - Reads order details from Kafka.  
   - Processes transactions (payments).

---

## Features

- **Scalable architecture** with decoupled services.
- **Real-time processing** of orders and confirmations.
- **Event-driven design** using Kafka topics.
- **Extensible backend** that can integrate new services easily.

---

## Getting Started

### Prerequisites

- Python 3.10+
- Apache Kafka
- pip

### Setup

1. Clone the repository:

```bash
git clone https://github.com/ghazza-2/Kafka-Project.git
cd Kafka-Project
2. Create and activate a virtual environment:
python -m venv venv
# Windows
venv\Scripts\Activate.ps1
# Linux / Mac
source venv/bin/activate
3. Install dependencies:
pip install -r requirements.txt
Start Kafka and the backend services.
