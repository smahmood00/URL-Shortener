# URL Shortener

A modern URL shortening service built with React, Vite, and Supabase. Create shortened URLs, track click analytics, and generate QR codes for your links.

## Features

- 🔗 URL Shortening with custom alias support
- 📊 Analytics Dashboard
  - Click tracking
  - Device statistics
  - Geographic location data
- 🔐 User Authentication
- 📱 Responsive Design
- 📈 Real-time Statistics
- 🎨 Modern UI with Tailwind CSS
- 🔄 QR Code Generation

## Tech Stack

- Frontend:
  - React 18
  - Vite
  - Tailwind CSS
  - Radix UI Components
  - React Router DOM
  - Recharts for analytics visualization
  - UA Parser JS for device detection

- Backend:
  - Supabase (Database & Authentication)
  - Supabase Storage (QR Code storage)

## Prerequisites

- Node.js (LTS version recommended)
- npm or yarn
- Supabase account

## Environment Setup

1. Create a `.env` file in the project root:
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_KEY=your_supabase_anon_key
```

## Database Schema

### URLs Table
- `id` (primary key)
- `user_id` (references auth.users)
- `title` (text)
- `original_url` (text)
- `short_url` (text)
- `custom_url` (text, nullable)
- `qr` (text)
- Created at timestamp

### Clicks Table
- `id` (primary key)
- `url_id` (references urls.id)
- `city` (text)
- `country` (text)
- `device` (text)
- Created at timestamp

## Installation

1. Clone the repository
```bash
git clone <repository-url>
cd url-shortener
```

2. Install dependencies
```bash
npm install
# or
yarn install
```

3. Start the development server
```bash
npm run dev
# or
yarn dev
```

4. Build for production
```bash
npm run build
# or
yarn build
```

## Project Structure

```
url-shortener/
├── src/
│   ├── components/     # React components
│   ├── db/            # Database API functions
│   ├── hooks/         # Custom React hooks
│   ├── layouts/       # Layout components
│   ├── lib/           # Utility functions
│   └── pages/         # Page components
├── public/            # Static assets
└── ...configuration files
```

## Features in Detail

### URL Shortening
- Generate short URLs automatically
- Support for custom aliases
- QR code generation for each shortened URL

### Analytics
- Track clicks on shortened URLs
- Monitor device types (desktop, mobile, tablet)
- Geographic location tracking
- Visual data representation with charts

### Authentication
- User registration and login
- Protected routes for authenticated users
- Personal dashboard for URL management


