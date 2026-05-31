# Technical Requirements
This document list the technical requirements for the project.

## Technological Stack
- Apache Spark
- Apache Kafka
- Docker

## Data Schema
- Transaction
  - transactionId (UUID)
  - accountId (UUID)
  - timestamp (String (Scala Date Format))
  - amount (Double)
  - currency (String ("USD", "EUR" ...))
  - location (latitude/longitude)
  - ipAddress (String)

## Fraud detection Rules
- Large Transaction from New/Suspicious position:
  - A large transaction made from a new location.
- Multiple small transactions from different positions:
  - An account making more than 5 transactions within a 5-minute window, where at least 3 of those transactions originate from distinct geographical locations.