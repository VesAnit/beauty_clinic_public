# AI Assistant for Aesthetic Medicine Clinic



## Public Limited Version

This is a public limited version of an administrator agent implementation for a beauty clinic. This repository contains a demonstration notebook showing the basic concept of a procedure search system using RAG (Retrieval-Augmented Generation).

## Business Idea

**Problem:** Aesthetic medicine clinics receive numerous daily inquiries from clients about procedures, their costs, duration, specialists, and appointment availability. Administrators spend significant time handling repetitive questions, which reduces clinic efficiency. Not all inquiries come during business hours, leading to loss of potential clients.

**Solution:** An intelligent AI assistant that:
- Automatically processes client inquiries in natural language
- Searches for relevant information about procedures in the database
- Provides personalized responses considering the query context
- Books clients for procedures (implementation not demonstrated in this notebook)

**Business Value:**
- Reduced workload for administrators
- 24/7 information availability for clients
- Instant query processing without waiting
- Personalized recommendations based on up-to-date database
- Automation of procedure booking process

## What Happens in the Notebook

The demonstration notebook shows the basic workflow of a RAG system:

### 1. Data Loading and Validation
- Reading procedure data from an Excel file (`test.xlsx`)
- Data type validation (strings, integers)
- Data preparation for database loading

### 2. Database Structure Creation
- Creating the `medical` schema in PostgreSQL
- Creating the `procedures` table with procedure information
- Creating the `appointments` table for client bookings

### 3. RAG System Configuration
- LLM initialization (AWS Bedrock is used in the notebook)
- Configuring a retriever that creates SQL queries using LLM
- Prompt configuration for SQL generation considering data specifics (anesthesia, cost)

### 4. Response Generation
- LLM generates a polite, structured response based on found data
- Provides information about all suitable specialists
- Offers to book a procedure


## Conclusion

This demonstration version shows the basic concept of a RAG system for searching medical procedures. The full version is a production-ready solution with a conversational agent, Telegram bot, and automated ETL pipeline.

