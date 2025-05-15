# Discord Token Checker

Discord Token Checker is a powerful Discord token checker that verifies tokens and extracts account information. It validates tokens while collecting data on email/phone verification status, server memberships, Nitro subscriptions, billing details, and creation dates. Features include both sequential and turbo (parallel) processing modes, proxy support with auto-rotation, categorized results in organized output files, and a user-friendly interface with color-coded output and progress tracking.

## 📸 Screenshots
![image](https://github.com/user-attachments/assets/3c919933-17aa-4a95-9318-8dd31ce9092d)
![image](https://github.com/user-attachments/assets/d9036565-df5a-4259-87c5-73415430f53c)
![image](https://github.com/user-attachments/assets/ebd505c8-e915-483d-b461-e483cac21981)


## ✨ Features

- **Token Validation**: Verifies Discord tokens and identifies valid, invalid, or locked accounts
- **User Information Retrieval**: Extracts username, email, phone verification status
- **Account Details**: Retrieves creation date, server count, and verification status
- **Nitro Detection**: Identifies accounts with Discord Nitro subscriptions
- **Billing Status**: Detects accounts with payment methods attached
- **MFA Detection**: Identifies accounts with 2FA enabled
- **Proxy Support**: Full HTTP proxy support including authentication
- **Rate Limit Handling**: Smart retry mechanisms for handling Discord rate limits
- **Token Categorization**: Sorts tokens into multiple categories:
    - Email verified accounts
    - Phone verified accounts
    - Accounts with billing methods
    - Accounts with Nitro
    - 2FA-enabled accounts
    - Accounts by creation year
    - Locked vs unlocked accounts
- **Multithreaded Mode**: "Turbo mode" with configurable thread count for faster checking
- **Detailed Logging**: Comprehensive output of account information
- **Colorized Output**: Clear, color-coded terminal output for easy status reading
- **Duplicate Removal**: Automatic filtering of duplicate tokens and proxies
- **Error Handling**: Graceful handling of connection issues and API errors

## 📥 Installation

### Option 1: Download the Executable

1. Go to the [Releases](https://github.com/tahagorme/discord-token-checker/releases) tab
2. Download the latest `token_checker.exe`
3. Run the executable

### Option 2: Run from Source Code

1. Clone the repository or download the source code:
    ```
    git clone https://github.com/tahagorme/discord-token-checker.git
    ```
2. Make sure you have Python 3.8+ installed
3. Install required dependencies:
    ```
    pip install tls-client colorama pyfiglet
    ```
4. Run the checker:
    ```
    python token_checker.py
    ```

## 📋 How to Use

### Setup
1. Run the tool first - it will automatically create the necessary folder structure
2. Add your tokens to input/tokens.txt (one token per line)
3. (Recommended) Add proxies to input/proxies.txt (one proxy per line) to avoid rate limits

### Running the Checker

1. Launch the tool by running the executable or Python script
2. Choose whether to use proxies (if available)
3. Choose between normal mode or turbo mode for faster checking
4. Wait for the checking process to complete
5. View results in the console and in the outputs directory

## 📁 Output Files

The tool generates the following output files:

- `outputs/valid_tokens.txt` - All valid tokens
- `outputs/invalid_tokens.txt` - All invalid tokens
- `outputs/detailed_tokens.txt` - Detailed information for each valid token

## 📂 Directory Structure

After running the tool, your directory will look like this:

```
discord-token-checker/
├── input/
│   ├── tokens.txt         # Place your tokens here
│   └── proxies.txt        # Place your proxies here
│
├── outputs/
│   ├── valid_tokens.txt   # All valid tokens
│   ├── invalid_tokens.txt # All invalid tokens
│   ├── detailed_tokens.txt # Detailed token information
│   │
│   └── categories/
│       ├── email_verified.txt  # Tokens with verified emails
│       ├── phone_verified.txt  # Tokens with phone numbers
│       ├── billing.txt         # Accounts with payment methods
│       ├── nitro.txt           # Accounts with Nitro
│       ├── 2fa.txt             # Accounts with 2FA enabled
│       ├── locked.txt          # Locked tokens
│       ├── unlocked.txt        # Unlocked tokens
│       ├── 2016.txt            # Accounts created in 2016
│       ├── 2017.txt            # Accounts created in 2017
│       └── ...                 # Other years
│
├── token_checker.py       # Source code (if using Option 2)
└── token_checker.exe      # Executable (if using Option 1)
```

### Category Files

Valid tokens are automatically sorted into categories under `outputs/categories/`:

- `email_verified.txt` - Tokens with verified emails
- `phone_verified.txt` - Tokens with phone numbers
- `locked.txt` - Locked accounts
- `unlocked.txt` - Unlocked accounts
- `nitro.txt` - Accounts with Discord Nitro
- `billing.txt` - Accounts with billing information
- `2fa.txt` - Accounts with 2FA enabled
- Year-based files (e.g., `2016.txt`) - Accounts created in specific years

## ⚠️ Important Notes

- This tool is for educational purposes only
- Using proxies is recommended to avoid IP-based rate limiting
- Too many requests in a short time may get your IP temporarily blocked by Discord

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Credits

Developed by uutu (Discord) / tahagorme (Telegram)

---

Feel free to [open an issue](https://github.com/tahagorme/discord-token-checker/issues) if you encounter any problems or have suggestions for improvements!
