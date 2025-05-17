# Streamlined React Project Setup

## 1. Create a [Vite](https://vitejs.dev/ "target='_blank'") React Project

```bash
npm create vite@latest my-react-app -- --template react
```

## 2. Install Core Packages
- [React-Router](https://reactrouter.com/ "target='_blank'")
- [React-Icons](https://react-icons.github.io/react-icons/ "target='_blank'")
- [Tailwind CSS](https://tailwindcss.com/ "target='_blank'")
- [DaisyUI](https://daisyui.com/ "target='_blank'")

```bash
npm i react-router react-icons tailwindcss@latest @tailwindcss/vite@latest daisyui@latest
```

#### vite.config.js

```bash
import tailwindcss from '@tailwindcss/vite';
```

```bash
tailwindcss(),
```

#### index.css

```bash
@import "tailwindcss";
@plugin "daisyui";
```

## 3. React Router Setup

### Create Routes

```jsx
import { createBrowserRouter } from "react-router";

const router = createBrowserRouter([
  {
    path: "/",
    element: <div>Hello World</div>,
    errorElement: <div>404 Not Found</div>,
    children: [
      {
        index: true,
        path: "/",
        element: <div>About Page</div>,
      },
      {
        path: "about",
        element: <div>About Page</div>,
      },
    ],
  },
]);

export default router;
```

### Import Router Provider

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

### 5. Additional Utilities

#### [Axios](https://axios-http.com/ "target='_blank'")

```bash
npm install axios
```

#### [React Helmet Async](https://github.com/staylor/react-helmet-async "target='_blank'")

```bash
npm i react-helmet-async
```

#### [Lucide React](https://lucide.dev/ "target='_blank'")

```bash
npm install lucide-react
```

#### [Recharts](https://recharts.org/ "target='_blank'")

```bash
npm install recharts
```

#### [Date FNS](https://date-fns.org/ "target='_blank'")

```bash
npm install date-fns --save
```

#### [React Fast Marquee](https://www.react-fast-marquee.com/ "target='_blank'")

```bash
npm install react-fast-marquee --save
```

#### [React Tabs](https://github.com/reactjs/react-tabs "target='_blank'")

```bash
npm install --save react-tabs
```

## 6. Build for Production

```bash
npm run build
```

## 7. Firebase Hosting and Deploy

### Install Firebase CLI

```bash
npm install -g firebase-tools
```

### Login to Firebase

```bash
firebase login
```

### Initialize Firebase Hosting

```bash
firebase init hosting
```

### Deploy to Firebase

```bash
firebase deploy
```
