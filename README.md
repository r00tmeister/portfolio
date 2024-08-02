# Virtual CV Portfolio Documentation

## Introduction
Welcome to the documentation for the Virtual CV Portfolio of r00tmeister. This project showcases a personal CV and portfolio, built with Nuxt.js and styled using Tailwind CSS.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Technology Stack](#technology-stack)
4. [Setup and Installation](#setup-and-installation)
5. [Project Structure](#project-structure)
6. [Customization](#customization)
7. [Deployment](#deployment)
8. [Contributing](#contributing)
9. [License](#license)
10. [Acknowledgements](#acknowledgements)

## Project Overview
The Virtual CV Portfolio is a web application designed to showcase personal information, professional experience, skills, and projects in an interactive and visually appealing format.

## Features
- **Responsive Design:** Optimized for both desktop and mobile devices.
- **Utility first and modular design:** Built using modular utility first Tailwind and Nuxt.
- **Easy Customization:** Built with modular components for easy updates.

## Future Considerations
- **Dynamic Content:** Fetch data dynamically to keep the portfolio up-to-date. Currently using objects, will in the future incorporate NoSQL DB to pull the data from. Possible inlcude LinkedIn API and Github API in the future to dynamically pull latests profile information and projects to the portfolio.

## Technology Stack
- **Frontend Framework:** Nuxt.js
- **Styling:** Tailwind CSS
- **Backend:** N/A (Static Site)
- **Hosting:** [GithubPages]
- **Other Tools:** [Pinia]

## Setup and Installation
### Prerequisites
- Node.js (see package.json for version)
- npm

### Installation Steps
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/your-repo.git
   ```
2. **Navigate to the Project Directory:**
   ```bash
   cd your-repo
   ```
3. **Install Dependencies:**
   ```bash
   npm install
   ```
4. **Run the Development Server:**
   ```bash
   npm run dev
   ```

## Project Structure
- **/assets:** Static assets like images and fonts.
- **/components:** Vue components used throughout the application.
- **/layouts:** Layout components that wrap around pages.
- **/pages:** Vue files corresponding to the app's pages.
- **/static:** Static files to be served as-is.
- **/store:** Vuex store for state management.
- **/nuxt.config.js:** Nuxt configuration file.

## Customization
### Changing Content
To update the content, modify the pages and their respective components.

### Styling
Tailwind CSS is used for styling. You can customize the design by editing the `/tailwind.config.js` file and the component inline styles.

## Deployment
### Building for Production
1. **Build the Project:**
   ```bash
   npm run build
   ```
2. **Generate Static Files:**
   ```bash
   npm run generate
   ```
3. **Deploy to Hosting Service:**
   ```bash
   git add .
   ```
    ```bash
   git push origin main
   ```
   There is a github actions workflow file that will automatically deploy the code being pushed to the main branch.

## Contributing
We welcome contributions! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgements
- Nuxt.js for providing a great development framework.
- Tailwind CSS for the utility-first CSS framework.
