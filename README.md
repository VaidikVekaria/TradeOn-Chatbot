# TradeON Chatbot

**Empowering investors with real-time financial insights through conversational AI.**

## 🚀 Overview

TradeON is an intelligent chatbot designed to assist users in making informed stock investment decisions. It provides up-to-date financial data, including balance sheets, cash flow statements, historical stock prices, and more. The chatbot supports side-by-side comparisons of publicly traded companies using real-time data from Yahoo Finance and OpenAI's tools.

## 🎯 Objectives

- Deliver accurate, real-time financial insights.
- Enable multi-company comparisons.
- Guide users through a structured, conversational workflow.
- Support investment decisions with data-driven analysis.

## 🧠 How It Works

### Phase 1: Input Collection

The chatbot engages users in a guided dialogue to gather all necessary parameters:
- Ticker symbol
- Company name
- Stock exchange
- Time period

It ensures completeness by prompting for missing details using clarifying questions and multiple-choice suggestions.

### Phase 2: Data Retrieval & Analysis

Once inputs are collected:
- Retrieves financial data via Yahoo Finance API.
- Analyzes trends, patterns, and risks.
- Provides summaries, comparisons, and follow-up suggestions.

## 🛠️ Key Components

### Data Source

- **Yahoo Finance API**: Core data provider using the `Ticker` function.

### Core Functions

#### Input Collection

- `initialize_system_message()`: Sets up expert persona and strategy.
- `ConversationManager` class:
  - `add_user_message()`, `add_assistant_message()`
  - `get_response()`, `run_function_call()`
  - `moderation_check()`, `check_exit_command()`

#### Data Analysis

- `get_yf_data(my_dict)`: Retrieves financial data.
- `run_yf_prompt(data_dict)`: Formats and analyzes data.
- `get_market_sentiment()`: Uses OpenAI web search for sentiment and news.

#### Orchestration

- `tradeON(chat)`: Manages the full interaction loop.

## ⚙️ Implementation Notes

- Designed for use in **Jupyter Notebook**.
- Modular architecture allows for easy expansion and integration of new features.

## 🧩 Challenges & Lessons Learned

### Challenges

- Choosing between different OpenAI function call formats.
- Structuring complex financial data for model input.
- Integrating web search results effectively.

### Lessons Learned

- Clear phase separation improves usability.
- Comprehensive input validation enhances output quality.
- Modular design supports future scalability.

## 📈 Future Enhancements

- Add support for alternative data sources.
- Expand analytical capabilities (e.g., predictive modeling).
- Improve UI/UX for broader accessibility.
