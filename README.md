# PROJEKT-ZALICZENIOWY
# PadelShopManager

A comprehensive console-based inventory management system for padel sport equipment shops, built in C#.

## Table of Contents
- [Introduction](#introduction)
- [Technologies](#technologies)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Data Storage](#data-storage)
- [Screenshots](#screenshots)
- [Project Status](#project-status)
- [Author](#author)

## Introduction

PadelShopManager is a console application designed to help padel equipment shop owners manage their inventory efficiently. The system provides a complete CRUD (Create, Read, Update, Delete) interface for managing three main product categories: rackets, balls, and clothing items.

The application features a Polish user interface while maintaining clean English code structure, making it accessible to Polish users while keeping the codebase internationally readable.

## Technologies

- **Language**: C# (.NET)
- **Platform**: Console Application
- **Data Storage**: CSV files (plain text)
- **Architecture**: Procedural programming with structs
- **File I/O**: FileStream, StreamReader, StreamWriter

## Features

### Product Categories
- **Rackets** (`Rakiety`)
  - Brand, Model, Price management
  - Data persistence in `rackets.txt`

- **Balls** (`Pilki`) 
  - Name, Price management
  - Data persistence in `balls.txt`

- **Clothing** (`Ubrania`)
  - **Shirts** (`Koszulki`): Name, Size, Price
  - **Shorts** (`Spodenki`): Name, Size, Price  
  - **Shoes** (`Buty`): Name, Size, Price
  - Data persistence in `shirts.txt`, `shorts.txt`, `shoes.txt`

### Core Functionality
- â **Add new items** to any category
- â **Display all items** in organized lists
- â **Remove items** with confirmation prompts
- â **Auto-generated IDs** for all products
- â **Input validation** for all fields
- â **Data persistence** across application sessions
- â **Polish language UI** for better user experience

### Technical Features
- **Convert-based parsing** instead of TryParse
- **Structured data types** using C# structs
- **File-based storage** with CSV format
- **Menu-driven navigation** system
- **Error handling** for invalid inputs

## Installation

1. **Prerequisites**
   - .NET SDK installed on your system
   - Any IDE supporting C# (Visual Studio, VS Code, Rider)

2. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/PadelShopManager.git
   cd PadelShopManager
   ```

3. **Build the project**
   ```bash
   dotnet build
   ```

4. **Run the application**
   ```bash
   dotnet run
   ```

## Usage

### Main Menu Navigation
Upon starting the application, you'll see the main menu:

```
=== PADEL SHOP MANAGER ===

1. Rakiety
2. Pilki  
3. Ubrania
4. WyjÅcie

Wybierz opcjÄ (1-4):
```

### Managing Products

1. **Adding Items**: Select a category and choose "Dodaj" option
2. **Viewing Items**: Select "WyÅwietl wszystkie" to see all items in a category
3. **Removing Items**: Choose "UsuÅ" and enter the item ID to remove

### Data Entry Examples

**Adding a Racket:**
- Brand: "Babolat"
- Model: "Drive Max 110" 
- Price: "299.99"

**Adding Clothing:**
- Name: "Professional Polo Shirt"
- Size: "L"
- Price: "79.99"

## Project Structure

```
PadelShopManager/
âââ Program.cs              # Main application file
âââ README.md              # Project documentation
âââ rackets.txt           # Rackets data storage
âââ balls.txt             # Balls data storage
âââ shirts.txt            # Shirts data storage
âââ shorts.txt            # Shorts data storage
âââ shoes.txt             # Shoes data storage
```

### Code Architecture

- **Structs**: `Racket`, `Ball`, `Shirt`, `Shorts`, `Shoes`
- **Data Arrays**: Static arrays with 100-item capacity per category
- **File Operations**: Load/Save methods for each product type
- **UI Methods**: Menu systems and CRUD operations

## Data Storage

The application uses simple CSV format for data persistence:

**Rackets format:** `id,brand,model,price`
```
1,Babolat,Drive Max 110,299.99
2,Wilson,Pro Staff,449.00
```

**Clothing format:** `id,name,size,price`
```
1,Professional Polo,L,79.99
2,Court Shorts,M,59.99
```

**Balls format:** `id,name,price`
```
1,Tournament Ball Set,25.99
2,Training Balls,18.50
```

## Screenshots

*Console interface example:*
```
=== ZARZÄDZANIE RAKIETAMI ===

1. WyÅwietl wszystkie
2. Dodaj
3. UsuÅ
4. Cofnij

Wybierz opcjÄ (1-4):
```

## Project Status

ð¢ **Active Development**

**Completed Features:**
- â Full CRUD operations for all product categories
- â Data persistence with CSV files
- â Polish UI with English codebase
- â Input validation and error handling

**Potential Future Enhancements:**
- ð Database integration (SQLite/SQL Server)
- ð Product search and filtering
- ð Sales reporting features
- ð Multi-language support
- ð GUI version (WPF/WinForms)

## Learning Objectives

This project demonstrates:
- **File I/O operations** in C#
- **Struct-based data modeling**
- **Console application development**
- **Data validation** and user input handling
- **Menu-driven application** architecture
- **CSV data format** handling

## Author

**Your Name**
- GitHub: [@yourusername](https://github.com/yourusername)
- Email: your.email@example.com

---

*This project was created as part of learning C# programming and console application development.* 
