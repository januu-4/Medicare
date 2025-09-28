# MediReportInterpreter Design Guidelines

## Design Approach: Healthcare System-Based
**Selected Approach**: Design System (Material Design + Healthcare adaptations)
**Justification**: Healthcare applications require trust, accessibility, and information clarity. Material Design provides excellent patterns for data-heavy interfaces with strong visual hierarchy.

## Core Design Elements

### A. Color Palette
**Primary Colors**:
- Light Mode: 210 100% 50% (medical blue)
- Dark Mode: 210 80% 60% (softer blue for reduced eye strain)

**Secondary Colors**:
- Success/Health: 120 60% 50% (calming green)
- Warning/Attention: 35 90% 55% (amber for alerts)
- Error/Critical: 0 70% 50% (medical red)

**Neutral Palette**:
- Light Mode: 210 15% 98% (background), 210 10% 15% (text)
- Dark Mode: 210 15% 8% (background), 210 5% 95% (text)

### B. Typography
**Font Family**: Inter via Google Fonts CDN
- Headers: 600-700 weight for authority and trust
- Body: 400-500 weight for readability
- Medical data: 500 weight for emphasis
- Captions: 400 weight

### C. Layout System
**Spacing Units**: Tailwind spacing of 4, 6, 8, 12, 16
- Component padding: p-6, p-8
- Section margins: mb-12, mt-16
- Element spacing: gap-4, gap-6

### D. Component Library

**Navigation**:
- Clean sidebar with medical iconography (Heroicons medical set)
- Breadcrumb navigation for report sections
- Tab-based navigation for report analysis views

**Data Display**:
- Card-based layout for report summaries
- Table components for extracted medical values with color-coded ranges
- Timeline components for health trends using Recharts line charts
- Progress indicators for OCR processing status

**Forms & Upload**:
- Drag-and-drop upload zones with medical document icons
- Form validation with inline feedback
- File preview cards with processing status indicators

**Chat Interface**:
- WhatsApp-style chat bubbles with medical professional avatars
- Timestamp formatting optimized for medical consultations
- Status indicators for message delivery and read receipts

**Alerts & Reminders**:
- Toast notifications for medication reminders
- Banner alerts for critical health values
- Badge indicators for unread messages/reports

### E. Healthcare-Specific Patterns

**Trust Indicators**:
- Security badges for data privacy
- Professional certifications display
- Encryption status indicators

**Medical Data Visualization**:
- Color-coded health ranges (green/yellow/red zones)
- Trend arrows for improving/declining metrics
- Reference range displays alongside patient values

**Accessibility**:
- High contrast mode support for vision-impaired users
- Large touch targets for elderly patients
- Screen reader optimized content structure

## Images Section
**Hero Image**: Large medical consultation image showing doctor-patient interaction with digital reports
**Report Thumbnails**: Preview images of sample medical reports (lab results, prescriptions)
**Feature Icons**: Medical iconography for upload, analysis, chat, and reminder features
**Doctor Avatars**: Professional headshots for chat interface (placeholder images)
**Health Charts**: Sample visualization screenshots showing trend analysis