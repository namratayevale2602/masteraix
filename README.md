## Setting the React Vite Frontend :

> React Vite setup Documentation : https://vite.dev/guide/

        bash

        npm create vite@latest

- select folder
- select react

        bash

        npm install

  - this install necessary node_modules to run the react frontend file.

- now to run the project of react frontend

         bash

         npm run dev

- now we can run the project on browser on default port

        http://localhost:5173/

- if we want to test on mobile as well and its on same network as pc wifi

- go to package.json

        "scripts": {
        "dev": "vite --host",
        "build": "vite build",
        "lint": "eslint .",
        "preview": "vite preview"
        },

- Now delete all content inside App.jsx and App.css and index.css

  - App.jsx
  - App.css
  - index.css

- Now recreate App.jsx

        import React from "react";

        function App() {
        return <div>App</div>;
        }

        export default App;

> Tailwind CSS with Vite setup Documentation :

        https://tailwindcss.com/docs/installation/using-vite

- 01 Install Tailwind CSS

        Install tailwindcss and @tailwindcss/vite via npm.

        Terminal

                  npm install tailwindcss @tailwindcss/vite

- 2 Configure the Vite plugin

  Add the @tailwindcss/vite plugin to your Vite configuration.

        vite.config.ts

                import { defineConfig } from "vite";
                import react from "@vitejs/plugin-react";
                import tailwindcss from "@tailwindcss/vite";

                // https://vite.dev/config/
                export default defineConfig({
                plugins: [react(), tailwindcss()],
                });

- 3 Import Tailwind CSS

  Add an @import to your CSS file that imports Tailwind CSS.

  inside index.css in our case

          @import "tailwindcss";

- 4 Start your build process

  Run your build process with npm run dev or whatever command is configured in your package.json file.

  Terminal

        npm run dev

## React Router Setup :

    bash

        npm i react-router-dom

> App.jsx

        import React from "react";
        import {
        createBrowserRouter,
        createRoutesFromElements,
        Route,
        RouterProvider,
        } from "react-router-dom";

        import Layout from "./Layout/Layout";
        import Home from "./pages/Home/Home";
        import About from "./pages/About/About";
        import Contact from "./pages/Contact/Contact";

        function App() {
        // http://localhost:5173
        // http://localhost:5173/ - index
        // http://localhost:5173/about  - path about
        // http://localhost:5173/contact  - path contact
        const router = createBrowserRouter(
            createRoutesFromElements(
            <>
                <Route path="/" element={<Layout />}>
                <Route index element={<Home />} />
                <Route path="about" element={<About />} />
                <Route path="contact" element={<Contact />} />
                </Route>
            </>
            )
        );

        return <RouterProvider router={router} />;
        }

        export default App;

> Layout.jsx

                import React from "react";
                import { Outlet } from "react-router-dom";
                import Navbar from "../components/Navbar/Navbar";
                import Footer from "../components/Footer/Footer";
                function Layout() {
                return (
                    <>
                    <Navbar />
                    <Outlet />
                    <Footer />
                    </>
                );
                }

                export default Layout;

## Navbar

Take referance from : https://www.material-tailwind.com/docs/react/navbar

Install

        npm i framer-motion lucide-react

install framer-motion & lucide-react library
#   m a s t e r a i x  
 #   m a s t e r a i x  
 #   m a s t e r a i x  
 