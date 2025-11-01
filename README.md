[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/JTXl4WMa)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=21240962&assignment_repo_type=AssignmentRepo)
# COMP 163 - Project 1: Character Creator & Chronicles
# 🎯 Project Overview

Build a text-based RPG character creation and story progression system that demonstrates mastery of functions and file I/O operations.

# Required Functions 
Complete these functions in project1_starter.py:

create_character(name, character_class) - Create new character

calculate_stats(character_class, level) - Calculate character stats

save_character(character, filename) - Save character to file

load_character(filename) - Load character from file

display_character(character) - Display character info

level_up(character) - Increase character level

# 🎭 Character Classes
Implement these character classes with unique stat distributions:


Warrior: High strength, low magic, high health

Mage: Low strength, high magic, medium health

Rogue: Medium strength, medium magic, low health

Cleric: Medium strength, high magic, high health

# 📁 Required File Format
Your save_character() function must create files in this exact format:

Character Name: [name]

Class: [class]

Level: [level]

Strength: [strength]

Magic: [magic]

Health: [health]

Gold: [gold]


# Run specific test file
python -m pytest tests/test_character_creation.py -v

# Test your main program
python project1_starter.py

GitHub Testing:

After pushing your code, check the Actions tab to see automated test results:

✅ Green checkmarks = tests passed
❌ Red X's = tests failed (click to see details)

# ⚠️ Important Notes
Protected Files

DO NOT MODIFY files in the tests/ directory

DO NOT MODIFY files in the .github/ directory

Modifying protected files will result in automatic academic integrity violation

# AI Usage Policy

✅ Allowed: AI assistance for implementation, debugging, learning

📝 Required: Document AI usage in code comments

🎯 Must be able to explain: Every line of code during interview

# 📝 Submission Checklist

 All required functions implemented
 
 Code passes all automated tests
 
 README updated with your documentation
 
 Interview scheduled and completed
 
 AI usage documented in code comments

# 🏆 Grading

Implementation (70%): Function correctness, file operations, error handling

Interview (30%): Code explanation and live coding challenge

# COMP 163 - Project 1: Character Creator

This project is a Python-based utility designed to manage basic character data for a fantasy Role-Playing Game (RPG). It allows users to create new characters, calculate their starting stats, level them up, view a formatted character sheet, and persist/retrieve data from a text file.

# Game Concept: Stat Formula Overview

The game's concept is built around the mathematical identity of each class, defined by how their stats scale using multiplicative formulas based on the character's Level (L). This system ensures immediate and predictable class roles:

Warrior: Designed as the primary tank and melee combatant, receiving the highest growth multipliers for Strength (15 * L * 5) and Health (40 * L * 2).

Mage: Focused entirely on offense, they receive the highest multiplier for Magic (30 * L * 3), but minimal investment in Strength and Health.

Rogue: Built as a balanced hybrid, their formulas provide medium, equal scaling for both Strength (12 * L * 5) and Magic (25 * L * 3), making them versatile but fragile due to lower Health growth.

Cleric: Acts as a durable caster, pairing high Magic growth (30 * L * 3) with significant Health scaling (40 * L * 2).

# Design Choices & Stat Formulas

The core design principle was creating exaggerated, class-defining stat lines that scale predictably using simple multiplicative formulas.

Stat Calculation (calculate_stats function)

The formulas use the character's level to multiply class-specific base values, ensuring rapid growth in core stats.

File I/O Design (save_character and load_character)
    
The file format is chosen for human readability and simple parsing, using a clear Key: Value format for each line.

# Bonus Creative Features

The main creative feature is the design of the stat system itself, offering four distinct playstyles through highly differentiated growth formulas. Additionally:

Simple Leveling: The level_up function automatically recalculates all stats upon leveling, preventing manual math errors and keeping the stat system balanced.
    
Formatted Display: The display_character function provides a clean, easy-to-read character sheet for quick status checks.

# AI Usage

The following assistance was utilized from the AI model:

Core Logic Implementation: 

Assistance in correcting initial logic errors within the create_character function (specifically resolving a NameError and preventing accidental recursive calls).

Code Structure: 

Ensuring the final code maintained the requested specific function order (create_character first) while keeping all dependent functions callable.

# How to Run

Save the File: Ensure the code is saved as a Python file named character_creator.py.
    
Open Terminal: Navigate to the directory containing the file using your terminal or command prompt.
    
Execute: Run the file directly. The if name == "main": block contains built-in tests that will automatically execute and print output to the console, demonstrating the creation, leveling, saving, and loading functions.
