Demo site - https://lokeshloki3.github.io/discordclone/

STEPS to run on VS Code locally: 

1. Install Node.

	Install Tailwind using PostCSS method

2. Run command:
	npm init -y (For creating package.json Press Enter to all options if asked without -y, with -y not asked)

3. Run commands:
	A. npm install -D tailwindcss postcss autoprefixer vite
	(For creating node_modules)
	B. npx tailwindcss init -p
	(creates tailwind.config.js and -p creates postcss.config.js)
	
4. Install tailwind css intellisense extension. [IGNORE IF ALREADY INSTALLED]

5. Add "*" in content: ["*"] in [ tailwind.config.js ] file.

6. Add scripts in [ package.json ] file:
	"scripts": {
	  "start": "vite"
	},

7. Create main.css and insert: 
	@tailwind base;
	@tailwind components;
	@tailwind utilities;

8. Link main.css to HTML file using <link rel="stylesheet" href="./main.css">.

9. Run command to go live:
	A. npm run start

10. Use the given Local link to go live. (Ctrl+Click)

(All files in same folder and npm run start and not use Go live)


GithubPages(Need production build(main2.css or main3.css - can name anything)) -
	
	Install Tailwind using CLI method for Production
	(Either use Method 1 or Method 2)
	
Method 1 -
 
	1. Run command -
		npx tailwindcss -i ./main.css -o ./main2.css --watch
		(It will create main2.css)
	2. Change main.css to main2.css in HTML file using <link rel="stylesheet" href="./main2.css">

Method 2 - (Steps 3 to 5)

	3. Add in scripts after start in [ package.json ] file:
		"scripts": {
			"dev" : "tailwindcss build main.css -o main3.css",
		},

	4. Run command -
		npm run dev
		(It will create main3.css)
	5. Change main.css to main3.css in HTML file using <link rel="stylesheet" href="./main2.css">

6. Create file .gitignore and write node_modules in it and save

7. Upload project on Github (Public Repo)

8. Go to Settings Pages on Github - Change Branch - None to Main and Save

9. Wait 1 min or Go to Actions section to see progess. Once completed again visit to see site.
