# OneTable

![OneTable Logo](https://raw.githubusercontent.com/metagamma/OneTable/main/assets/logo.svg)

OneTable is a powerful Windows desktop application that streamlines the process of migrating Excel data to SQLite databases. Built with .NET 8, it enables users to efficiently handle multiple Excel files simultaneously, converting worksheets into queryable SQLite tables for enhanced data analysis and reporting capabilities.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![.NET](https://img.shields.io/badge/.NET-8.0-purple.svg)](https://dotnet.microsoft.com/download/dotnet/8.0)

## 🚀 Features

- **Multiple File Processing**: Import unlimited Excel files (.xlsx, .xls) simultaneously
- **Sheet Management**: Process multiple worksheets from each Excel file
- **Automated Table Creation**: Automatic SQLite table generation with appropriate schema
- **Data Type Inference**: Smart detection of column types
- **Progress Tracking**: Real-time progress monitoring during migration
- **User-Friendly Interface**: Clean and intuitive Windows Forms interface
- **Transaction Support**: Secure data migration with SQL transaction handling
- **Error Handling**: Robust error management and user feedback

## 📋 Prerequisites

- Windows OS (Windows 10 or later recommended)
- .NET 8.0 Runtime

## 🔧 Installation

### Option 1: Using the Installer

1. Download the latest installer from the [Releases](https://github.com/metagamma/OneTable/releases) page
2. Run the installer and follow the setup wizard
3. Launch OneTable from the Start menu

### Option 2: Building from Source

```bash
# Clone the repository
git clone https://github.com/metagamma/OneTable.git

# Navigate to the project directory
cd OneTable

# Restore NuGet packages
dotnet restore

# Build the solution
dotnet build

# Run the application
dotnet run
```

## 🌐 Supported Languages

OneTable's interface is available in multiple languages to serve a global user base:

### Currently Supported

| Language   | Code | Status             | Completion |
|------------|------|-------------------|------------|
| English    | en   | ✅ Complete        | 100%       |
| Spanish    | es   | ✅ Complete        | 100%       |
| French     | fr   | ✅ Complete        | 100%       |
| Portuguese | pt   | ✅ Complete        | 100%       |
| German     | de   | ✅ Complete        | 100%       |

## 📦 Dependencies

- System.Data.SQLite (1.0.119)
- NPOI (2.7.1)

## 🛠️ Usage

1. **Launch the Application**
   - Open OneTable from your Start menu or desktop shortcut

2. **Add Excel Files**
   - Click "Add Excel" button
   - Select one or multiple Excel files
   - Added files will appear in the list on the left

3. **Configure Migration (Optional)**
   - Select specific sheets to migrate
   - Configure column data types
   - Set custom table names

4. **Process Files**
   - Click "Process Files" button
   - Monitor progress in the status bar
   - Wait for completion message

5. **Access Your Data**
   - Find the generated SQLite database in the application folder
   - Use your preferred SQLite client to query the data

## Database Structure

Each Excel worksheet is converted into a separate SQLite table with the following naming convention:
```
[ExcelFileName]_[SheetName]
```

Example:
```sql
-- For a file named "Sales2024.xlsx" with sheet "Q1"
CREATE TABLE [Sales2024_Q1] (
    [ID] INTEGER,
    [Date] TEXT,
    [Amount] REAL,
    -- Additional columns...
);
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Roadmap

- [ ] Advanced data type mapping
- [ ] Custom SQL query builder
- [ ] Excel template support
- [ ] Data validation rules
- [ ] Export capabilities
- [ ] Batch processing optimization

---

**Note**: OneTable is currently in active development. While we strive for stability, please backup your data before processing important files.