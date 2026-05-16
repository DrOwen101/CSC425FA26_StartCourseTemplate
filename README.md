# Welcome to CSC425FA26 with Dr. Jason T Owen.
Your class will meet from 11am - 12:15pm every Tuesday & Thursday
# Dr. Owen is available for office hours in BB652H:
Monday: 5pm - 6pm
Tuesday: 9:30am - 12:30pm
Wednesday: 9:30am - 12:30pm
Thursday: 9:30am - 12:30pm
Fri: By appointment only

# Prerequisites before starting the course
Create a free GitHub account
--- Tip: Use a personal email and not a school one if you want to begin creating a professional coding portfolio of work.

# This is your personal repository. Complete these steps to set up your development environment for the course.

### Step 1: Install Visual Studio Code (VSCode)
1. Download VSCode from [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Install the application for your operating system
3. Open VSCode and familiarize yourself with the interface
4. **Recommended Extensions** (Install from VSCode Extensions marketplace):
   - ESLint
   - Prettier - Code formatter
   - ES7+ React/Redux/React-Native snippets
   - PostgreSQL (by Chris Kolkman)

### Step 2: Install Node.js and npm
1. Download Node.js from [https://nodejs.org/](https://nodejs.org/)
2. Install the **LTS (Long Term Support)** version
3. Verify installation by opening a terminal and running:
   ```bash
   node --version
   npm --version
   ```
4. You should see version numbers for both (Node v20+ and npm v10+ recommended)

### Step 3: Install Git (if not already installed)
1. Download Git from [https://git-scm.com/](https://git-scm.com/)
2. Install for your operating system
3. Configure Git with your information:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

## GitHub Setup

### Step 4: Join the GitHub Classroom Course
1. Click the GitHub Classroom link provided in Canvas
2. Authorize GitHub Classroom to access your GitHub account
3. Accept the assignment
4. GitHub Classroom will create a unique repository for you with the starting template

### Step 5: Clone Your Repository
1. Copy the repository URL from your GitHub repository page (green "Code" button)
2. Open a terminal/command prompt
3. Navigate to where you want to store your projects:
   ```bash
   cd ~/Documents  # or your preferred location
   ```
4. Clone the repository:
   ```bash
   git clone <your-repository-url>
   cd CSC425FA26
   ```
5. Open the project in VSCode:
   ```bash
   code .
   ```
   Or open VSCode and use File → Open Folder to select the CSC425FA26 folder

## Project Setup (Vite + React)

### Step 6: Install Project Dependencies
1. Open the integrated terminal in VSCode (View → Terminal or `` Ctrl+` ``)
2. Make sure you're in the project root directory
3. Install all dependencies:
   ```bash
   npm install
   ```
4. Wait for all packages to download and install (this may take a few minutes)

### Step 7: Start the Development Server
1. In the terminal, run:
   ```bash
   npm run dev
   ```
2. You should see output indicating the server is running, typically on `http://localhost:5173`
3. Keep this terminal window open - this is your development server

### Step 8: Open the App in Your Browser
1. Open your web browser (Chrome, Firefox, Safari, or Edge)
2. Navigate to `http://localhost:5173` (or the URL shown in your terminal)
3. You should see your React starter app running
4. Try editing `src/App.jsx` - the browser will automatically refresh with your changes (Hot Module Replacement)

## PostgreSQL Setup

### Step 9: Install PostgreSQL
1. Download PostgreSQL from [https://www.postgresql.org/download/](https://www.postgresql.org/download/)
2. Install PostgreSQL for your operating system
3. During installation, remember the password you set for the `postgres` superuser
4. Default port is `5432` (keep this unless you have a conflict)

### Step 10: Create Your Course Database

**Follow these commands in order:**

1. **Connect to PostgreSQL** (run this in your terminal):
   ```bash
   psql -U postgres
   ```
   Enter your postgres password when prompted.

2. **Create the database** (run this inside the `postgres=#` prompt):
   ```sql
   CREATE DATABASE csc425fa26;
   ```
   You should see: `CREATE DATABASE`

3. **Verify the database was created** (list all databases):
   ```sql
   \l
   ```
   Look for `csc425fa26` in the list.

4. **Exit PostgreSQL**:
   ```sql
   \q
   ```

5. **Connect to your new database** (run this in your terminal):
   ```bash
   psql -U postgres -d csc425fa26
   ```
   You should now see `csc425fa26=#` as your prompt.

6. **Exit when done**:
   ```sql
   \q
   ```

### Step 11: Configure Database Connection
1. Create a `.env` file in your project root (if not already present)
2. Add your PostgreSQL connection details:
   ```
   DB_HOST=localhost
   DB_PORT=5432
   DB_NAME=csc425fa26
   DB_USER=postgres
   DB_PASSWORD=your_password_here
   ```
3. **IMPORTANT**: Never commit your `.env` file to Git (it should be in `.gitignore`)

**Note:** Replace `your_password_here` with the actual password you set during PostgreSQL installation.

## Understanding Your React Starter App

### Project Structure
```
CSC425FA26/
├── public/          # Static assets
├── src/
│   ├── assets/      # Images, fonts, etc.
│   ├── App.jsx      # Main App component
│   ├── App.css      # App styles
│   ├── main.jsx     # Entry point
│   └── index.css    # Global styles
├── index.html       # HTML template
├── package.json     # Dependencies and scripts
├── vite.config.js   # Vite configuration
└── eslint.config.js # ESLint configuration
```

### Available npm Scripts
- `npm run dev` - Start development server with hot reload
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally
- `npm run lint` - Check code for errors and style issues

## Verification Checklist

✅ VSCode installed and running  
✅ Node.js and npm installed (check with `node --version` and `npm --version`)  
✅ GitHub repository cloned locally  
✅ Terminal accessible in VSCode  
✅ Dependencies installed (`node_modules` folder exists)  
✅ Development server running (`npm run dev`)  
✅ App accessible in browser at `http://localhost:5173`  
✅ PostgreSQL installed and running  
✅ PostgreSQL dashboard (pgAdmin or VSCode extension) accessible  
✅ csc425fa26 database created  
✅ React app displays in browser and hot reload works  

## Getting Help

- **React Documentation**: [https://react.dev/](https://react.dev/)
- **Vite Documentation**: [https://vite.dev/](https://vite.dev/)
- **PostgreSQL Documentation**: [https://www.postgresql.org/docs/](https://www.postgresql.org/docs/)
- **Course Resources**: Check Canvas for additional materials

## Next Steps

Once your environment is set up, you're ready to start building! Check Canvas for your first assignment.

---

**Course**: CSC425FA26  
**Semester**: Fall 2026
