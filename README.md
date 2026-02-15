# Economic Survey 2025-26 - Interactive Study Guide

An interactive web application to study and master India's Economic Survey 2025-26.

## 📊 Overview

This project provides a comprehensive, interactive platform for studying the Economic Survey 2025-26 published by the Government of India. The application features:

- **Dashboard** with key facts and economic scenarios
- **17 Chapters** with structured summaries
- **Complete chapter content** with expandable sections
- **Progress tracking** to monitor your learning
- **Personal notes** system with export functionality
- **Mobile-responsive** design

## 🎯 Features

### Dashboard
- Critical economic context and key messages
- Essential statistics (GDP growth, fiscal deficit, tariffs, etc.)
- Three scenarios for 2026 with probability analysis

### Study Chapters
- 17 comprehensive chapters covering all aspects of the economy
- Executive summaries for quick understanding
- Key points highlighting critical information
- "Why it matters" explanations for career relevance

### Complete Content
- Full chapter text from the official PDF
- Expandable sections for detailed reading
- Improved readability with proper formatting
- Easy navigation and search

### Progress Tracking
- Mark chapters as complete
- Visual progress indicator
- Track your learning journey

### Notes System
- Take notes for each chapter
- Auto-save functionality
- Export notes as text files
- Persistent storage using browser localStorage

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- No installation required - it's a single HTML file!

### Usage

1. **Open the file**: Simply open `index.html` in your web browser
2. **Start with Dashboard**: Review key facts and scenarios
3. **Study chapters**: Click any chapter to view detailed content
4. **Take notes**: Write notes as you study each chapter
5. **Track progress**: Mark chapters complete as you finish them

## 📚 Chapter Structure

The Economic Survey is organized into 17 chapters:

1. **State of the Economy** - Macroeconomic overview and global scenarios
2. **Fiscal Policy** - Government finances and fiscal consolidation
3. **Monetary & Financial** - RBI policy and banking sector
4. **External Sector** - Trade, balance of payments, and forex
5. **Prices & Inflation** - Inflation trends and outlook
6. **Agriculture** - Food security and productivity
7. **Services Sector** - IT, financial services, and exports
8. **Manufacturing** - PLI schemes and Make in India
9. **Infrastructure** - Transport, energy, and digital infrastructure
10. **Climate & Environment** - Green transition and sustainability
11. **Human Development** - Education and healthcare
12. **Employment & Skills** - Job creation and skilling
13. **Social Inclusion** - Poverty reduction and inequality
14. **Artificial Intelligence** - AI strategy (Special Essay)
15. **Urban Development** - Cities and governance (Special Essay)
16. **Strategic Autonomy** - Self-reliance (Special Essay)
17. **State Capacity** - Governance effectiveness (Special Essay)

## 💻 Technical Details

- **Single-page application** built with vanilla HTML, CSS, and JavaScript
- **No external dependencies** - works completely offline
- **Dynamic content loading** from JSON files for better maintainability
- **localStorage** for data persistence
- **Responsive design** for mobile, tablet, and desktop
- **FontAwesome icons** for enhanced UI (CDN)

### Architecture

The application uses a hybrid approach:
- **Structured Data**: Chapter content stored in JSON files (`chapter_01.json` to `chapter_17.json`)
- **Dynamic Rendering**: JavaScript fetches and renders JSON content on-demand
- **Fallback Support**: Hardcoded HTML content available if JSON loading fails
- **Client-side Only**: No server required, runs entirely in the browser

See [JSON_FORMAT.md](JSON_FORMAT.md) for detailed information about the chapter data schema.

## 📖 Data Source

Content extracted from the official Economic Survey 2025-26 PDF published by the Government of India, Ministry of Finance.

## 🎓 Use Cases

- **Students** preparing for competitive exams (UPSC, State PCS)
- **Professionals** working in economics, policy, or finance
- **Researchers** studying Indian economy
- **Journalists** covering economic news
- **Policy analysts** understanding government priorities

## 🛠️ Development

### Project Structure
```
economic-survey-2025-26/
├── index.html          # Main application file
├── chapter_01.json     # Chapter 1 data (State of the Economy)
├── chapter_02.json     # Chapter 2 data (Fiscal Policy)
├── ...                 # Chapters 3-16
├── chapter_17.json     # Chapter 17 data (State Capacity)
├── JSON_FORMAT.md      # JSON schema documentation
├── README.md           # This file
├── LICENSE             # MIT License
└── .gitignore          # Git ignore rules
```

### Local Development
1. Clone the repository
2. Open `index.html` in your browser (or serve via HTTP server)
3. Make changes to JSON files or HTML file
4. Refresh browser to see updates

**Note**: Chapter content is now loaded dynamically from JSON files. To add or modify chapter content, edit the corresponding `chapter_XX.json` file. See `JSON_FORMAT.md` for schema details.

## 📝 License

MIT License - Feel free to use, modify, and distribute

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests
- Improve documentation

## 📞 Support

For questions or issues, please open a GitHub issue.

## 🙏 Acknowledgments

- Government of India, Ministry of Finance for publishing the Economic Survey
- All contributors and users of this project

---

**Disclaimer**: This is an unofficial study tool. For official information, please refer to the Economic Survey 2025-26 published by the Government of India.
