 # Shopify Dev Store


[<img src="src/assets/images/devworthy_amiresponsive_whole.png" alt="An image representing how the site looks across different devices of varying size.">](https://anthonyradose.github.io/dev-worthy/#/)


By Alan, Anthony, Ieuan, Krish, and Melody


[🔗 View the live project here.](https://anthonyradose.github.io/dev-worthy/#/)


This is the documentation for DevWorthy – a motivational web app designed to support aspiring developers in overcoming imposter syndrome. Built using ReactJS with JSX, Bootstrap CSS for styling, and modern JavaScript practices, the site was developed as part of the April 2025 Code Institute Hackathon.


## ✅ Criteria

1. 🧩 The team has built one of the 5 suggested projects  
2. 💡 The team has innovated on their choice of project  
3. 📱 The project is fully responsive  
4. 📋 The project is well planned using GitHub Projects or other issue board tools

---

## 🧠 User Experience - UX

### 🎯 Strategy

This project has been built as a collaborative project through [Code Institute](https://codeinstitute.net/) as a learning tool for working in a professional environment through:

- 🤝 Teamwork  
- 🚀 Exposure to Agile Development  
- 🔄 Experience with version control  
- 📈 Adding to CV and portfolio  
- 🌐 Exposure on social media  
- ⏱️ Delivering projects to tight deadlines

The aim is to create a site that spreads positive and uplifting messages that users can view daily to remind themselves that they are worthy of the goals they pursue.

#### 🧭 User Goals

- 💬 View inspiring quotes  
- 👩‍💻 View coding tips and tricks  
- ⭐ Save quotes to favourites  
- 🧑‍🤝‍🧑 View information about the team

<sup><sub>[🔝 Back to top](#devworthy)</sub></sup>


-----

### 📦 Scope

The scope of DevWorthy was to create a clean, uplifting web app that delivers motivational content to developers experiencing imposter syndrome. The MVP focused on displaying daily affirmations, ensuring accessibility, responsiveness, and a positive user experience.

Features such as user accounts, quote submissions, or personalization were considered out of scope for the hackathon timeframe but could be explored in future iterations.

The project emphasized:

- ✨ Clean UI  
- 📱 Mobile-first design  
- 🛠️ Showcasing modern frontend development tools

<sup><sub>[🔝 Back to top](#devworthy)</sub></sup>

---

### 🧱 Structure

#### 🗺️ Site Structure

As the purpose of the initial site is quite simple, the navigation route is linear, encouraging users to explore quotes, the dev team, and favourites. Navigation includes quote saving/removal and internal linking between sections.

- 🏠 **Home Page:** Provides an inspiring quote. Users can add quotes to favourites or refresh for a new one.  
- 👥 **Credits Page:** Showcases the April 2025 Hackathon Team 4.  
- ⭐ **Favourites Page:** Displays saved quotes and allows users to remove them.

<sup><sub>[🔝 Back to top](#devworthy)</sub></sup>

---

### 🧩 Skeleton

#### 📝 Wireframes


<img src="src/assets/images/DevWorthy_wireframes1.png" alt="Wireframe for homepage" width="400"/>

<img src="src/assets/images/DevWorthy_wireframes2.png" alt="Wireframe for about page" width="400"/>

<img src="src/assets/images/DevWorthy_wireframes3.png" alt="Wireframe for favourites page" width="400"/>

All wireframes have been created with [Balsamiq](https://balsamiq.com/).

<sup><sub>[🔝 Back to top](#devworthy)</sub></sup>

---

## 🎨 User Interface - Design

### 🧁 Surface

The design of the site has been implemented using [Bootstrap](https://getbootstrap.com/) styling across the site. This framework was chosen due to the experience of team members. Streamlining the main aspects of the site's style allowed for members to spend more time with functionality and content creation.

#### 🔤 Typography

Fonts have been imported from [Google Fonts](https://fonts.google.com/).


[Poppins:](https://fonts.google.com/specimen/Poppins) This geometric sans-serif font is used for headers and titles due to its modern, stylish appearance and strong visual presence. Its clean lines and bold weights make it ideal for grabbing attention while maintaining clarity and professionalism.


[Roboto:](https://fonts.google.com/specimen/Roboto?query=roboto) This sans-serif font is used for the main body text due to its clean, modern look and excellent readability, especially on mobile devices and at small sizes.

#### 🎨 Colours

<img src="src/assets/images/DevWorthy_colorScheme.png" alt="Wireframe for favourites page" width="400"/>


Colour scheme images made with [coolers](https://coolors.co).

<sup><sub>[🔝 Back to top](#devworthy)</sub></sup>

-------

## ✨ Features

### 🌐 Site Features

#### 🔖 Favicon

<img src="src/assets/images/DevWorthy_favicon.png" alt="Favicon" width="200"/>

Favicon generated with [Favicon.io](https://favicon.io/) using the logo image for the site.

#### Navbar

| Feature | Description | Image |
| :---: | :---: | :---: |
| Brand logo | The brand logo acts as navigation back to the homepage | <img src="src/assets/images/dev-worthy-logo.png" alt="Brand logo" width="200"/> |
| Desktop navigation | This is how the navbar appears on desktop | <img src="src/assets/images/devworthy_desktopheader.png" alt="Navbar desktop view" width="200"/> |
| Mobile navigation | This is how the navbar appears on mobile | <img src="src/assets/images/devworthy_mobileheader.png" alt="Navbar mobile view" width="200"/>

#### Footer

| Feature | Description | Image |
| :---: | :---: | :---: |
| Desktop Footer | This is how the footer appears on desktop | <img src="src/assets/images/devworthy_desktopfooter.png" alt="Footer desktop view" width="200"/> |
| Mobile Footer | This is how the footer appears on mobile | <img src="src/assets/images/devworthy_mobilefooter.png" alt="Footer mobile view" width="200"/> |

#### Home

<img src="src/assets/images/devworthy_amiresponsive_home.png" alt="An image representing how the homepage looks across different devices of varying size.">

| Feature | Description |
| :---: | :---: |
| __Daily Quote__ | User can view a daily inspirational quote |
| __Dev Tips__ | User can view a dev tip to boost motivation |
| __Add to favourites__ | User can add quote to the favourites page |
| __Generate new quote__ | User can generate a new quote |

##### Feature App - Quote Generator

A simple quote generator app built using **Vite** and **React.js** that displays affirmation quotes from an external API. Quotes are selected at random when the user clicks the button.

---

###### 🔧 Features & Functionality

- **User Interface:** Built with React and Vite for a fast, responsive experience.
- **Random Quotes:** On button click, a new quote is fetched and displayed.
- **Loading/Error States:** Handles loading and API errors gracefully.

---

###### 🧠 React Concepts Used

 `useState`
`useState` is a React hook that allows you to add state (data that changes over time) to functional components.

It’s used to:
- Remember values between renders
- Store user input, counters, or fetched data

---

###### 🔄 Fetching Quotes from the API

Quotes are fetched using the `fetch()` function, and the component’s state is updated using `setQuote()`.

>```js
>const response = await fetch('https://api.example.com/quote');
>const data = await response.json();
>setQuote(data);
>

#### Favourites

<img src="src/assets/images/devworthy_amiresponsive_favourites.png" alt="An image representing how the favourites page looks across different devices of varying size.">

| Feature | Description |
| :---: | :---: |
| __Favourites view__ | User can see their favourites |
| __Remove from favourites__ | User can remove a quote from favourites |

#### Credits

<img src="src/assets/images/devworthy_amiresponsive_credits.png" alt="An image representing how the credits page looks across different devices of varying size.">

| Feature | Description |
| :---: | :---: |
| __View team 4__ | User can view members of the team! |
| __View team links__ | User can flip a team member's card to view their socials |

#### 404

<img src="src/assets/images/devworthy_404.png" alt="An image representing how the 404 page looks across different devices of varying size.">

<sup><sub>[*Back to top*](#devworthy)</sup></sub>


------

## 🚀 Future Implementations

| Feature | Description |
|----|----|
| Character limit on quotes | Some quotes generated by the API are very long, we would like to keep generated quotes below a certain character limit to keep a consistent look. |
| **Quote Submission Form** | Allow users to submit their own quotes. |
| **User Authentication** | Enable user accounts to save favorites, submit content, or personalize the site. |
| **Dark Mode Toggle** | Improve accessibility and UX with a light/dark theme switch. |
| **Search & Filter** | Let users quickly find content via tags, categories, or keywords. |
| **Accessibility Enhancements** | Add ARIA roles, improve keyboard navigation, and screen reader support. |
| **Multilingual Support** | Implement i18n for broader accessibility across languages. |

<sup><sub>[🔝 Back to top](#devworthy)</sub></sup>

-----

## ♿ Accessibility

### 🖼️ Alt Text

Alternative text has been included for all images across the site to ensure that visually impaired users can understand the content through screen readers.

### 🏷️ Aria Labels

Aria labels have been included for all links across the site with modals labelled by their headings, enhancing screen reader navigation and improving the experience for users with disabilities.

### 🎨 Colours

Colours are simple with high contrast between background and content, ensuring that text is easily readable by users with varying levels of vision.

### 🔤 Fonts

Fonts have been chosen for their simple style, promoting easy reading and ensuring legibility for all users.

<sup><sub>[🔝 Back to top](#devworthy)</sub></sup>

-------

## Technologies Used

### 🧠 Languages & Technologies Used

| Tool/Language | Category | Purpose |
|----|----|----|
| ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) / ![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) | Programming / Framework | Main logic for components, interactivity, and UI |
| ![JSX](https://img.shields.io/badge/JSX-61DAFB?style=for-the-badge&logo=react&logoColor=white) | Syntax Extension     | Combines JavaScript and HTML-like syntax in React components             |
| ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) | Markup Language      | Defines the structure of content via JSX                                 |
| ![JSON](https://img.shields.io/badge/JSON-292929?style=for-the-badge&logo=json&logoColor=white) | Data / Config Format | Used in configuration files like `package.json` |
| ![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white) | Documentation | Used for writing documentation like `README.md` |

### 🚀 Built With

| Tool/Framework | Category | Purpose |
|----|----|----|
| ![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) | Frontend | Core JavaScript framework used to build reusable UI components. |
| ![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white) | Build Tool | Fast dev server and build tool that bundles your app for production. |
| ![gh-pages](https://img.shields.io/badge/gh--pages-deploy-blue?style=for-the-badge&logo=github) | Deployment | Deploys your production build to GitHub Pages. |
| ![npm](https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white) | Package Manager | Manages dependencies and scripts for the project. |
| ![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=for-the-badge&logo=eslint&logoColor=white) / ![Prettier](https://img.shields.io/badge/Prettier-F7B93E?style=for-the-badge&logo=prettier&logoColor=black) | Linting/Formatting | Ensures code quality and formatting consistency (if configured). |

>#### React + Vite
>
>This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.
>
>Currently, two official plugins are available:
>
>- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) >uses [Babel](https://babeljs.io/) for Fast Refresh
>- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/>plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
>
>##### Expanding the ESLint configuration
>
>If you are developing a production application, we recommend using TypeScript with type-aware lint >rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/>create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`]>(https://typescript-eslint.io) in your project.
>

### 🛠️ Libraries & Tools

| Library/Tool | Category | Purpose |
|----|----|----|
| ![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) | Frontend Framework | Core JavaScript framework for building UI components. |
| ![ReactDOM](https://img.shields.io/badge/ReactDOM-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) | DOM Rendering | Provides DOM-specific methods for React. |
| ![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white) | Build Tool | Fast development server and build tool. |
| ![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=for-the-badge&logo=eslint&logoColor=white) | Linting Tool | Identifies and reports on patterns found in ECMAScript/JavaScript code. |
| ![ESLint Plugin React Hooks](https://img.shields.io/badge/ESLint_plugin--react--hooks-61DAFB?style=for-the-badge&logo=react&logoColor=white) | Linting Plugin | Enforces best practices for React Hooks. |
| ![ESLint Plugin React Refresh](https://img.shields.io/badge/ESLint_plugin--react--refresh-61DAFB?style=for-the-badge&logo=react&logoColor=white) | Linting Plugin | Ensures React Fast Refresh is properly configured. |
| ![TypeScript Definitions for React](https://img.shields.io/badge/@types--react-61DAFB?style=for-the-badge&logo=typescript&logoColor=white) | Type Definitions    | Provides TypeScript definitions for React. |
| ![TypeScript Definitions for ReactDOM](https://img.shields.io/badge/@types--react--dom-61DAFB?style=for-the-badge&logo=typescript&logoColor=white) | Type Definitions    | Provides TypeScript definitions for ReactDOM. |
| ![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white) | CSS Framework | Frontend framework for building responsive websites. |
| ![gh-pages](https://img.shields.io/badge/gh--pages-deploy-blue?style=for-the-badge&logo=github) | Deployment Tool | Deploys your production build to GitHub Pages. |
| ![Vite Plugin React SWC](https://img.shields.io/badge/@vitejs/plugin--react--swc-646CFF?style=for-the-badge&logo=vite&logoColor=white) | Vite Plugin | Enables React support in Vite using SWC. |


### 🧰 Programs & Tools Used

| Program/Tool | Purpose |
|----|----|
| [Git](https://git-scm.com/) | Version control and collaboration |
| [GitHub](https://github.com/) | Hosting the project and managing source code |
| [Google Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools) | Debugging, inspecting elements, and testing responsiveness |
| [Favicon.io](https://favicon.io/) | Creating the site favicon |
| [Figma](https://figma.com/) | Creating wireframes and visual assets |
| [Balsamiq](https://balsamiq.com/) | Wireframe and mockup creation |
| [JSHint](https://jshint.com/) | JavaScript code validation and linting |
| [UI.dev](https://ui.dev/) | Displaying and testing layout across screen sizes |
| Samsung Talkback | Accessibility testing on mobile devices |


### 🧪 Testing and Validation Tools

| Tool/Service | Purpose |
|----|----|
| ![Samsung Talkback](https://img.shields.io/badge/Samsung_Talkback-077ABC?style=for-the-badge&logo=samsung&logoColor=white) | To test accessibility features on mobile devices. |
| [![UI.dev](https://img.shields.io/badge/UI.dev--Am_I_Responsive%3F-000?style=for-the-badge&logo=google-chrome&logoColor=white)](https://ui.dev/amiresponsive) | To preview the site across a range of screen sizes. |
| [![W3C Validator](https://img.shields.io/badge/W3C_Validation-HTML%2FCSS-005A9C?style=for-the-badge&logo=w3c&logoColor=white)](https://validator.w3.org/) | To validate the site's HTML and CSS for standards compliance. |

<sup><sub>[*Back to top*](#devworthy)</sup></sub>

-------

## 📦 Deployment & Local Development

### 🔄 Local Deployment

#### 🍴 How to Fork

By forking the GitHub Repository, we make a copy of the original repository on our GitHub account to view and/or make changes without affecting the original owner's repository.  
You can fork this repository by using the following steps:

1. Log in to GitHub and locate the [GitHub Repository](https://github.com/anthonyradose/dev-worthy)
2. At the top of the Repository (not top of page) just above the "Settings" Button on the menu, locate the "Fork" Button.
3. Once clicked, you should now have a copy of the original repository in your own GitHub account!

#### 📥 How to Clone

You can clone the repository by following these steps:

1. Go to the [GitHub repository](https://github.com/anthonyradose/dev-worthy)
2. Locate the Code button above the list of files and click it
3. Select if you prefer to clone using HTTPS, SSH, or GitHub CLI and click the copy button to copy the URL to your clipboard
4. Open Git shell or Terminal
5. Change the current working directory to the one where you want the cloned directory
6. In your IDE Terminal, type the following command to clone my repository:
    - `git clone -URL-`
7. Press Enter to create your local clone.

<sup><sub>[🔝 Back to top](#devworthy)</sup></sub>

-----

## 🧪 Testing

Please see [TESTING.md](TESTING.md) for all testing elements of this site.

<sup><sub>[🔝 Back to top](#devworthy)</sup></sub>

-----

## 🏆 Credits & Acknowledgements

### 🔧 Code Used

* **[Quote Generator Walkthrough](https://github.com/codingWithElias/react-random-quote-generator)** – A guide for creating a dynamic quote generator with React.
* **[Video Header](https://jsfiddle.net/StartBootstrap/enajc82d/)** – A customizable video header template to enhance the UI.

---

### 💡 APIs Implemented

We've integrated some awesome APIs for your daily dose of inspiration and dev tips:

* **[Affirmation Quotes API](https://github.com/well300/quotes-api)** – Get a random affirmation quote to boost your spirits.
* **[Dev Tips API](https://github.com/OmerMohideen/programming-quotes-api)** – Handy programming quotes to keep your code game strong.

---

### 🎨 Design & Content

* **[Favicon.io](https://favicon.io/)** – Used to create the perfect custom favicons for the site.
* **[Google Fonts](https://fonts.google.com/)** – Offering stylish fonts that enhance readability and appeal.

---

### 📸 Media

* **[UI.dev - AmiResponsive](https://ui.dev/amiresponsive)** – Showcasing the site's responsive design with sleek device mockups.
* **[ChatGPT](https://chat.openai.com/)** – Helped generate the logo, adding a creative touch to our project.
* **[Bootstrap Icons](https://icons.getbootstrap.com/)** – Providing icons that bring life and clarity to the interface.

---

### 🙏 Special Thanks

A huge shoutout to our team for all the effort and dedication in bringing **DevWorthy** to life:

- [**Alan**](https://github.com/llancruzz) – The visionary behind the app’s design and overall concept, with significant contributions to the UX to ensure a seamless user experience.
- [**Anthony**](https://github.com/anthonyradose) – The dev guru who helped shaped logic and functionality, handled API integration, did extensive debugging, and ensured everything was working smoothly.
- [**Ieuan**](https://github.com/IeuanPriede) – The architect of the user interface, responsible for design and structuring of pages.
- [**Krish**](https://github.com/kslg) – The wizard who brought the quote generator to life by implementing its core React functionality and integrating the external API for seamless user experience.
- [**Melody**](https://github.com/Melody-Lisa) – Scrum Master, keeping the team on track, and managing the majority of the documentation throughout the project.

---

<sup><sub>[*Back to top*](#devworthy)</sup></sub>
