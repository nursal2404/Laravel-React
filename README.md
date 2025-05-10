# Laravel + React Fullstack App

This project uses Laravel Breeze (API stack) for the backend and React (with Vite and Tailwind CSS) for the frontend. Below is a step-by-step setup guide.

---

## 📁 Project Structure

```
/laravel-react-api      ← Laravel API backend
/react-breeze-api       ← React frontend (Vite)
```

---

## 🧩 Backend Setup (Laravel Breeze API)

1. **Create Laravel Project**

```bash
laravel new laravel-react-api
cd laravel-react-api
```

2. **Install Laravel Breeze (API version)**

```bash
composer require laravel/breeze --dev
php artisan breeze:install api
```

3. **Run Migrations (if needed)**

```bash
php artisan migrate
```

4. **Serve the Laravel API**

```bash
php artisan serve
```

> The Laravel API will be available at:  
> `http://127.0.0.1:8000` or based on your `php artisan serve` output.

---

## 💻 Frontend Setup (React + Vite + Tailwind)

1. **Create React Project with Vite**

```bash
npm create vite@latest react-breeze-api -- --template react
cd react-breeze-api
```

2. **Install Dependencies**

```bash
npm install
npm run dev     # Run the app for the first time
```

> To stop: Press `Ctrl + C`

3. **Install Routing and HTTP Client**

```bash
npm install react-router-dom
npm install axios
```

4. **Install Tailwind CSS**

```bash
npm install -D tailwindcss@3.3.3 postcss autoprefixer
npx tailwindcss init -p
```

5. **Configure Tailwind (in `tailwind.config.js`)**

Make sure your config looks like this:

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

6. **Add Tailwind to `src/index.css`**

Replace content of `src/index.css` with:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

7. **Run the Frontend App**

```bash
npm run dev
```

> Your frontend will run at:  
> `http://localhost:5173` by default

---

