# SkillCertify - The Internship Platform

A modern learning platform that offers comprehensive courses and internship opportunities with integrated payment processing.

## 🚀 Features

- **Course Catalog**: Browse through various courses in different categories
- **Payment Integration**: Secure payment processing with Razorpay
- **Responsive Design**: Modern UI that works on all devices
- **Course Details**: Detailed course information with enrollment
- **Contact Forms**: Email integration for inquiries
- **Smooth Navigation**: Optimized routing and scroll behavior

## 🛠️ Tech Stack

### Frontend
- **React 18** - Modern React with hooks
- **Vite** - Fast build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework
- **Framer Motion** - Smooth animations
- **React Router** - Client-side routing
- **Radix UI** - Accessible UI components

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **Razorpay** - Payment gateway integration
- **CORS** - Cross-origin resource sharing

### External Services
- **Razorpay** - Payment processing
- **EmailJS** - Email functionality for contact forms

## 📦 Installation

### 1. Clone the repository
```bash
git clone <https://github.com/yashumak/SkillCertify--The-Internship-platform>
cd SkillCertify
```

### 2. Install Frontend Dependencies
```bash
npm install
```

### 3. Install Backend Dependencies
```bash
cd server
npm install
cd ..
```

### 4. Set up Environment Variables

Create a `.env` file in the root directory:
```env
# Razorpay Configuration
RAZORPAY_KEY_ID=your_razorpay_key_id_here
RAZORPAY_KEY_SECRET=your_razorpay_key_secret_here

# Frontend Environment Variables
VITE_RAZORPAY_KEY_ID=your_razorpay_key_id_here

# Server Configuration
PORT=5000

# Email Configuration (if using EmailJS)
VITE_EMAILJS_SERVICE_ID=your_emailjs_service_id
VITE_EMAILJS_TEMPLATE_ID=your_emailjs_template_id
VITE_EMAILJS_USER_ID=your_emailjs_user_id
```

Create a `.env` file in the server directory:
```env
RAZORPAY_KEY_ID=your_razorpay_key_id_here
RAZORPAY_KEY_SECRET=your_razorpay_key_secret_here
PORT=5000
```

### 5. Set up Razorpay

1. **Create a Razorpay Account**:
   - Go to [Razorpay Dashboard](https://dashboard.razorpay.com/)
   - Sign up for a new account
   - Complete KYC verification

2. **Get API Keys**:
   - Go to Settings → API Keys
   - Generate a new key pair
   - Copy the Key ID and Key Secret

3. **Update Environment Variables**:
   - Replace `your_razorpay_key_id_here` with your actual Key ID
   - Replace `your_razorpay_key_secret_here` with your actual Key Secret

### 6. Start Development Servers

**Start Backend Server**:
```bash
cd server
npm run dev
```

**Start Frontend Server** (in a new terminal):
```bash
npm run dev
```

### 7. Open your browser
Navigate to `http://localhost:5173`

## 🚀 Available Scripts

### Frontend
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

### Backend
- `npm run dev` - Start development server with nodemon
- `npm start` - Start production server

## 💳 Payment Integration

The application includes a complete Razorpay payment integration:

### Features:
- **Secure Payment Processing**: All payments are processed through Razorpay
- **Payment Verification**: Server-side signature verification
- **Order Management**: Automatic order creation and tracking
- **Customer Data**: Collects customer information during payment
- **Success Handling**: Proper success and error handling

### Payment Flow:
1. User clicks "Enroll Now" on a course
2. Payment modal opens with course details
3. User fills in personal information
4. Razorpay payment gateway opens
5. User completes payment
6. Payment is verified on the server
7. Success confirmation is shown

### API Endpoints:
- `POST /api/create-order` - Create a new payment order
- `POST /api/verify-payment` - Verify payment signature
- `GET /api/payment-status/:paymentId` - Get payment status
- `GET /api/health` - Health check endpoint

## 📁 Project Structure

```
SkillCertify/
├── public/                 # Static assets
├── server/                 # Backend server
│   ├── index.js           # Express server with Razorpay integration
│   └── package.json       # Server dependencies
├── src/
│   ├── components/         # Reusable UI components
│   │   ├── ui/            # Base UI components
│   │   ├── Navbar.jsx     # Navigation component
│   │   ├── Footer.jsx     # Footer component
│   │   ├── CourseCard.jsx # Course display component
│   │   ├── FeaturedCourses.jsx
│   │   └── PaymentModal.jsx # Payment integration component
│   ├── pages/             # Page components
│   │   ├── Home.jsx       # Landing page
│   │   ├── Courses.jsx    # Course catalog
│   │   ├── About.jsx      # About page
│   │   ├── Contact.jsx    # Contact page
│   │   ├── courses/       # Course-related pages
│   │   └── legal/         # Legal pages
│   ├── App.jsx            # Main application component
│   ├── main.jsx           # Application entry point
│   └── index.css          # Global styles
├── package.json           # Frontend dependencies and scripts
├── vite.config.js         # Vite configuration
├── tailwind.config.js     # Tailwind CSS configuration
├── env.example            # Environment variables template
└── README.md              # Project documentation
```

## 🔧 Configuration

### Razorpay Configuration
- **Test Mode**: Use test keys for development
- **Live Mode**: Use live keys for production
- **Webhook Setup**: Configure webhooks for payment notifications

### Environment Variables
- `RAZORPAY_KEY_ID`: Your Razorpay Key ID
- `RAZORPAY_KEY_SECRET`: Your Razorpay Key Secret
- `VITE_RAZORPAY_KEY_ID`: Frontend Key ID (same as above)
- `PORT`: Server port (default: 5000)

## 🚀 Deployment

### Frontend Deployment
1. Build the project: `npm run build`
2. Deploy the `dist` folder to your hosting service
3. Set environment variables in your hosting platform

### Backend Deployment
1. Deploy the `server` folder to your server
2. Install dependencies: `npm install`
3. Set environment variables
4. Start the server: `npm start`

## 🔒 Security

- **Payment Verification**: All payments are verified server-side
- **Environment Variables**: Sensitive data is stored in environment variables
- **CORS**: Proper CORS configuration for API security
- **Input Validation**: Form validation on both frontend and backend

## 📞 Support

For support and questions:
- Create an issue on GitHub
- Contact through the contact form on the website

## 📄 License

This project is licensed under the MIT License.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

---

**Note**: Make sure to replace all placeholder values in environment variables with your actual Razorpay credentials before running the application.

------------------------------------------------------------