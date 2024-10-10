Get started with Tailwind CSS
Tailwind CSS works by scanning all of your HTML files, JavaScript components, and any other templates for class names, generating the corresponding styles and then writing them to a static CSS file.

It's fast, flexible, and reliable — with zero-runtime.

(1)Installation
Tailwind CLI
Installing Tailwind CLI
The simplest and fastest way to get up and running with Tailwind CSS from scratch is with the Tailwind CLI tool. The CLI is also available as a standalone executable if you want to use it without installing Node.js.
https://tailwindcss.com/docs/installation
Install Tailwind CSS
Install tailwindcss via npm, and create your tailwind.config.js file.

Terminal

npm install -D tailwindcss
npx tailwindcss init
Configure your template paths
Add the paths to all of your template files in your tailwind.config.js file.

tailwind.config.js

/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
Add the Tailwind directives to your CSS
Add the @tailwind directives for each of Tailwind’s layers to your main CSS file.

src/input.css

@tailwind base;
@tailwind components;
@tailwind utilities;
Start the Tailwind CLI build process
Run the CLI tool to scan your template files for classes and build your CSS.

Terminal

npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
Start using Tailwind in your HTML
Add your compiled CSS file to the <head> and start using Tailwind’s utility classes to style your content.

src/index.html

<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="./output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
(2)Using PostCSS
https://tailwindcss.com/docs/installation/using-postcss
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init
npm run dev
(3) play-cdn
https://tailwindcss.com/docs/installation/play-cdn
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
