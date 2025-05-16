# Streamlined React Project Setup Guide

## 1. Create a [Vite](https://vitejs.dev/){target="_blank"} React Project
```bash
npm create vite@latest my-react-app -- --template react
```

## 2. Install Packages

### 2.1 Core Packages
- [React-Router](https://reactrouter.com/){target="_blank"}
- [React-Icons](https://react-icons.github.io/react-icons/){target="_blank"}
- [Tailwind CSS](https://tailwindcss.com/){target="_blank"}
- [DaisyUI](https://daisyui.com/){target="_blank"}

```bash
npm i react-router react-icons tailwindcss@latest @tailwindcss/vite@latest daisyui@latest
```

### 2.2 Additional Utilities

#### [Axios](https://axios-http.com/){target="_blank"}
```bash
npm install axios
```

#### [React Helmet Async](https://github.com/staylor/react-helmet-async){target="_blank"}
```bash
npm i react-helmet-async
```

#### [Lucide React](https://lucide.dev/){target="_blank"}
```bash
npm install lucide-react
```

#### [Recharts](https://recharts.org/){target="_blank"}
```bash
npm install recharts
```

#### [Date FNS](https://date-fns.org/){target="_blank"}
```bash
npm install date-fns --save
```

#### [React Fast Marquee](https://www.react-fast-marquee.com/){target="_blank"}
```bash
npm install react-fast-marquee --save
```

#### [React Tabs](https://github.com/reactjs/react-tabs){target="_blank"}
```bash
npm install --save react-tabs
```

## 3. React Router Setup

### 3.1 Create Routes
```jsx
import { createBrowserRouter } from "react-router";

const router = createBrowserRouter([
  {
    path: "/",
    element: <div>Hello World</div>,
    errorElement: <div>404 Not Found</div>,
    children: [
      {
        path: "about",
        element: <div>About Page</div>,
      },
      {
        path: "contact",
        element: <div>Contact Page</div>,
      },
    ],
  },
]);
```

### 3.2 Import Router Provider
```jsx
import { RouterProvider } from "react-router";
```

```jsx
<RouterProvider router={router} />
```

## 4. Development Server (Local)
```bash
npm run dev
```

## 5. Build for Production
```bash
npm run build
```

## 6. Firebase Hosting and Deploy

### 6.1 Install Firebase CLI
```bash
npm install -g firebase-tools
```

### 6.2 Login to Firebase
```bash
firebase login
```

### 6.3 Initialize Firebase Hosting
```bash
firebase init hosting
```

### 6.4 Deploy to Firebase
```bash
firebase deploy
```