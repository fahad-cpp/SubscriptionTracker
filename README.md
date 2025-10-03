# SubTracker - Subscription Management System

![SubTracker Logo](https://via.placeholder.com/200x80/3b82f6/ffffff?text=SubTracker)

## 📋 Overview
SubTracker is a **subscription management system** that helps users track, manage, and optimize recurring payments. It provides an intuitive dashboard for monitoring active subscriptions, upcoming payments, and account settings—all in one place.

### 🎯 Key Features
- **Dashboard**: Real-time statistics and quick access to subscriptions  
- **Subscription Management**: Add, edit, cancel, or categorize subscriptions  
- **Payment Tracking**: Calendar & list views for upcoming payments  
- **Smart Notifications**: Email + in-app reminders for due payments  
- **Authentication**: Secure login & registration system  
- **Responsive Design**: Optimized for desktop, tablet & mobile  
- **Data Export**: Export payment history as CSV  
- **User Settings**: Custom preferences & profile management  

---

## 🚀 Live Demo
- [Homepage](./index.html)  
- [Dashboard](./dashboard.html)  
- [Authentication](./auth.html)  
- [Upcoming Payments](./upcoming-payments.html)  
- [Settings](./settings.html)  

**Demo Credentials**  
```
Email: demo@subtracker.com  
Password: demo123
```

---

## 🛠️ Tech Stack

### Frontend
- HTML5, CSS3 (Grid & Flexbox), JavaScript (ES6+)  
- Font Awesome (icons), Google Fonts (Inter)  

### Backend (Integration Ready)
- Node.js + Express.js  
- MongoDB (v4.4+)  
- RESTful APIs  

### Design System
- Mobile-first, responsive layout  
- CSS custom properties for theming  
- Reusable UI components  
- WCAG 2.1 accessibility  

---

## 📂 Project Structure
```
subtracker/
├── index.html                  # Landing page
├── dashboard.html              # Main dashboard
├── auth.html                   # Login/Registration
├── upcoming-payments.html       # Payment calendar & list
├── settings.html                # User settings
├── styles.css                   # Dashboard styles
├── auth.css                     # Authentication styles
├── upcoming-payments.css        # Payment page styles
├── settings.css                 # Settings page styles
├── home.css                     # Landing page styles
├── script.js                    # Dashboard functionality
├── auth.js                      # Authentication logic
├── upcoming-payments.js         # Payment management
├── settings-mobile.js           # Mobile settings interactions
├── upcoming-payments-mobile.js  # Mobile payment interactions
├── home.js                      # Landing page interactions
├── scripts/
│   └── mongodb-setup.js         # DB initialization
├── api/
│   └── payments.js              # Payment API endpoints
└── README.md
```

---

## 🔧 Setup Instructions

### Prerequisites
- Node.js v14+  
- MongoDB v4.4+  
- Modern browser  

### Quick Start (Frontend Only)
```bash
git clone https://github.com/yourusername/subtracker.git
cd subtracker

# Option 1: Python
python -m http.server 8000

# Option 2: Node
npx serve .

# Or open index.html directly
```
Access via `http://localhost:8000`

### Full Setup (With Backend)
```bash
# Install dependencies
npm install express mongodb cors dotenv

# Start MongoDB
mongod
node scripts/mongodb-setup.js

# Configure .env
MONGODB_URI=mongodb://localhost:27017/subtracker
PORT=5000

# Start server
node server.js
```

---

## 📱 Screenshots
| Landing | Dashboard | Authentication |
|---------|-----------|----------------|
| ![Landing](https://via.placeholder.com/400x250/f8fafc/1e293b?text=Landing) | ![Dashboard](https://via.placeholder.com/400x250/3b82f6/ffffff?text=Dashboard) | ![Auth](https://via.placeholder.com/400x250/8b5cf6/ffffff?text=Login) |

| Upcoming Payments | Settings | Mobile View |
|-------------------|----------|--------------|
| ![Payments](https://via.placeholder.com/400x250/10b981/ffffff?text=Payments) | ![Settings](https://via.placeholder.com/400x250/f59e0b/ffffff?text=Settings) | ![Mobile](https://via.placeholder.com/200x400/6366f1/ffffff?text=Mobile) |

---

## 🎨 Design System

**Colors**  
- Blue `#3b82f6` (Primary)  
- Purple `#8b5cf6` (Accent)  
- Green `#10b981` (Success)  
- Orange `#f59e0b` (Warning)  
- Dark `#1e293b`, Light `#64748b` (Text)  

**Typography**  
- Font: *Inter* (Google Fonts)  
- Weights: 300–800  
- Fluid responsive scaling  

**Components**  
- Cards, buttons, forms, modals, navigation  

---

## 🔧 API Endpoints

**Auth**  
```
POST /api/auth/login
POST /api/auth/register
GET  /api/auth/me
POST /api/auth/logout
```

**Subscriptions**  
```
GET    /api/subscriptions
POST   /api/subscriptions
PUT    /api/subscriptions/:id
DELETE /api/subscriptions/:id
```

**Payments**  
```
GET  /api/payments/upcoming
POST /api/payments/:id/mark-paid
GET  /api/payments/export
```

**User Settings**  
```
GET  /api/user/profile
PUT  /api/user/profile
PUT  /api/user/preferences
```

---

## 📊 Database Schema

**Users**
```json
{
  _id: ObjectId,
  name: String,
  email: String,
  password: String (hashed),
  preferences: {
    currency: String,
    notifications: Boolean,
    theme: String
  },
  createdAt: Date,
  updatedAt: Date
}
```

**Subscriptions**
```json
{
  _id: ObjectId,
  userId: ObjectId,
  serviceName: String,
  amount: Number,
  currency: String,
  billingCycle: String,
  nextPaymentDate: Date,
  category: String,
  status: String,
  color: String,
  createdAt: Date,
  updatedAt: Date
}
```

---

## 🔒 Security
- Bcrypt password hashing  
- JWT authentication  
- Input validation (server-side)  
- CORS protection  
- API rate limiting  
- CSP headers for XSS prevention  

---

## 🧪 Testing
- [ ] Register/Login flow  
- [ ] Dashboard data loading  
- [ ] Subscription CRUD  
- [ ] Payment calendar & reminders  
- [ ] Settings & preferences  
- [ ] Responsive layout (mobile/desktop)  
- [ ] Cross-browser compatibility  

**Supported Browsers**: Chrome 90+, Firefox 88+, Safari 14+, Edge 90+, Mobile Safari/Chrome  

---

## 🚀 Deployment

**Static Hosting (Netlify/Vercel)**  
```bash
npm run build
```

**Server Hosting (Heroku/DigitalOcean)**  
```
web: node server.js
MONGODB_URI=your_connection_string
NODE_ENV=production
```

---

## 🤝 Contributing
1. Fork repo  
2. `git checkout -b feature/your-feature`  
3. Commit (`git commit -m "Add feature"`)  
4. Push & open PR  

**Guidelines**:  
- Semantic HTML  
- CSS variables for theming  
- Mobile-first responsive design  
- ARIA for accessibility  
- Clean, documented JS  
- Cross-browser testing  

---

## 📝 License
MIT License - see [LICENSE](LICENSE)  

---

## 📞 Support
Email: **support@subtracker.com**  
or open an issue on GitHub  

---

## 🔄 Version History

### v1.0.0 (Current)  
- ✅ Dashboard, authentication, subscriptions, payments, responsive UI  
- ✅ Settings & preferences, CSV export  

### Planned (v1.1.0)  
- 🔄 Real-time notifications  
- 🔄 Advanced analytics  
- 🔄 Subscription recommendations  
- 🔄 Multi-currency support  
- 🔄 Dark mode  
- 🔄 API integrations  

---

**Built with ❤️ by the SubTracker Team**  
*Last updated: December 2024*
