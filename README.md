# Tailwind-Project

---
https://tailwindcss.com/
---

### Preparation:

Open Visual Studio Code or your preferred code editor.

Show the installation process, including Node.js; Tailwind requires Node.js to compile its CSS.

## Activity 1: Project Setup

Begin by creating a new project directory and navigate into it.

Initialize a new npm project with `npm init -y`

Install Tailwind CSS via npm: `npm install -D tailwindcss postcss autoprefixer`

Create your `tailwind.config.js` and `postcss.config.js` files by running `npx tailwindcss init -p`

Inside the `tailwind.config.js` add paths to all of your template files `["./src/**/*.{html,js}"]`

**The file should look like this:**

	/** @type {import('tailwindcss').Config} */
	module.exports = {
	  content: ["./src/**/*.{html,js}"],
	  theme: {
    extend: {},
	  },
	  plugins: [],
	}

### Folder Structure:

You should then create the `src` file at the root of your project. 

Within `src` create the `index.html` and `input.css` files.

### At this point, your file structure should be:

	TailwindCss/
	|
	├── node_modules/ 
	├── src/
	│   ├── index.html
	│   ├── input.css 
	│   └── output.css 
	├── package-lock.json 
	├── package.json 
	├── postcss.config.js
	└── tailwind.config.js

### Creating a Simple Page:

Inside the index.html file, use the following emmet abbreviation: `html:5>(div>h1{My Tailwind Page}+p+button)footer>p{Tailwind© 2024}`

The `input.css` file should have these directives at the top of the document:

	@tailwind base;
	@tailwind components;
	@tailwind utilities;
	
Once this is done, run this in the terminal: `npx tailwindcss -i ./src/input.css -o ./src/output.css --watch`

* side note: you can have any output folder, but putting the `output.css` in the `public/` folder is best practice.

### Running Tailwind:

## Activity 2: Creating a Simple Webpage with Tailwind CSS
### Setup HTML Document:

Open your `index.html` file located in the src directory. 
This file will be the canvas for your Tailwind project. Start by adding the basic HTML5 

	
	<!DOCTYPE html>
	<html lang="en">
	<head>
	    <meta charset="UTF-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	    <title>Document</title>
	</head>
	<body>
	    <div>
	        <h1>My Tailwind Page</h1>
	        <p></p>
	        <button></button>
	    </div>
	    <footer>
	        <p>Tailwind© 2024</p>
	    </footer>
	</body>
	</html>
		
Add Tailwind to HTML: Within your HTML file's <body> tag, we'll create a simple structure to demonstrate Tailwind's utility classes. Paste the following code inside the <body> tag:

`<body class="bg-gray-50 flex items-center justify-center min-h-screen">`
	
`<div class="w-full max-w-md mx-auto bg-white rounded-lg shadow-md p-8">`
	    
`<h1 class="text-center text-4xl font-bold text-gray-800">Hello, world!</h1>`
	
`<p class="mt-5 text-lg text-gray-700 w-full p-4 bg-gray-100 border border-gray-200 rounded">Welcome to your first Tailwind CSS page!</p>`
	
`<button class="mt-5 w-full bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded transition ease-in-out duration-150">Click Me</button>`
	        
This code snippet creates a div with a padding utility class, a heading with Tailwind's typography classes, a paragraph for introductory text, and a button styled with Tailwind's colour, padding, margin, and rounded corner utilities.

Compile Tailwind CSS: Make sure your Tailwind CSS is compiled. If you haven't already, run the following command in your terminal to compile your Tailwind CSS and watch for changes:

`npx tailwindcss -i ./src/input.css -o ./src/output.css --watch`

This command will generate your output.css file, which includes all of Tailwind's utility classes applied to your HTML elements.

# DOC

	<!doctype html>
	<html lang="en">
	<head>
	    <meta charset="UTF-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	    <title>My Tailwind Page</title>
	    <link href="output.css" rel="stylesheet">
	</head>
	<body class="bg-gray-50 flex items-center justify-center min-h-screen">
	    <div class="w-full max-w-md mx-auto bg-white rounded-lg shadow-md p-8">
	        <h1 class="text-center text-4xl font-bold text-gray-800">Hello, world!</h1>
	        <p class="mt-5 text-lg text-gray-700 w-full p-4 bg-gray-100 border border-gray-200 rounded">
	            Welcome to your first Tailwind CSS page!
	        </p>
	        <button class="mt-5 w-full bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded transition ease-in-out duration-150">
	            Click Me
	        </button>
	    </div>
	</body>
	</html>




