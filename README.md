# ✨ React GitHub Dots

Hey! 👋 This is a React component that creates the GitHub's green dots contribution graph. Perfect for spicing up your portfolio or tracking activity in a visually appealing way!

![npm version](https://img.shields.io/npm/v/@raulcanodev/react-github-dots)
![license](https://img.shields.io/npm/l/@raulcanodev/react-github-dots)

[![Compatible with React](https://img.shields.io/badge/React-Compatible-61DAFB?logo=react)](https://reactjs.org/)
[![Compatible with Next.js](https://img.shields.io/badge/Next.js-Compatible-000000?logo=next.js)](https://nextjs.org/)

![SCR-20250105-oixx](https://github.com/user-attachments/assets/e0ce5e34-a9a3-4029-95d4-415e16ac7443)

## ✨ About this package

- 📊 Beautiful GitHub-style contribution visualization
- 🌓 Seamless light and dark mode support
- 🎨 Make it yours with custom color schemes
- 🔄 Real-time GitHub data at your fingertips
- 📱 Looks great on any screen size
- ⚡️ Smart caching for optimal performance

## 🚀 Getting Started

1. Pop this into your terminal:

```bash
npm install @raulcanodev/react-github-dots
```

2. Within your React app:
```jsx
import ContributionGraph from '@raulcanodev/react-github-dots';

function App() {
  return (
    <ContributionGraph 
      username="your-github-username"
      token="your-github-token"
      theme="dark" // or "light"
      cacheTime="8h" // Cache data for 8 hours
    />
  );
}
```

For Next.js 13+ (App Router), add the client directive:
```jsx
'use client';
import ContributionGraph from '@raulcanodev/react-github-dots';

export default function Page() {
  return (
    <ContributionGraph 
      username="your-github-username"
      token="your-github-token"
      theme="dark"
      cacheTime="1d"
    />
  );
}
```

## 🎛 Configuration Options

Here's what you can tweak:

| Prop | Type | Default | What it does |
|------|------|---------|-------------|
| `username` | string | required | Your GitHub username |
| `token` | string | required | Your GitHub access token |
| `theme` | 'light' \| 'dark' | 'dark' | Pick your style |
| `customColorScheme` | object | null | Custom colors |
| `loadingComponent` | ReactNode | null | Custom loading state |
| `cacheTime` | false \| '2h' \| '8h' \| '1d' | '1d' | Control data caching duration |

### 🎨 Customize The Dot Colors

Want your own color scheme? Here's how:

```jsx
<ContributionGraph 
  username="your-github-username"
  token="your-github-token"
  customColorScheme={{
    0: '#ebedf0', // No contributions
    1: '#ff9b9b', // 1-3 contributions
    2: '#ff4040', // 4-6 contributions
    3: '#ff0000', // 7-9 contributions
    4: '#990000'  // 10+ contributions
  }}
/>
```

### ⚡️ Cache Control

Optimize performance with smart caching:

```jsx
// Disable caching - always fetch fresh data
<ContributionGraph 
  username="your-github-username"
  token="your-github-token"
  cacheTime={false}
/>

// Cache for 2 hours
<ContributionGraph 
  username="your-github-username"
  token="your-github-token"
  cacheTime="2h"
/>

// Cache for 8 hours
<ContributionGraph 
  username="your-github-username"
  token="your-github-token"
  cacheTime="8h"
/>

// Cache for 1 day (default)
<ContributionGraph 
  username="your-github-username"
  token="your-github-token"
  cacheTime="1d"
/>
```

## 🛠 Development & Contributions

### Getting Set Up

1. Grab the code:

```bash
git clone https://github.com/raulcanodev/react-github-dots.git
cd react-github-dots
```

2. Install what you need:

```bash
npm install
```

3. Build it:

```bash
npm run watch
```

### 🧪 Testing Locally

1. Link your package locally, which allows you to test it in other projects:

```bash
npm link
```

2. Create a new React app and link the component:

```bash
npx create-react-app test-github-dots
cd test-github-dots
npm install react react-dom
npm link @raulcanodev/react-github-dots
```

3. In your App.jsx, import and use:

```jsx
import ContributionGraph from '@raulcanodev/react-github-dots';
```

### 🔄 Development Flow

Want to see changes in real-time? Here's how:

1. In your package directory:

```bash
npm run watch
```

2. In your test app:

```bash
npm run dev
```

Need to refresh the link for any bug? Try:

```bash
npm unlink @raulcanodev/react-github-dots
npm link @raulcanodev/react-github-dots
```

## 🔑 Getting Your GitHub Token

You'll need a GitHub Personal Access Token with `read:user` scope. Get one here: https://github.com/settings/tokens?type=beta

## 📝 License

MIT © Raul Cano

---

Made with ❤️ by Raul Cano. Questions? Issues? Feel free to reach out!

Want to contribute? PRs are always welcome! 🙌