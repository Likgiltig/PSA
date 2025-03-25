
# 🔐 Password Strength Analyzer (PSA)
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
Password: slimjim1234
Password Strength (Entropy): 29.31 bits
Password Rating: Very Weak
Estimated Crack Time: 6.65 seconds
Weak password. Suggestions:
- Add uppercase letters.
- Add special characters.
- Avoid common patterns or sequences.
Character Sets Used: Lowercase, Digits

Password: SlimJim1234!
Password Strength (Entropy): 44.56 bits
Password Rating: Moderate
Estimated Crack Time: 3.00 days
Character Sets Used: Uppercase, Lowercase, Digits, Special
```

## Strength Rating Breakdown
-   **Very Weak**: < 30 bits
-   **Weak**: 30-40 bits
-   **Moderate**: 40-50 bits
-   **Strong**: 50-60 bits
-   **Very Strong**: > 60 bits


## Disclaimer ⚠️
**WARNING:** This is a research and educational tool for password strength estimation. It is NOT suitable for professional security implementations. Passwords with dictionary words remain vulnerable to attacks, and this script provides only a basic estimation of password strength.

**DO NOT USE** for:
-   Authentication systems
-   Security-critical applications
-   Enterprise password management

