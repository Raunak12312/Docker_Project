# 🌍 International Greetings App - React + i18next

**Author:** Raunak

## 📝 Project Overview

This is a complete i18n (internationalization) tutorial project built with **React** and **i18next**. It demonstrates how to implement multi-language support in a React application with support for English, Hindi, French, and Arabic.


## 🚀 Getting Started

### Prerequisites
- Node.js 20+
- Docker (optional, for containerized setup)

### Installation

#### Option 1: Local Setup
```bash
npm install --legacy-peer-deps
npm run dev
```

#### Option 2: Docker Setup
```bash
docker build -t react-app:dev .
docker run -p 5173:5173 react-app:dev
```

The app will be available at `http://localhost:5173`

## 📂 Project Structure

```
src/
├── components/
│   └── language-selector.jsx    # Language switching component
├── i18n/
│   └── i18n.js                  # i18next configuration
├── App.jsx                       # Main application component
├── main.jsx                      # React entry point
└── index.css                     # Global styles

public/locales/                   # Translation files
├── en/translation.json
├── hi/translation.json
├── fr/translation.json
└── ar/translation.json
```

## 🌐 Supported Languages

- 🇬🇧 English (en)
- 🇮🇳 Hindi (hi)
- 🇫🇷 French (fr)
- 🇸🇦 Arabic (ar)

## 📦 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## 🔧 Technologies Used

- **React** 18.2.0
- **Vite** 8.0.8
- **i18next** 23.7.11
- **i18next HTTP Backend** 2.4.2
- **i18next Browser Language Detector** 7.2.0
- **react-i18next** 13.5.0

## 📚 How to Add New Translations

1. Add translation keys to JSON files in `public/locales/{language}/translation.json`
2. Use the `useTranslation()` hook in your components:

```jsx
import { useTranslation } from 'react-i18next';

function MyComponent() {
  const { t } = useTranslation();
  return <h1>{t('greeting')}</h1>;
}
```

## 🐳 Docker Notes

The Dockerfile uses:
- `node:20-alpine` base image (lightweight)
- `npm install --legacy-peer-deps` to resolve peer dependency conflicts
- Vite's host binding for container access

## 💡 Tips for Users

- Language preference is stored in browser local storage
- The app auto-detects user browser language on first visit
- Translations are loaded from static JSON files for better performance

## 📝 License

This project is based on the i18next tutorial series.

---

For issues or questions, please refer to the [i18next documentation](https://www.i18next.com/)
