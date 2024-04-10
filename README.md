# Tailwind-Project

---
https://tailwindcss.com/
---

# Action Outline:

## Have Intro

* Opening: Show the Tailwind CSS website and their snapshots of popular websites that utilize Tailwind CSS for their design. Use dynamic transitions and make it engaging.

* Introduce Tailwind CSS: Briefly explain what Tailwind CSS is, touching on its utility-first approach to styling. Highlight its rapid adoption in the web development community.

* Pros and Cons: Discuss the advantages of using Tailwind CSS. Despite a steeper learning curve, the framework allows for faster prototyping and a high degree of customization.

## Describe use case

* Target Audience: Explain who typically uses Tailwind CSS.

* Comparison with Traditional CSS.

* Demo Overview: outline what we will be doing in the demo.

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
	
	

Focus on creating the public, src, and within src, the assets, components, styles, and utilities directories.

### Tailwind Integration:
In the `src/styles/tailwind.css` file, demonstrate how to import Tailwind's base, components, and utilities using Tailwind's directives.

Show how to set up the `postcss.config.js` to process the Tailwind file.

### Creating a Simple Page:

Inside the index.html file, use the following emmet abbreviation: `html:5>(header>h1{Welcome to My Page}+nav>ul>li*3>a)+main>section*3>article*2>h2+p+footer>p{Copyright © 2024}`

The input.css file should have these directives at the top of the document:

	@tailwind base;
	@tailwind components;
	@tailwind utilities;
	
Once this is done, run this in the terminal: `npx tailwindcss -i ./src/input.css -o ./src/output.css --watch`

* side note: you can have any output folder, but it is best practice to put the `output.css` in the `public/` folder.

### Running Tailwind:

## Activity 2: Creating a Simple Webpage with Tailwind CSS
### Setup HTML Document: 
Open your index.html file located in the src directory. 
This file will be the canvas for your Tailwind project. Start by adding the basic HTML5 

boilerplate code:
	
	<!DOCTYPE html>
	<html lang="en">
	<head>
	    <meta charset="UTF-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	    <title>My Tailwind Page</title>
	    <link href="./output.css" rel="stylesheet">
	</head>
	<body>
	    <!-- Content goes here -->
	</body>
	</html>
	
Add Tailwind to HTML: Within your HTML file's <body> tag, we'll create a simple structure to demonstrate Tailwind's utility classes. Paste the following code inside the <body> tag:

	<div class="p-10">
	    <h1 class="text-3xl font-bold underline">Hello, world!</h1>
	    <p class="mt-5 text-lg">Welcome to your first Tailwind CSS page!</p>
	    <button class="mt-5 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
	        Click Me
	    </button>
	</div>

This code snippet creates a div with a padding utility class, a heading with Tailwind's typography classes, a paragraph for introductory text, and a button styled with Tailwind's colour, padding, margin, and rounded corner utilities.

Compile Tailwind CSS: Make sure your Tailwind CSS is compiled. If you haven't already, run the following command in your terminal to compile your Tailwind CSS and watch for changes:

`npx tailwindcss -i ./src/input.css -o ./src/output.css --watch`

This command will generate your output.css file, which includes all of Tailwind's utility classes applied to your HTML elements.
	
## Slow Down so People Can Keep up

**Pacing:** Make sure to pace the tutorial so that viewers have enough time to follow along. Avoid rushing through commands and explanations.

**Clarifications:** Periodically pause to explain why certain steps are taken and how Tailwind's utility classes work. This helps in understanding rather than just copying commands.

**Encourage Experimentation:** Towards the end, encourage viewers to experiment with Tailwind's classes in their components, suggesting they try to create a layout or component on their own.             
