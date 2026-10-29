# Interlink Multi Bot

⚡ Automated multi-account bot for claiming Interlink Labs airdrop tokens on autopilot – now with full proxy and OTP login support.

---

## 🔗 Register Your Main Account

👉 **Referral Link:** [https://interlinklabs.ai/referral?refCode=9707162734](https://interlinklabs.ai/referral?refCode=9707162734)

---

## 🚀 Features

- 🔄 **Multi-Account Support**: Run unlimited accounts from one script
- 🕒 **Auto Claiming**: Automatically claims airdrop tokens every 4 hours
- 🛡️ **Proxy Rotation**: Smart proxy rotation for each account (HTTP, HTTPS, SOCKS4, SOCKS5 supported)
- 🔐 **Persistent Sessions**: JWT token stored per account for auto re-login
- 🔁 **OTP Verification**: Full email-based OTP flow
- 💥 **Auto Retry**: Built-in retry system for failed claims or network errors
- 📈 **Claim Timer**: Countdown for next eligible claim per account
- 📊 **Account Overview**: Real-time claim status, balance display, and timers for each account

---

## 📋 Prerequisites

- ✅ Node.js v16 or newer
- ✅ NPM v8 or newer
- ✅ At least 1 Interlink account (email verified)
- ✅ Optional: Working proxy list (recommended for multi-accounts)

---

## 🛠️ Installation

1. **Clone the repo**:
```bash
git clone https://github.com/DalleDai/Interlink-Bot.git
cd Interlink-Bot
```

2. **Install dependencies**:
```bash
npm install
```

3. **Set up your accounts**:
Create a file called `accounts.txt` in the root directory with your Interlink account info.

```
email1@example.com:passcode1
email2@example.com:passcode2
email3@example.com:passcode3
```

4. **Set up proxies (optional but recommended)**:
Create a file called `proxies.txt` in this format (one proxy per line):

```
http://ip:port:user:pass
socks5://ip:port
ip:port:user:pass
```

Each account will be assigned a proxy in order.

---

## 🚀 Usage

To run the bot:

```bash
node index.js
```

### On First Run for Each Account:

You’ll be prompted for:
- Email/Username
- Passcode
- OTP (check your email inbox)

Once done:
✅ JWT token will be saved automatically in `tokens/` folder  
✅ You won’t be asked again unless the token expires

---

## 🔄 How It Works

1. Loads all accounts from `accounts.txt`
2. Rotates proxies (if provided)
3. Logs in and saves tokens in `tokens/` directory
4. Checks if claim is available
5. Automatically claims tokens if eligible
6. Starts countdown for next eligible time (4 hours)
7. Loops and auto claims every 4 hours — completely hands-off 🎯

---

## ⚙️ Configuration

You can adjust claim intervals or customize claim logic by editing the timing and flow inside `index.js`.

---

## 🧠 Tips

- 🛠 Create a separate proxy for each account for best safety
- 🛡 Run this in a VPS or background terminal for 24/7 farming
- ✅ Claim logs and console colors help you monitor each account

---

## 🔒 Security

- Passwords and OTPs are never saved
- Only secure tokens are saved for session persistence
- All API communication is over HTTPS

---

## ❗ Disclaimer

This tool is for educational purposes only.  
You are solely responsible for how you use this bot.  
We are not responsible for account restrictions or bans.

---

## 📄 License

Licensed under the MIT License – see the LICENSE file.

---

## 🧑‍💻 Contributors

- Developed by [cryptodai3](https://t.me/cryptodai3)
- Supported by the Web3 farming community 💚

---

## 🙌 Support the Project

If this helps you, show love by:
- Using our referral link 💰
- Sharing the repo 🙌
- Reporting bugs & ideas 🧠
