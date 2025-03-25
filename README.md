
# 🔐 Password Strength Analyzer (PSA)

## Overview
This Python script provides a comprehensive password strength analysis tool that calculates password entropy, rates password strength, and estimates crack time. It offers detailed insights into password security and provides actionable recommendations for improving password quality.

## Features
-   📊 Entropy-based strength calculation
-   🏆 Password strength rating system
-   ⏱️ Estimated crack time calculation
-   🛡️ Detailed password security feedback
-   🔍 Pattern detection for weak passwords

## How It Works

The password strength analyzer uses multiple techniques to evaluate password security:

1.  **Entropy Calculation**    
    -   Measures password complexity based on length and character diversity
    -   Applies penalties for common patterns and sequences
2.  **Strength Rating**    
    -   Categorizes passwords from "Very Weak" to "Very Strong"
    -   Provides granular strength assessment
3.  **Crack Time Estimation**    
    -   Calculates potential time to crack the password
    -   Adjusts estimation based on guessing speed

## Installation

### Prerequisites
-   No external dependencies beyond standard library

### Clone the Repository
```bash
git clone https://github.com/Likgiltig/PSA.git
cd PSA-main
```

## Usage
To check passwords you need to alter the python script file. For more advanced usage, consider rewriting the script to use `argparse`. This will allow you to pass the password and guesses per second as command-line arguments, making the script more suitable for terminal use and integration with other tools.
```python
# Basic usage
check_password('YourPassword123!')
# Custom guessing rate (optional)
check_password('YourPassword123!', guesses_per_second=50000000)
```

### Example Output
```
Password: YourPassword123!
Password Strength (Entropy): 52.34 bits
Password Rating: Strong
Estimated Crack Time: 3.42 years
Character Sets Used: Uppercase, Lowercase, Digits, Special
```

## Strength Rating Breakdown
-   **Very Weak**: < 30 bits
-   **Weak**: 30-40 bits
-   **Moderate**: 40-50 bits
-   **Strong**: 50-60 bits
-   **Very Strong**: > 60 bits


## Disclaimer
This is a client-side strength estimation tool. Always implement additional server-side password validation and use secure hashing techniques. Don't rely on this script solely for password strength.

