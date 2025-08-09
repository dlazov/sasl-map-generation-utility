# SASL Map Generation Utility

A comprehensive collection of web-based tools for generating random map selections for **Solitaire Advanced Squad Leader (SASL)** board games. These utilities implement the official SASL tables and dice rolling mechanics to help players quickly generate appropriate maps for their scenarios.

## 🎯 Overview

This project provides four specialized HTML utilities that generate random map selections based on SASL's official terrain selection and mapboard tables. Each utility covers different map categories and includes advanced filtering options, intelligent mate pair detection, and visual styling enhancements.

## 🗂️ Utilities Included

### 1. **SASL Map Selection - All Maps** (`SASL_Map_Selection_Expanded_All.html`)
The most comprehensive utility covering all available SASL maps from multiple publishers:
- **Coverage**: MMP, BFP, LFT, Friendly Fire, and Hazmat maps
- **Table Size**: 82 entries (expanded from original 60)
- **Filters**: BFP, FrF, Haz, DW (Double-Wide), Rivers
- **Dice System**: rollD82() for maximum coverage

### 2. **SASL Geo Map Selection - MMP** (`SASL_Geo_Map_Selection_MMP.html`)
Focused on MMP's geographic maps with historic numbered pairs:
- **Coverage**: Maps 1-92 and SK boards g-h
- **Table Size**: 48 entries
- **Filters**: DW (Double-Wide), Rivers
- **Special Features**: Historic numbered pairs (64/65, 80/81, 82/83, 87/88)
- **Dice System**: rollD48() for MMP-specific coverage

### 3. **SASL Map Selection - Double Wide** (`SASL_Map_Selection_Double_Wide_All.html`)
Specialized for double-wide map selections:
- **Coverage**: Double-wide maps from MMP and BFP
- **Table Size**: 22 entries
- **Filters**: BFP, DW (Double-Wide)
- **Focus**: Mated board pairs and double-wide scenarios
- **Dice System**: rollD22() for double-wide specific maps

### 4. **SASL Map Selection - "Fort" Style** (`SASL_Map_Selection_Fort_Style_MMP.html`)
Dedicated to the "Fort"-style maps using the "a/b" format:
- **Coverage**: Fort maps 1a/b through 22a/b
- **Table Size**: 15 entries
- **Format**: Uses "a/b" notation instead of "(mates with)" text
- **Dice System**: rollD15() for fort-style coverage

## ✨ Key Features

### 🎲 **Intelligent Dice Rolling**
- Implements official SASL 2D6 terrain selection
- Variable dice systems (D15, D22, D48, D82) based on table coverage
- Dice Roll Modifiers (DRM) for both terrain and mapboard selection
- Automatic clamping to valid roll ranges

### 🔗 **Advanced Mate Pair Logic**
- **Automatic Detection**: Recognizes mated board pairs from table data
- **Special Ordering**: Implements correct ordering for specific pairs:
  - Standard numbered: 64→65, 80→81, 82→83, 87→88
  - BFP Double-Wide: 'a' boards always come first (DW1a→DW1b, etc.)
  - BFP Hills: BFP-H→BFP-I ordering
- **Dual Board Generation**: Automatically adds both boards when mate pairs are rolled
- **Clean Display**: Shows board names with DW indicators instead of verbose mate text

### 🎨 **Visual Enhancements**
- **River Highlighting**: Blue styling for river boards
- **Mated Board Indicators**: Bold text with "DW" badges
- **Filter Sections**: Clean checkbox interface for board type filtering
- **Responsive Design**: Works across different screen sizes

### 🔍 **Multi-Category Filtering**
- **BFP Filter**: Include/exclude Bounding Fire Productions maps
- **FrF Filter**: Include/exclude Friendly Fire maps  
- **Haz Filter**: Include/exclude Hazmat maps
- **DW Filter**: Include/exclude double-wide/mated boards
- **Rivers Filter**: Include/exclude river boards
- **Recursive Rerolling**: Automatically rerolls when filtered board types are generated

### 🎯 **Smart Board Generation**
- **Terrain-Based Selection**: Uses official SASL terrain categories
- **Map Alignment**: Random North/South orientation (South for special pairs)
- **Board Counting Logic**: Handles mate pairs in board count calculations
- **Reroll Functionality**: Individual board rerolling with same parameters

## 🚀 Usage

1. **Open any HTML file** in a web browser
2. **Select terrain category** from the dropdown (Standard A8a, Urban A8b, etc.)
3. **Choose number of boards** to generate (1-10)
4. **Set dice roll modifiers** for terrain and mapboard selection
5. **Configure filters** using checkboxes to exclude unwanted board types
6. **Click "Generate Terrain"** to create your map selection
7. **Use "Reroll" buttons** to regenerate individual mapboards

## 📋 Technical Implementation

### **XML Data Structure**
- **TableA8**: Terrain selection with roll ranges and terrain types
- **TableA9**: Mapboard selection with comprehensive board listings
- **Embedded Data**: All tables embedded as XML strings for offline use

### **JavaScript Architecture**
- **Modular Functions**: Separate functions for parsing, generation, and display
- **DOM Manipulation**: Dynamic table generation and updates
- **Event Handling**: Interactive reroll buttons and filter checkboxes
- **Input Validation**: Roll clamping and error handling

### **CSS Styling Framework**
- **Progressive Enhancement**: Builds from basic to advanced styling
- **Specialized Classes**: `.river-text`, `.mated-board`, `.dw-indicator`
- **Filter Interface**: `.filter-section`, `.checkbox-label` for clean UI
- **Responsive Layout**: Flexible container and table designs

## 🎮 SASL Integration

These utilities implement the official **SASL 2nd Edition** rules:
- **Chapter A8**: Terrain Selection tables and procedures
- **Chapter A9**: Mapboard Selection tables and dice mechanics
- **2nd Edition Updates**: Expanded map coverage and updated board listings
- **Publisher Integration**: Supports MMP, BFP, LFT, Friendly Fire, and Hazmat maps

## 📖 Background

Originally developed by **Steve P. Inman** for 1st edition SASL, these utilities have been extensively updated by **Don Lazov** (August 8, 2025) to support:
- 2nd edition SASL tables and expanded map coverage
- Modern web standards and responsive design
- Advanced filtering and mate pair detection
- Enhanced visual feedback and user experience

## 📄 License

This project is licensed under the **GNU General Public License v3.0**. See the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests to improve these utilities.

---

*Perfect for SASL players who want quick, accurate map generation with the flexibility to customize their selections based on available maps and scenario requirements.*