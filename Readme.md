# The Banking Compass - Inbound Banking Support Agent

### Overview
The Banking Compass is an intelligent, bilingual banking assistant built on the Inya.ai platform that handles customer queries across voice and chat channels for Bank of Baroda, Union Bank of India, and Central Bank of India.

### 🌟 Key Features
- **Bilingual Support**: English, Hindi, and Hinglish with seamless switching
- **Secure Authentication**: OTP-based verification using mock data
- **Complete Banking Coverage**: All 10 IVR scenarios + fraud checks + FAQs
- **Smart Escalation**: Warm transfer with full context preservation
- **100% Synthetic Data**: Privacy-first approach with no real PII


## 🚀 Getting Started

### Option 1: Direct Testing (Recommended)
Simply click on our live agent link to start testing immediately:
- **Live Agent Link**: [Insert your Inya.ai shareable link]
- No setup required - just start chatting!

### Option 2: Build Your Own Agent
Want to create your own version? Follow these steps:

#### Step 1: Clone the Repository
bash
git clone https://github.com/ishashwatthakur/The-Banking-Dataset.git
cd The Banking Compass

#### Step 2: Download the Datasets
All 11 synthetic datasets are available 

- `customers.csv` (12 rows) - Customer profiles and authentication
- `transactions.csv` (15 rows) - Transaction history
- `digitaltransactions.csv` (12 rows) - UPI/NetBanking transactions
- `complaints.csv` (8 rows) - Complaint tracking
- `chequestatus.csv` (8 rows) - Cheque status
- `loandetails.csv` (6 rows) - Loan information
- `atms.csv` (6 rows) - ATM locations
- `branches.csv` (6 rows) - Branch network
- `faq_sheet.csv` (10 rows) - Common FAQs
- `fraudwatchlist.csv` (10 rows) - Fraud entities
- `fd_rates.csv` (6 rows) - FD interest rates

#### Step 3: Create Your Inya.ai Agent
1. Log in to your Inya.ai account
2. Create a new agent
3. Navigate to the Knowledge Base section
4. Upload all 11 CSV files 

#### Step 4: Configure the System Prompt
Copy the system prompt from `system_prompt.txt` and paste it into your agent's configuration.

**Important**: The system prompt defines:
- How the agent should behave
- What information to extract from the knowledge base
- Security protocols (OTP verification, data masking)
- Language handling (English/Hindi/Hinglish)
- Error handling and escalation rules

You can customize the system prompt based on your needs:
- Modify the tone (formal/casual)
- Add new intents or entities
- Change escalation triggers
- Adjust language preferences

#### Step 5: Configure Agent Settings

##### Greeting Message
Set a welcoming greeting that reflects your brand:

Default: "Namaste! I'm The Banking Compass, your bilingual banking assistant. How may I help you today? / नमस्ते! मैं Banking Compass हूं। आज मैं आपकी कैसे मदद कर सकता हूं?


##### Ending Message
Configure a polite closing message:

Default: "Thank you for using The Banking Compass. Have a great day! / Banking Compass का उपयोग करने के लिए धन्यवाद। आपका दिन शुभ हो!"


##### Other Settings to Configure:
- **Language Detection**: Enable auto-detection
- **Session Timeout**: Set to 5 minutes
- **Max Retries**: Set to 2 for OTP/errors
- **Escalation Webhook**: Configure if connecting to live agents
- **Voice Settings**: Enable for voice channel support
- **Logging**: Enable structured JSON logging

## 📊 Understanding the Datasets

Each dataset serves a specific purpose in the agent's knowledge base:

| Dataset | Purpose | Key Fields |
|---------|---------|------------|
| customers.csv | User authentication & account info | AccountNumber, Balance, MockOTP |
| transactions.csv | Transaction history | TransactionID, Amount, Date |
| complaints.csv | Complaint tracking | TicketID, Status, Resolution |
| branches.csv | Branch locations | IFSC, Address, Services |
| atms.csv | ATM network | Location, Status, CashAvailable |
| fraudwatchlist.csv | Fraud detection | EntityName, RiskLevel, Action |


## 🧪 Testing Your Agent

### Test Scenarios
We recommend testing these 20 scenarios:
1. Account balance inquiry
2. Transaction history
3. Card blocking
4. Dispute raising
5. Complaint status check
6. Branch/ATM location
7. KYC status
8. Cheque status
9. FD rates
10. Loan details
11. Hindi language queries
12. Wrong OTP handling
13. Escalation flows
14. Fraud entity checks
15. Ambiguous requests

### Sample Test Conversations

**English:**

User: What's my balance?
Bot: I'll help you check your balance. Please provide your 12-digit account number.
User: 123456789012
Bot: For security, I'm sending an OTP to your registered mobile ****3210. Please enter the 6-digit OTP.
User: 123456
Bot: Thank you! Your account balance is ₹15,430.55. Status: Active.


**Hindi:**

User: मेरा बैलेंस बताओ
Bot: मैं आपका बैलेंस चेक करने में मदद करूंगा। कृपया अपना 12-अंकों का खाता नंबर दें।


## 🔧 Customization Guide

### Modifying the System Prompt
The system prompt controls the agent's behavior. Key sections to customize:

1. **Identity & Tone**
   
   You are "The Banking Compass," a secure, friendly, expert banking assistant...
   

2. **Security Rules**
   
   For sensitive actions, always verify OTP from MockOTP field...
   

3. **Language Handling**
   
   Auto-detect English/Hindi and respond in same language...
   

4. **Knowledge Base Rules**
   
   Only use data from the 11 CSV files. Never invent information...
   

### Adding New Features
To add new banking features:
1. Add relevant data to existing CSVs or create new ones
2. Update the system prompt with new intents
3. Add test cases for the new features
4. Update greeting/ending messages if needed



## 📁 Repository Structure


   ├── The Banking Compass/
   ├── customers.csv
   ├── transactions.csv
   ├── complaints.csv
   └── ... (8 more datasets)
   ├── README.md


## 🔒 Security & Compliance
- **No Real Data**: 100% synthetic datasets
- **Masked Outputs**: Account (******1234), Card (****5678)
- **Simulated OTP**: Uses MockOTP field from dataset
- **Audit Logs**: Structured JSON logging
- **Privacy First**: No PII storage or processing


## 📹 Demo & Documentation
- **Live Agent**: [Your Inya.ai agent link]
- **Video Demos**: [YouTube Playlist Link]


---

## 🤝 Contributing
This project was created for the Inya.ai Buildathon 2025. Feel free to:
- Fork and customize for your bank
- Add new languages
- Enhance the datasets
- Improve the system prompt



## 🙏 Acknowledgments
- **Gnani.ai** for organizing the buildathon
- **Inya.ai platform** for powerful conversational AI capabilities
- **Our Team** for the dedication and hard work


## 📞 Support
For questions about:
- **This implementation**: Open an issue in this repository
- **Inya.ai platform**: Contact Inya.ai support
- **Buildathon queries**: Contact Gnani.ai organizers


**Note**: This agent is a demonstration using synthetic data. For production use, please ensure compliance with your organization's security and regulatory requirements.

This enhanced README now includes:
- ✅ Clear options for both testing and building
- ✅ Detailed steps for creating your own agent
- ✅ System prompt customization guidance
- ✅ Greeting and ending message configuration
- ✅ Agent settings recommendations
- ✅ Explanation of how to modify the agent
- ✅ Clear structure for GitHub repository
- ✅ Testing guidelines and examples

