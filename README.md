# NOC Resume Analyzer
# NOC Resume Analyzer - Automated Immigration Assessment

An intelligent n8n workflow that automates Canadian immigration assessment by extracting NOC (National Occupational Classification) codes from PDF resumes using AI-powered analysis.

## 🎯 Overview

This automation workflow streamlines the immigration consultant process by:
- **PDF Resume Processing**: Extracts text from uploaded resume PDFs
- **AI-Powered Analysis**: Uses GPT-4o Mini to identify job roles and match NOC codes
- **Structured Data Extraction**: Formats candidate information for assessment
- **Database Storage**: Stores results in local n8n database for analysis

## 🚀 Features

- **Automated NOC Code Matching**: AI identifies primary and secondary NOC codes for each role
- **Comprehensive Data Extraction**: Captures education, skills, certifications, and work history
- **TEER Level Classification**: Determines skill levels for immigration eligibility
- **Email Integration**: Form-based resume submission system
- **Local Database**: No external dependencies for data storage

## 🛠️ Technical Stack

- **Automation Platform**: n8n (workflow orchestration)
- **AI Model**: GPT-4o Mini via OpenRouter API
- **PDF Processing**: Native n8n PDF text extraction
- **Database**: n8n built-in database
- **Memory**: Simple conversation memory for context
- **Form Interface**: n8n form trigger for resume uploads

## 📋 Prerequisites

- n8n installed and running
- OpenRouter API key (for GPT-4o Mini access)
- Basic understanding of Canadian NOC codes

## ⚙️ Installation

1. **Clone this repository:**
git clone https://github.com/ussyberry/noc-match-mvp.git
cd noc-match-mvp

2. **Import workflow into n8n:**
- Open n8n interface
- Go to Templates → Import
- Select `workflows/noc-resume-analyzer.json`

3. **Configure API credentials:**
- Add OpenRouter API key in OpenRouter Chat Model node
- Configure email settings if using notifications

4. **Test the workflow:**
- Upload a sample resume PDF via the form
- Verify NOC codes are extracted and stored

## 📊 Workflow Architecture

📄 Resume Upload → 📝 PDF Extraction → 🤖 AI Analysis → ⚙️ Data Parser → 💾 Database Storage

### Node Breakdown:

- **📄 Resume Upload Form**: Web form for PDF submissions
- **📝 PDF Text Extraction**: Converts PDF to text
- **🤖 NOC Code Analyzer**: AI agent for job role analysis
- **⚙️ Data Parser & Formatter**: Structures extracted data
- **💾 Resume Database Storage**: Stores results locally

## 🔍 Sample Output

{
"email": "candidate@example.com",
"noc_codes": 65501,
"all_noc_codes": "65501,65301,14101,12203,0122",
"education": "[{"degree":"Bachelor of Business","institution":"University"}]",
"skills": "["Customer Service","Sales","Management"]",
"certifications": "["PMP Certification"]"
}

## 🎯 Use Cases

- **Immigration Consultants**: Automate initial candidate assessment
- **HR Departments**: Screen international candidates
- **Career Counselors**: Identify skill gaps for Canadian market
- **Recruitment Agencies**: Match candidates to NOC-specific roles

## 📈 Business Value

- **Time Savings**: Reduces manual resume review from hours to minutes
- **Accuracy**: Consistent NOC code identification across candidates
- **Scalability**: Process multiple resumes simultaneously
- **Data Structure**: Standardized format for further analysis

## 🛡️ Data Privacy

- All processing done locally in n8n
- No external data storage (except OpenRouter API calls)
- Resumes processed in memory, not permanently stored
- Compliant with Canadian privacy regulations

## 🔧 Customization

- **NOC Code Database**: Extend with additional classification rules
- **AI Prompts**: Modify for specific industry focus
- **Output Format**: Adapt database schema for custom needs
- **Integration**: Connect to external CRM or assessment tools

## 📚 Documentation

- [Setup Guide](docs/setup-guide.md) - Detailed installation instructions
- [API Configuration](docs/api-setup.md) - OpenRouter integration
- [NOC Code Reference](docs/noc-codes.md) - Canadian classification system

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/enhancement`)
3. Commit changes (`git commit -am 'Add new feature'`)
4. Push branch (`git push origin feature/enhancement`)
5. Create Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**Usman Alex Kadiri**
- GitHub: [@ussyberry](https://github.com/ussyberry)
- Email: usman.kadiri@gmail.com
- Specializing in API integrations, n8n automation, and immigration technology

---

*Built with ❤️ for the Canadian immigration community*
