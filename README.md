# Developer Portfolio 🚀

A modern, responsive web portfolio built with **Next.js**, designed to showcase projects,
skills, experience, and education for a full-stack developer.

## ✨ Features

- **Multi-language**: Full support for Spanish, English, and Portuguese using `next-intl`
- **Dark/Light Theme**: Theme toggle with persistent state
- **Contact Form**: Integrated with Telegram, Gmail, and email
- **reCAPTCHA Verification**: Anti-spam protection for forms
- **Animations**: Smooth animations powered by Lottie React
- **Blog**: Integrated blog section
- **Responsive**: Mobile-first design adaptable to all devices
- **SEO Optimized**: Metadata and structure optimized for search engines
- **Docker**: Containers configured for development and production

## 🛠️ Tech Stack

### Frontend

- **Next.js** 16.0.10 - Modern React Framework
- **React** 19.2.3 - UI Library
- **Tailwind CSS** 4.1.16 - Styling Framework
- **SASS** 1.69.5 - CSS Preprocessor
- **Lottie React** 2.4.1 - JSON Animations
- **React Icons** 4.11.0 - Vector Icons
- **React Toastify** 10.0.4 - Notifications

### Backend & API

- **Nodemailer** 6.9.15 - Email sending
- **Axios** 1.6.8 - HTTP Client
- **React Google reCAPTCHA** 3.1.0 - Anti-spam verification

### Internationalization

- **next-intl** 4.7.0 - Language management

## 📦 Main Dependencies

```json
{
  "dependencies": {
    "next": "16.0.10",
    "react": "19.2.3",
    "tailwindcss": "latest",
    "next-intl": "4.7.0",
    "nodemailer": "6.9.15",
    "lottie-react": "2.4.1"
  }
}
```

## 🚀 Quick Start

### Prerequisites

- Node.js >= 18.x
- pnpm (recommended) o npm

### Installation

1. **Clone the repository**

```bash
git clone <repository-url>
cd developer-portfolio
```

2. **Install dependencies**

```bash
pnpm install
# or
npm install
```

3. **Configure environment variables**

Create a `.env` file in the root directory:

```env
# Email Configuration
EMAIL_ADDRESS=your_email@gmail.com
GMAIL_PASSKEY=your_gmail_app_password

# Telegram Configuration
TELEGRAM_BOT_TOKEN=your_bot_token
TELEGRAM_CHAT_ID=your_chat_id

# Google reCAPTCHA
NEXT_PUBLIC_RECAPTCHA_SITE_KEY=your_site_key
RECAPTCHA_SECRET_KEY=your_secret_key
```

### Development

```bash
pnpm dev
# or
npm run dev
```

The application will be available at `http://localhost:3000`

### Production Build

```bash
pnpm build
pnpm start
# or
npm run build
npm run start
```

## 🐳 Docker

### Development

```bash
docker-compose up
```

The development container uses `Dockerfile.dev` with hot reload enabled.

### Production

```bash
docker build -f Dockerfile.prod -t developer-portfolio:latest .
docker run -p 3000:3000 developer-portfolio:latest
```

## 📁 Project Structure

```
├── app/
│   ├── api/                   # API routes
│   │   ├── contact/           # Contact API (POST)
│   │   ├── data/              # Data API
│   │   └── google/            # Google integrations
│   ├── assets/                # Lottie animations and SVGs
│   ├── blog/                  # Blog page
│   ├── components/            # Reusable components
│   │   ├── homepage/          # Main page components
│   │   │   ├── about/
│   │   │   ├── blog/
│   │   │   ├── contact/
│   │   │   ├── education/
│   │   │   ├── experience/
│   │   │   ├── hero-section/
│   │   │   ├── projects/
│   │   │   └── skills/
│   │   └── helper/            # Helper components
│   ├── css/                   # Global styles
│   └── [locale]/              # Internationalized routes
├── public/                    # Static assets
├── i18n/                      # Language configuration
├── messages/                  # Translations (EN, ES, PT)
├── utils/                     # Utility functions
│   ├── data/                  # Portfolio data
│   │   ├── personal-data.js
│   │   ├── skills.js
│   │   ├── experience.js
│   │   ├── educations.js
│   │   └── projects-data.js
│   └── content/               # Content JSON files
├── middleware.js              # Next.js Middleware
├── next.config.js             # Next.js configuration
├── tailwind.config.js         # Tailwind CSS configuration
└── package.json               # Project dependencies
```

## 🔧 Configuration

### Supported Languages

Languages are configured in `i18n/routing.js`. Translation files are located in `messages/`:

- `en.json` - English
- `es.json` - Spanish
- `pt.json` - Portuguese

### Portfolio Data

Edit the files located in `utils/data/`:

- `personal-data.js` - Personal information
- `skills.js` - Technical skills
- `experience.js` - Work experience
- `educations.js` - Education and certifications
- `projects-data.js` - Featured projects

### Lottie Animations

JSON animation files are stored in `app/assets/lottie/`

## 📧 Contact Form

The contact form is integrated with:

- **Gmail**: Sends an email to your configured address
- **Telegram**: Sends a message to your Telegram bot
- **Validations**: Email and reCAPTCHA

**Configuring Gmail:**

1. Enable 2-Factor Authentication (2FA)
2. Generate an App Password
3. Use it in GMAIL_PASSKEY

**Configuring Telegram:**

1. Create a bot via @BotFather
2. Obtain the bot token
3. Get your account's chat ID

## 🎨 Themes and Styling

- Tailwind CSS for utility classes
- SASS for custom styles in `app/css/`
- Dark/Light mode support
- Reusable components located in `components/helper/`

## 📊 Available Scripts

```bash
pnpm dev      # Start development server
pnpm build    # Build for production
pnpm start    # Start production server
pnpm lint     # Run linter
```

## 🔗 Contact Links

- **Email**: borisleonel12@gmail.com
- **GitHub**: https://github.com/boris-mita/
- **LinkedIn**: https://www.linkedin.com/in/boris-leonel-8a3296175/

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (git checkout -b feature/AmazingFeature)
3. Commit your changes (git commit -m 'Add AmazingFeature')
4. Push to the branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

## 📧 Support

To report bugs or request new features, please open an issue in the repository.

---

**Developed by** [Boris Leonel](https://github.com/boris-mita)  
**Stack**: Next.js • React • Tailwind CSS • Node.js
