# Go to your project folder (make sure the path is correct, quotes handle spaces)
cd "~/Desktop/Hostel_craves_final/swiggyclone copy"

# Remove node_modules and cache from Git tracking
git rm -r --cached node_modules
git rm -r --cached .cache

# Create/overwrite README.md with the cleaned project-specific content
echo "# Hostel Craves 🍔

A food delivery web app built with **React.js** for Manipal University Jaipur students to order food easily from local vendors.

## Features

- Browse restaurants and their menus
- Add items to cart and place orders
- Payment options (mock integration)
- Order tracking and confirmation
- User authentication (Login/Register)
- State management using React Context API

## Tech Stack

- **Frontend:** React.js, HTML5, CSS3, JavaScript (ES6+)
- **Backend:** Node.js, Express.js (if backend included)
- **Database:** MongoDB / MongoDB Atlas
- **APIs:** Custom REST APIs
- **State Management:** React Context API

## Getting Started

1. Clone the repo:  
\`\`\`bash
git clone https://github.com/kanishkakasana26/Hostel-Craves.git
cd Hostel-Craves
\`\`\`

2. Install dependencies:  
\`\`\`bash
npm install
\`\`\`

3. Run the app:  
\`\`\`bash
npm start
\`\`\`

Open [http://localhost:3000](http://localhost:3000) in your browser to view the app.

---

## Build for Production

\`\`\`bash
npm run build
\`\`\`

The app will be optimized for production in the \`build\` folder.

---

## Contributing

Feel free to fork the repository and submit pull requests.

---

## License

MIT License
" > README.md

# Stage all files
git add .

# Commit changes
git commit -m "Clean repo, remove node_modules/cache, update README"

# Set correct remote (replace if already exists)
git remote remove origin
git remote add origin https://github.com/kanishkakasana26/Hostel-Craves.git

# Push to GitHub (force in case of conflicts)
git branch -M main
git push -u origin main --force
