# HealthCare Pro - Healthcare Management System

A comprehensive, futuristic healthcare management web application built with HTML, CSS, JavaScript, and Firebase. This system provides complete patient management, appointment scheduling, prescription management, and medical history tracking.

## 🌟 Features

### Core Functionality
- **Authentication & Authorization**
  - Secure login and sign-up system
  - Role-based access control (Patient, Doctor, Receptionist, Admin)
  - Protected routes and user validation

- **Patient Management**
  - Add new patients with detailed information
  - Edit patient records
  - View patient profiles with complete details
  - Search patients by name, email, or phone
  - Customer information validation

- **Appointment Management**
  - Book appointments with doctors
  - View appointment schedules
  - Update appointment status (Pending, Confirmed, Completed, Cancelled)
  - Cancel appointments
  - Doctor schedule view
  - Appointment history timeline

- **Prescription System**
  - Create prescriptions with multiple medicines
  - Manage medicine details (name, dosage, frequency, duration)
  - Add clinical notes
  - Generate professional PDF prescriptions
  - Download prescriptions as PDF files
  - Track prescription history

- **Medical History Timeline**
  - Complete medical history for each patient
  - Timeline view of all medical events
  - Appointment history
  - Prescription history
  - Diagnosis tracking
  - Timestamp tracking for all records

### UI/UX
- **Futuristic Design**
  - Modern dark theme with vibrant accent colors
  - Smooth animations and transitions
  - Responsive layout for all devices
  - Intuitive navigation
  - Real-time notifications

- **Dashboard**
  - Overview statistics and metrics
  - Recent activity feed
  - Quick access to main features
  - Role-specific views

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Firebase account with Firestore database enabled

### Installation

1. **Clone or Download the Project**
   ```bash
   # Unzip the project files to your desired location
   ```

2. **Open in Browser**
   - Navigate to the project folder
   - Open `index.html` in your web browser
   - Or use a local server:
     ```bash
     # Using Python 3
     python -m http.server 8000
     
     # Using Node.js (if you have http-server installed)
     npx http-server
     
     # Using PHP
     php -S localhost:8000
     ```

3. **Access the Application**
   - Open `http://localhost:8000` in your browser
   - You'll be redirected to the login page

### Firebase Setup

The application is pre-configured with Firebase credentials. If you want to use your own Firebase project:

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Create a new project
3. Enable Firestore Database (in Native mode)
4. Enable Authentication (Email/Password)
5. Update the Firebase config in `js/firebase-config.js`:
   ```javascript
   const firebaseConfig = {
       apiKey: "YOUR_API_KEY",
       authDomain: "YOUR_AUTH_DOMAIN",
       projectId: "YOUR_PROJECT_ID",
       storageBucket: "YOUR_STORAGE_BUCKET",
       messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
       appId: "YOUR_APP_ID"
   };
   ```

## 📋 How to Use

### 1. Authentication

**Sign Up:**
1. Click "Sign Up" tab on the login page
2. Enter your details:
   - Full Name
   - Email Address
   - Password (minimum 6 characters)
   - Select your Role (Patient, Doctor, Receptionist, Admin)
3. Click "Create Account"
4. You'll be redirected to the dashboard

**Login:**
1. Enter your email and password
2. Click "Login to Account"
3. You'll access the dashboard

### 2. Patient Management

**Add a Patient:**
1. Navigate to "Patients" from the sidebar
2. Click "+ Add Patient" button
3. Fill in the form:
   - Full Name
   - Email
   - Phone Number
   - Date of Birth
   - Gender
   - Address (optional)
4. Click "Add Patient"

**View Patient Details:**
1. In the Patients section, click "View" button next to a patient
2. See complete patient information and medical history

**Edit Patient:**
1. Click "Edit" button next to a patient
2. Update the information
3. Click "Save" to apply changes

**Search Patients:**
1. Use the search bar in the Patients section
2. Type name, email, or phone number
3. Results filter in real-time

### 3. Appointment Management

**Book an Appointment:**
1. Navigate to "Appointments" from the sidebar
2. Click "+ Book Appointment" button
3. Fill in the form:
   - Select Patient
   - Doctor Name
   - Appointment Date & Time
   - Appointment Type
   - Reason for appointment
4. Click "Book Appointment"

**Update Appointment Status:**
1. In the Appointments section, click "Update" button
2. Enter the new status:
   - pending
   - confirmed
   - completed
   - cancelled
3. Appointment updates automatically

**View Doctor Schedule:**
1. Go to the Appointments section
2. See all appointments with doctor information
3. Filter by status using the table

**Cancel Appointment:**
1. Click "Delete" button next to an appointment
2. Confirm the cancellation

### 4. Prescription Management

**Create a Prescription:**
1. Navigate to "Prescriptions" from the sidebar
2. Click "+ Create Prescription" button
3. Select a patient and enter doctor name
4. Add medicines:
   - Click "+ Add Medicine"
   - Enter medicine name (e.g., Aspirin)
   - Enter dosage (e.g., 500mg)
   - Enter frequency (e.g., 3 times daily)
   - Set duration in days
5. Add any additional notes
6. Click "Create Prescription"

**Download Prescription as PDF:**
1. In the Prescriptions section, find the prescription
2. Click "Download" button
3. The PDF is generated and downloaded to your computer
4. PDF includes:
   - Patient information and age
   - Doctor information
   - All prescribed medicines with dosage and frequency
   - Clinical notes
   - Professional formatting

