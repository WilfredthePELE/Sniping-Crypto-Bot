#Solana Trading Assistant

This project implements a Solana Trading Assistant that leverages the Google Gemini model (via LangChain) and Solana blockchain APIs to make informed trading decisions for tokens. It fetches wallet transactions and token metadata using Helius and Solscan APIs, retrieves market data from DexScreener, and supports transaction creation for Solana trades. The assistant provides BUY, SELL, or HOLD recommendations based on token metrics, whale activity, and safety checks, with simulation mode enabled by default for safe testing.
Features

Trading Decisions: Uses Google Gemini (gemini-2.0-flash) to analyze token metrics (e.g., FDV, whale activity) and recommend BUY, SELL, or HOLD actions.
Wallet Monitoring: Fetches recent transactions for specified Solana wallets using the Helius API to detect significant transfers.
Token Safety Checks: Verifies token safety (e.g., disabled freeze authority) using the Solscan Pro API.
Market Data Integration: Retrieves real-time token price, FDV, volume, and liquidity from DexScreener.
Transaction Creation: Generates Solana transactions (e.g., SOL transfers) with Base64 serialization for Phantom wallet compatibility.
Simulation Mode: Supports simulated trades to test logic without executing real transactions.
Error Handling: Includes robust checks for API errors, missing keys, and invalid responses.

Prerequisites

Python 3.8 or higher
Required libraries: requests, langchain-google-genai, solana, py-solana
API keys for:
Google Gemini API for LLM integration
Helius API for Solana wallet and mint data
Solscan Pro API for token metadata


Internet access for API calls
(Optional) Phantom wallet for transaction signing

Installation

Create a virtual environment (optional but recommended):python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate


Install dependencies:pip install -r requirements.txt


Set up environment variables:
Replace 'your-api-key' in the script with your actual API keys, or set them as environment variables:export GOOGLE_API_KEY='your-google-api-key'
export HELIUS_API_KEY='your-helius-api-key'
export SOLSCAN




