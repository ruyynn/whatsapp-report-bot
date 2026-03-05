# 🤖 *WhatsApp Mass Reporter Bot*

A powerful Telegram bot that automatically sends mass reports to WhatsApp support using professional email templates. Send 10-50 reports per session with different email variations to increase visibility and priority.

<p align="center">
  <img src="https://img.shields.io/badge/Version-2.0-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/WhatsApp-Mass%20Reporter-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Telegram-Bot-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Node.js-18%2B-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />
</p>

---

## 📑 *Table of Contents*
- [Features](#-features)
- [Prerequisites](#-prerequisites)
- [Quick Start](#-quick-start)
- [How to Use](#-how-to-use)
- [Reporting Categories](#-reporting-categories)
- [Configuration](#-configuration-options)
- [Security](#-security-features)
- [Troubleshooting](#-troubleshooting)
- [Project Structure](#-project-structure)
- [Important Notes](#-important-notes)
- [Contributing](#-contributing)
- [Support](#-support)

---

## 🚀 *Features*

| Feature | Description |
|---------|-------------|
| 📨 **Mass Reporting** | Send 10-50 reports per session to WhatsApp support |
| 📝 **Professional Templates** | Pre-built email templates that get attention |
| 🔄 **Multiple Email Variations** | Unique content for each report to avoid duplication flags |
| 📊 **Real-time Progress** | Live updates during report sending |
| 🔁 **Automatic Retry System** | Failed reports are automatically retried |
| ⚖️ **Rate Limiting** | Smart limits to prevent abuse |
| 🔒 **Security First** | Uses App Passwords, never store regular passwords |

---

## 📋 *Prerequisites*

- ✅ Node.js 16.0 or higher
- ✅ npm or yarn
- ✅ Telegram account
- ✅ Gmail account (with 2FA enabled)
- ✅ Google App Password (required)

---

## ⚡ *Quick Start*

### 1. *Installation*

```bash
# Clone the repository
git clone https://github.com/infofbnr/whatsapp-report-bot
cd whatsapp-report-bot

# Run automated setup
npm run setup

# Install dependencies
npm install
```

### 2. Configuration
## 🤖 Telegram Bot Token

1. Message @BotFather on Telegram

2. Send `/newbot` and follow instructions

3. Copy the bot token

## 📧 Gmail App Password (REQUIRED)

1. Enable 2-Factor Authentication on your Google account

2. Generate App Password

3. Select "Mail" → "Other" → Name: "WhatsApp Bot"

4. Copy the 16-digit app password

## ⚙️ Edit .env File
```env
TELEGRAM_BOT_TOKEN=1234567890:ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghi
SMTP_EMAIL=your_email@gmail.com
SMTP_PASSWORD=your_16_digit_app_password  # ← APP PASSWORD ONLY!
```
### 3. Testing
```bash
# Test email configuration
npm run test:email

# Test bot configuration
npm run test:bot
```
### 4. Run the Bot
```bash
# Start the bot
npm start

# Development mode with auto-restart
npm run dev
```
# 🎯 How to Use
<div align="center"> <h3>⚡ Simple & Fast Reporting System ⚡</h3> </div>

 📱 Starting the Bot
 
<div> <table> <tr> <td width="50" align="center">1️⃣</td> <td>Find your bot on Telegram</td> </tr> <tr> <td align="center">2️⃣</td> <td>Open chat with the bot</td> </tr> <tr> <td align="center">3️⃣</td> <td>Send command: <code>/start</code></td> </tr> </table> <br> <blockquote> 💡 After sending /start, the bot will welcome you and show available commands </blockquote> </div>

 📤 Mass Reporting Process
 
<div> <table> <tr> <th width="50">Step</th> <th>Action</th> <th>Example</th> </tr> <tr> <td align="center"><b>1</b></td> <td>Send <code>/report</code> command</td> <td><code>/report</code></td> </tr> <tr> <td align="center"><b>2</b></td> <td>Enter WhatsApp number</td> <td><code>+1234567890</code></td> </tr> <tr> <td align="center"><b>3</b></td> <td>Select category (1-10)</td> <td><code>3</code> for Fake Account</td> </tr> <tr> <td align="center"><b>4</b></td> <td>Describe incident</td> <td><i>"This account is impersonating me..."</i></td> </tr> <tr> <td align="center"><b>5</b></td> <td>Contact info or <code>skip</code></td> <td><code>skip</code> or <code>email@example.com</code></td> </tr> <tr> <td align="center"><b>6</b></td> <td>Choose report count</td> <td><code>25</code> (between 10-50)</td> </tr> <tr> <td align="center"><b>7</b></td> <td>Watch live progress</td> <td>✅ Done • ⏳ Sending • ❌ Failed</td> </tr> </table> <br> <table> <tr> <th>Phase</th> <th>Steps</th> <th>Duration</th> </tr> <tr> <td align="center">⚡ Setup</td> <td align="center">1-2</td> <td align="center">~30 seconds</td> </tr> <tr> <td align="center">📋 Details</td> <td align="center">3-5</td> <td align="center">~1 minute</td> </tr> <tr> <td align="center">🚀 Sending</td> <td align="center">6-7</td> <td align="center">30s - 3 minutes</td> </tr> </table> </div>

 💬 Available Commands
 
<div> <table> <tr> <th width="120">Command</th> <th>Description</th> <th width="80">Usage</th> </tr> <tr> <td><code>/start</code></td> <td>Welcome & instructions</td> <td align="center">⭐ First time</td> </tr> <tr> <td><code>/report</code></td> <td>Start mass reporting</td> <td align="center">🚀 Main</td> </tr> <tr> <td><code>/mystats</code></td> <td>Your report history</td> <td align="center">📊 Check</td> </tr> <tr> <td><code>/emailstats</code></td> <td>Email performance</td> <td align="center">📧 Advanced</td> </tr> <tr> <td><code>/help</code></td> <td>Get help</td> <td align="center">🆘 Support</td> </tr> </table> <br> <div> <p><b>Quick tips:</b></p> <ul> <li>• Type <code>/help</code> anytime for assistance</li> <li>• Use <code>/mystats</code> to see your daily limits</li> <li>• Commands are case-sensitive (lowercase only)</li> </ul> </div> </div>

 📊 Reporting Categories
 
<div> <table> <tr> <th width="30">#</th> <th width="120">Category</th> <th>Description</th> <th>Common Use</th> </tr> <tr><td align="center">1</td><td>🚫 Spam</td><td>Unwanted promotions</td><td>Ads, chain messages</td></tr> <tr><td align="center">2</td><td>⚠️ Harassment</td><td>Bullying, threats</td><td>Hate comments</td></tr> <tr><td align="center">3</td><td>🎭 Fake Account</td><td>Impersonation</td><td>Celebrity fakes</td></tr> <tr><td align="center">4</td><td>👤 Impersonation</td><td>Pretending to be you</td><td>Identity theft</td></tr> <tr><td align="center">5</td><td>🔞 Illegal</td><td>Illegal content</td><td>Drugs, weapons</td></tr> <tr><td align="center">6</td><td>🔒 Privacy</td><td>Private info shared</td><td>Doxxing</td></tr> <tr><td align="center">7</td><td>⚡ Threats</td><td>Direct threats</td><td>Violence</td></tr> <tr><td align="center">8</td><td>💰 Scam</td><td>Fraud</td><td>Money scams</td></tr> <tr><td align="center">9</td><td>🤬 Abusive</td><td>Hate speech</td><td>Racism</td></tr> <tr><td align="center">10</td><td>❓ Other</td><td>Other violations</td><td>Miscellaneous</td></tr> </table> <br> <table> <tr> <th colspan="3">🔥 Popular Categories</th> </tr> <tr> <td align="center"><b>#1 Spam</b></td> <td align="center"><b>#3 Fake Account</b></td> <td align="center"><b>#8 Scam</b></td> </tr> <tr> <td align="center">🔥 Most Reported</td> <td align="center">👥 Common Issue</td> <td align="center">💰 Trending</td> </tr> </table> </div>

 ## ⚙️ Configuration Options
 
 ### 📝 .env File Settings
 ```text
# REPORTING LIMITS
MIN_REPORTS_PER_SESSION=10      # Minimum: 10 reports
MAX_REPORTS_PER_SESSION=50      # Maximum: 50 reports
MAX_REPORTS_PER_HOUR=100        # Per user: 100/hour
MAX_REPORTS_PER_DAY=500         # Per user: 500/day

# EMAIL SETTINGS
EMAIL_SEND_DELAY=3000           # 3 seconds between emails
MAX_EMAIL_ATTEMPTS=3            # Retry 3 times if failed
EMAIL_RETRY_DELAY=10000         # Wait 10s before retry

# SMTP CONFIGURATION (GMAIL)
SMTP_SERVICE=gmail              # Service provider
SMTP_HOST=smtp.gmail.com        # Gmail SMTP server
SMTP_PORT=587                   # TLS port
SMTP_SECURE=false               # Use TLS (not SSL)
```
🛡️ Security Features

<div> <table> <tr> <th colspan="2">🔒 SECURITY LAYERS</th> </tr> <tr> <td width="200">🔐 App Passwords Only</td> <td>• Never store regular passwords<br>• 16-digit temporary codes</td> </tr> <tr> <td>🚦 Rate Limiting</td> <td>• Prevent abuse<br>• Fair usage for all</td> </tr> <tr> <td>🌐 IP Restrictions</td> <td>• Whitelist/blacklist<br>• DDoS protection (Optional)</td> </tr> <tr> <td>🧹 Session Management</td> <td>• Auto cleanup after 24h<br>• No lingering data</td> </tr> <tr> <td>🗑️ No Data Storage</td> <td>• Reports deleted after sending<br>• Zero logs retention</td> </tr> </table> <br> <div align="center"> <b>✅ 100% Privacy Focused - Your data stays yours</b> </div> </div>

🔧 Troubleshooting

<div> <h3>❌ Common Issues & Solutions</h3> <details> <summary><b>📧 Emails not sending</b></summary> <br> <b>Symptoms:</b> <ul> <li>"SMTP Connection Error"</li> <li>No emails received</li> <li>Timeout messages</li> </ul> <b>Solutions:</b> <ol> <li>Verify you're using APP PASSWORD (16 digits)</li> <li>Enable 2-Factor Authentication</li> <li>Check SMTP settings in .env</li> <li>Test with: <code>npm run test:email</code></li> </ol> </details> <details> <summary><b>🤖 Bot not responding</b></summary> <br> <b>Symptoms:</b> <ul> <li>No reply from bot</li> <li>"Bot is offline" message</li> </ul> <b>Solutions:</b> <ol> <li>Check TELEGRAM_BOT_TOKEN in .env</li> <li>Verify internet connection</li> <li>Restart bot: <code>npm start</code></li> <li>Check logs in /logs folder</li> </ol> </details> <details> <summary><b>⏳ Rate limited</b></summary> <br> <b>Symptoms:</b> <ul> <li>"Too many requests"</li> <li>Slow responses</li> <li>Reports failing</li> </ul> <b>Solutions:</b> <ol> <li>Wait 1 hour cooldown</li> <li>Reduce reports to 20-25 per session</li> <li>Check your limits: <code>/mystats</code></li> <li>Increase EMAIL_SEND_DELAY to 5000ms</li> </ol> </details> </div>

🧪 Quick Test Commands

<div> <table> <tr> <th>Command</th> <th>What it tests</th> <th>Expected Result</th> </tr> <tr> <td><code>npm run test:email</code></td> <td>Email configuration</td> <td>✅ Connection successful</td> </tr> <tr> <td><code>npm run test:config</code></td> <td>.env file settings</td> <td>✅ All variables loaded</td> </tr> <tr> <td><code>npm run test:bot</code></td> <td>Bot connection</td> <td>✅ Bot is online</td> </tr> </table> </div>

📊 Status Indicators

<div> <p>During reporting, you'll see:</p> <ul> <li>✅ <b>[SUCCESS]</b> - Report sent successfully</li> <li>⏳ <b>[PENDING]</b> - Currently sending</li> <li>🔄 <b>[RETRY]</b> - Attempting again (max 3x)</li> <li>❌ <b>[FAILED]</b> - Could not send</li> <li>📊 <b>[PROGRESS]</b> - 25/50 reports sent</li> </ul> </div>

⚡ Quick Reference Card

<div> <table> <tr> <th>Action</th> <th>Command</th> <th>Time</th> </tr> <tr> <td>Start</td> <td><code>/start</code></td> <td>5s</td> </tr> <tr> <td>Report</td> <td><code>/report</code></td> <td>2-5min</td> </tr> <tr> <td>Stats</td> <td><code>/mystats</code></td> <td>2s</td> </tr> <tr> <td>Help</td> <td><code>/help</code></td> <td>3s</td> </tr> </table> </div>

🏆 Best Practices

<div> <ul> <li>✓ Use App Password (not regular password)</li> <li>✓ Start with 20-25 reports first</li> <li>✓ Provide detailed descriptions</li> <li>✓ Wait 1 hour between large sessions</li> <li>✓ Check <code>/mystats</code> to track usage</li> </ul> </div>

🚀 Ready to Start?

<div> <pre># One command to begin npm start</pre> </div>
<div align="center"> <img src="https://img.shields.io/badge/Made%20with-❤️-red"> <img src="https://img.shields.io/badge/For-WhatsApp%20Reporting-blue"> <img src="https://img.shields.io/badge/Status-Active-success"> </div>

# 🧪 Testing Commands
```bash
# Test email functionality
npm run test:email

# Verify configuration
npm run test:config

# Check bot status
npm run test:bot
```
📁 Project Structure
```text
whatsapp-mass-reporter/
├── 📄 index.js                   # Main application entry point
├── 📄 config.js                  # Configuration and settings
├── 📄 setup.js                   # Automated setup script
├── 📄 test-email.js              # Email testing utility
├── 📦 package.json               # Dependencies and scripts
├── 🔒 .env                       # Environment variables
├── 📂 services/
│   ├── telegram-service.js       # Telegram bot handling
│   ├── email-service.js          # Email sending logic
│   └── report-service.js         # Report generation
├── 📂 providers/
│   └── real-email-provider.js    # SMTP email provider
├── 📂 templates/
│   └── report-template.txt       # Email template
├── 📂 scripts/                   # Utility scripts
├── 📂 reports_backup/            # Report backups (optional)
├── 📂 temp/                      # Temporary files
└── 📂 logs/                      # Application logs
```
# 🚨 Important Notes
### ⚖️ Legal and Ethical Use

✅ Only report genuine violations

✅ Do not abuse the system

✅ Respect WhatsApp's Terms of Service

✅ Provide accurate information

✅ This tool is for legitimate reporting only

### 🔧 Technical Limitations

📶 Requires stable internet connection

📧 Gmail has daily sending limits (500 emails/day)

⏱️ WhatsApp support response times may vary

📨 Some emails may be filtered as spam initially

⏳ Performance
🚀 10 reports: ~30 seconds

⚡ 50 reports: ~2-3 minutes

📈 Speed depends on email service performance

# 🤝 Contributing
### 🍴 Fork the repository

🌿 Create a feature branch (`git checkout -b feature/amazing-feature`)

💾 Commit changes (`git commit -m 'Add amazing feature'`)

📤 Push to branch (`git push origin feature/amazing-feature`)

🔍 Open a Pull Request

# 📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

# ⚠️ Disclaimer
This bot is designed for legitimate reporting of WhatsApp policy violations. I am not responsible for misuse of this tool. Users are responsible for complying with WhatsApp's Terms of Service and applicable laws.

## 🌟 Show Your Support
If this project helped you, please give it a ⭐ on GitHub — it helps others discover this tool!

<p align="center"> <a href="https://github.com/infofbnr/whatsapp-report-bot"> <img src="https://img.shields.io/github/stars/infofbnr/whatsapp-report-bot?style=social" /> </a> </p>

# 📞 Support

### Need help?

🔍 Check the troubleshooting section above

✅ Verify your .env file configuration

🔑 Ensure you're using App Password (not regular password)

📧 Test email functionality with npm run test:email

🐛 For bugs or feature requests, please open an issue on GitHub

<p align="center"> <b>WhatsApp Mass Reporter Bot v2.0</b><br> By <a href="https://github.com/KINGSLEY771">KINGSLEY771</a> </p><p align="center"> <img src="https://img.shields.io/badge/Made%20with-Node.js-green" />  <img src="https://img.shields.io/badge/For-WhatsApp-blue" /> </p> 