**View Prescription History:**
1. Go to "Prescriptions" section
2. See all prescriptions with patient and doctor names
3. Medicine count and creation date displayed

### 5. Medical History Timeline

**View Complete Timeline:**
1. Navigate to "Medical History" from the sidebar
2. See a chronological timeline of all medical events
3. View appointments, prescriptions, and diagnoses
4. Each entry shows:
   - Type of event (appointment, prescription, diagnosis)
   - Patient name
   - Description and details
   - Date and time
   - Current status

### 6. Dashboard Overview

**Statistics:**
- Total number of patients
- Total appointments
- Total prescriptions
- Pending appointments count

**Recent Activity:**
- Recent appointments feed
- Recent prescriptions feed
- Quick overview of latest entries

### 7. Profile Settings

**Update Profile:**
1. Click "Profile Settings" in the sidebar
2. Edit your profile information:
   - Change your display name
   - View email and role information
3. Click "Save Changes"

## 🎨 Design Features

### Color Scheme
- **Primary Blue**: #1e88e5 (Main actions)
- **Secondary Teal**: #26a69a (Secondary actions)
- **Accent Red**: #ff6b6b (Important alerts)
- **Dark Background**: #0f1419 (Night mode)
- **Card Background**: #1a1f28

### UI Components
- **Cards**: Information containers with hover effects
- **Buttons**: Multiple styles (Primary, Secondary, Ghost, Danger)
- **Badges**: Status indicators with color coding
- **Modals**: Interactive forms and dialogs
- **Timeline**: Medical history visualization
- **Tables**: Responsive data display
- **Notifications**: Toast alerts for user feedback

## 🔐 Security

- **Firebase Authentication**: Secure user verification
- **Firestore Rules**: Database access control (Configure in Firebase Console)
- **Input Validation**: Client-side validation for all forms
- **Session Management**: Automatic logout on browser close (optional)
- **Role-Based Access**: Different features for different user roles

### Recommended Firestore Rules
```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    // Users collection
    match /users/{uid} {
      allow read, write: if request.auth.uid == uid;
    }
    
    // Patients collection
    match /patients/{document=**} {
      allow read: if request.auth != null;
      allow write: if request.auth != null && 
                      (request.auth.token.role == 'doctor' || 
                       request.auth.token.role == 'admin' ||
                       request.auth.token.role == 'receptionist');
    }
    
    // Similar rules for other collections
  }
}
```

## 📱 Responsive Design

- **Desktop**: Full-featured experience with sidebar navigation
- **Tablet**: Optimized layout for medium screens
- **Mobile**: Touch-friendly interface with collapsible menu

## 🔧 Technical Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Backend**: Firebase (Authentication + Firestore)
- **PDF Generation**: jsPDF library
- **Features**: Real-time updates, offline support

## 📁 Project Structure

```
├── index.html              # Login/signup page
├── dashboard.html          # Main dashboard
├── css/
│   └── style.css          # All styling (futuristic theme)
├── js/
│   ├── firebase-config.js # Firebase initialization
│   ├── auth.js            # Authentication logic
│   ├── patients.js        # Patient management
│   ├── appointments.js    # Appointment management
│   ├── prescriptions.js   # Prescription management
│   ├── utils.js           # Utility functions
│   └── dashboard.js       # Dashboard logic
└── README.md              # This file
```

## 🐛 Troubleshooting

### Login Issues
- **"User not found"**: Check if you've signed up first
- **"Wrong password"**: Verify your password
- **Cannot create account**: Ensure email hasn't been used and password is 6+ characters

### Data Not Loading
- Check browser console for errors (F12)
- Verify Firebase credentials are correct
- Ensure browser has internet connection
- Clear browser cache and reload

### PDF Not Generating
- Verify jsPDF library is loaded
- Check for browser popup blockers
- Try a different browser

### Modal Not Opening
- Refresh the page
- Clear browser cache
- Check if JavaScript is enabled

## 🚀 Future Enhancements

- Email notifications for appointments
- SMS alerts
- Video consultation integration
- AI-powered diagnosis suggestions
- Advanced analytics and reporting
- Multi-language support
- Voice prescriptions
- Integration with payment systems

## 📞 Support

For issues or questions:
1. Check browser console for error messages
2. Verify all files are in correct folders
3. Test with a different browser
4. Check Firebase project settings

## 📄 License

This project is provided as-is for healthcare management purposes. Ensure compliance with local healthcare regulations (HIPAA, GDPR, etc.) when deploying in production.

## ⚠️ Important Notes

1. **Data Privacy**: Implement proper encryption and access controls in production
2. **HIPAA Compliance**: If used in the US, implement HIPAA-compliant features
3. **Backup**: Regularly backup your Firestore database
4. **Testing**: Thoroughly test with sample data before production use
5. **Authentication**: Consider multi-factor authentication for production

## 🎉 Getting Started Checklist

- [ ] Download/clone the project
- [ ] Open index.html in browser or use local server
- [ ] Create an account with a test role
- [ ] Add a test patient
- [ ] Book a test appointment
- [ ] Create a test prescription
- [ ] Download and view the PDF
- [ ] Check the medical history timeline
- [ ] Explore all features

---

**HealthCare Pro** - Making Healthcare Management Simple and Efficient ✨
