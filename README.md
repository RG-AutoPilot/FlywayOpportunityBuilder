# Flyway Demo Scoper - Opportunity Builder

A collaborative web-based tool for scoping Flyway database migration opportunities and calculating ROI estimates. This tool helps teams assess their current database development and deployment processes, identify pain points, and estimate potential time savings from implementing Flyway.

![Flyway Demo Scoper Interface](https://github.com/user-attachments/assets/4d75a0ec-df89-4a42-a73b-761fec9c1384)

## Overview

The Flyway Demo Scoper is designed to be used collaboratively during client calls or internal assessments to:

- **Capture current state**: Document how teams currently handle database changes, version control, and deployments
- **Identify pain points**: Surface specific challenges in development, script generation, and deployment processes  
- **Estimate ROI**: Calculate potential time savings and productivity improvements from Flyway adoption
- **Generate summaries**: Create engineer-ready briefs for follow-up discussions and implementation planning

## Key Features

### 📋 Comprehensive Assessment Sections
1. **Company & Context** - Basic project information, database platforms, hosting, and release cadence
2. **Development & Version Control** - Current versioning practices, developer workflows, and pain points
3. **Deployment Script Generation** - How scripts are created, preparation times, and challenges
4. **Deployment & Release** - Deployment methods, timings, failure rates, and friction points
5. **Priorities & Success Criteria** - Key issues to solve and 90-day success metrics

### 💰 Real-time ROI Calculations
- **Development Sync & Capture Savings** - Time saved on version control workflows
- **Script Preparation Savings** - Reduced effort in deployment script generation  
- **Deployment Savings** - Faster, more reliable deployments with fewer failures
- Assumes ~50% time reduction when pain points are present (customizable)

### 🔄 Data Persistence & Export
- **Auto-save**: Form data automatically saved to browser localStorage
- **JSON Export/Import**: Save assessments as JSON files for later review
- **Copy Summary**: Generate and copy engineer-ready briefs to clipboard
- **Print/PDF**: Export completed assessments for documentation

### 🎨 User Experience
- Clean, modern dark theme interface
- Responsive design for various screen sizes
- Live progress tracking as form is completed
- Real-time ROI calculations as data is entered

## Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No server setup required - runs entirely in the browser

### Usage

1. **Open the application**: Open `FlywayOpp.html` in your web browser
2. **Fill out the form**: Work through each section collaboratively with your team
3. **Review ROI estimates**: Watch the calculations update in real-time
4. **Export results**: Use the "Copy Summary" button or download JSON for follow-up

### Running Locally

```bash
# Clone the repository
git clone https://github.com/RG-AutoPilot/FlywayOpportunityBuilder.git

# Navigate to the directory
cd FlywayOpportunityBuilder

# Serve the file (optional, for better security)
python3 -m http.server 8000

# Open in browser
# Direct: file:///path/to/FlywayOpp.html  
# Or via server: http://localhost:8000/FlywayOpp.html
```

## File Structure

```
FlywayOpportunityBuilder/
├── README.md              # This documentation
├── FlywayOpp.html         # Main application file (standalone)
└── .vs/                   # Visual Studio settings (can be ignored)
```

## Technical Details

- **Technology**: Pure HTML, CSS, and JavaScript (no external dependencies)
- **Browser Storage**: Uses localStorage for auto-save functionality
- **Data Format**: JSON for import/export operations
- **Responsive Design**: CSS Grid and Flexbox for mobile-friendly layouts
- **Accessibility**: ARIA labels and semantic HTML structure

## ROI Calculation Model

The tool uses a simplified model for ROI estimation:

```javascript
// Example calculation logic
const devSavings = painPoints.length > 0 ? currentTime * 0.5 : 0;
const monthlySavings = devSavings * developersCount * changesPerMonth;
```

**Key Assumptions:**
- ~50% time reduction when pain points are identified
- Calculations based on provided developer counts and change frequencies
- Estimates should be refined with organization-specific benchmarks

## Use Cases

### Sales & Presales
- Client discovery calls and assessments
- ROI justification for Flyway adoption
- Competitive analysis and positioning

### Internal Teams
- Current state assessment for migration planning
- Process improvement identification
- Success metrics definition

### Customer Success
- Health checks and optimization opportunities
- Renewal discussions with ROI evidence
- Implementation planning sessions

## Customization

The tool can be customized by modifying `FlywayOpp.html`:

- **Pain Points**: Update checkbox options in each section
- **ROI Model**: Adjust calculation logic in the `roiMinutes()` function
- **Styling**: Modify CSS variables for branding
- **Form Fields**: Add or remove assessment criteria

## Contributing

1. Fork the repository
2. Make your changes to `FlywayOpp.html`
3. Test thoroughly in multiple browsers
4. Submit a pull request with a clear description

## License

This project is part of the RG-AutoPilot organization. Please refer to your organization's licensing policies.

## Support

For questions or issues:
1. Check the existing GitHub issues
2. Create a new issue with detailed information
3. Contact the RG-AutoPilot team for internal support
