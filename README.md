# NEBA Backend

## Overview

This backend serves as the server-side component for the NEBA token ecosystem, specifically designed to handle Know Your Customer (KYC) verification processes. It integrates with Sumsub's KYC services to ensure compliance and security for token purchases.

## Purpose

The primary purpose of this backend is to process webhooks from Sumsub, a third-party KYC verification provider. When a user undergoes KYC verification through Sumsub, the backend receives status updates via webhooks. Upon successful verification, the user's wallet address is automatically added to a whitelist, granting them permission to purchase NEBA tokens.

## Key Features

- **Webhook Handling**: Receives and processes real-time status updates from Sumsub regarding KYC verification outcomes.
- **Whitelist Management**: Maintains a secure whitelist of verified wallet addresses eligible for NEBA token purchases.
- **Blockchain Integration**: Interacts with blockchain networks to manage whitelist entries and ensure decentralized compliance.
- **Database Management**: Stores verification data and user information securely using MongoDB.
- **API Endpoints**: Provides RESTful APIs for frontend interactions and administrative functions.

## Architecture

- **Controllers**: Handle business logic for webhook processing and whitelist operations.
- **Models**: Define data structures for KYC verifications and user profiles.
- **Routes**: Define API endpoints for external integrations.
- **Database**: Utilizes MongoDB for persistent data storage.
- **Blockchain**: Integrates with blockchain utilities for whitelist management.

## Technologies Used

- Node.js
- Express.js
- MongoDB
- Web3.js (for blockchain interactions)
- Sumsub API integration

## Getting Started

1. Install dependencies: `npm install`
2. Configure environment variables in `.env`
3. Start the server: `npm start`
