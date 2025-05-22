# Password Generator

A simple, command-line Python script for generating randomized secure passwords.

## Table of Contents

- [Features](#features)  
- [Prerequisites](#prerequisites)  
- [Installation](#installation)  
- [Usage](#usage)  
- [How It Works](#how-it-works)  
- [Customization](#customization)  

## Features

- Generates passwords with a mix of:
  - Lowercase and uppercase letters  
  - Digits (0–9)  
  - Common symbols (`! " # $ % & ' ( ) * +`)  
- Random ordering of all characters for maximum unpredictability  
- Fully customizable counts of letters, symbols, and numbers 

## Prerequisites

- Python 3.6 or higher

## Installation

Clone this repository and navigate into its directory:

```bash
git clone https://github.com/yourusername/PasswordGen.git
cd PasswordGen
```
## Usage

Run the script from your terminal:

```
python PasswordGen.py
```
You will be prompted to enter:

-How many letters you want in your password?  
-How many symbols you want?  
-How many numbers you want?  

Example session:
```
Welcome to the PyPassword Generator!
How many letters would you like in your password?
> 10
How many symbols would you like?
> 2
How many numbers would you like?
> 4
Generated password: aKfBdRtYpL!&5382
```
## How it works

Character Pools:  
-letters: a list of all lowercase and uppercase English letters  
-symbols: a list of common special characters  
-numbers: a list of digits 0–9  

User Input  
-The script prints a welcome message and uses input() to read three integer values specifying how many  
letters, symbols, and numbers to include .

Random Selection  
-For each category, it picks the requested number of characters using random.choice(), appending each to a list .  

Shuffling  
-The combined list of characters is shuffled with random.shuffle() to ensure full randomness .  

Output  
-The shuffled list is joined into a single string and printed to the console as the final password.   

## Customization

Change symbol set:  
Edit the 'symbols' list at the top of PasswordGen.py.  

Limit to specific characters:  
Modify the 'letters' or numbers lists to include only your desired characters.  

Non-interactive mode:  
Wrap the logic in functions and use the 'argparse' module to accept command-line flags instead of prompts.  
