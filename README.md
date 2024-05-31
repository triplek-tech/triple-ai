# Introduction
**triple-ai** accelerates modern web app development by seamlessly integrating Turborepo's monorepo features with Strapi's adaptable CMS Backend. It simplifies managing multiple packages and apps in one repository, utilizing Turborepo's tools for dependency management and task automation. Strapi enhances content creation and management with its intuitive interface and extensive plugin support. Whether you're a seasoned developer or new to the field, triple-ai provides a versatile platform for crafting innovative web experiences. Join us as we redefine web app development with Turborepo and Strapi.


## :ledger: Index

- [About](#beginner-about)
- [Usage](#zap-usage)
  - [Installation](#electric_plug-installation)
  - [Commands](#package-commands)
- [Development](#wrench-development)
  - [Pre-Requisites](#notebook-pre-requisites)
  - [Development Environment](#nut_and_bolt-development-environment)
  - [File Structure](#file_folder-file-structure)
  - [Build](#hammer-build)  
  - [Deployment](#rocket-deployment)  
- [Community](#cherry_blossom-community)
  - [Contribution](#fire-contribution)
  - [Branches](#cactus-branches)
  - [Guideline](#exclamation-guideline)  
- [FAQ](#question-faq)

##  :beginner: About
Welcome to triple-ai! Whether you're new to coding or a seasoned developer, this project is an initial basic setup leveraging Turborepo and Strapi. Our primary goal is to provide a foundational structure for building modern web applications with ease. Here, you'll find an introduction to the Turborepo monorepo setup, which streamlines package and app management, alongside Strapi, a powerful headless CMS. Our aim is to create a seamless environment where developers can efficiently develop, deploy, and scale web applications. Join us as we embark on this journey with triple-ai, empowering you to craft innovative web experiences. Let's explore the world of Turborepo and Strapi together!

## :zap: Usage
This repository leverages Turborepo for efficient monorepo management and Strapi for a flexible headless CMS. Follow the steps below to get started:
###  :electric_plug: Installation 
Clone the repository and install dependencies for all packages:

```sh
git clone <repository-url>
cd <repository-directory>
```

```sh
npx create-turbo@latest
```

###  :package: Commands
- For front-end web
```sh
cd apps/web
npm run dev
```
- For the backend Strapi
```sh
cd apps/backend
npm run develop
```
### Remote Caching

Turborepo can use a technique known as [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup), then enter the following commands:

```
cd my-turborepo
npx turbo login
```

##  :wrench: Development
If you want other people to contribute to this project, this is the section, make sure you always add this.

### :notebook: Pre-Requisites

Ensure you have the following tools installed:

- Node.js (>= 18.x)
- npm (>= 8.x) or Yarn (>= 1.x)

Additionally, this Turborepo has some additional tools already set up for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

To install Turborepo globally, run the following command:

```sh
npm install turbo --global
```

###  :nut_and_bolt: Development Environment

Setting up the development environment for this monorepo is straightforward. Follow these steps to get your project up and running.

#### 1. Clone the Repository

First, download the project by cloning the repository to your local machine:

```sh
git clone <repository-url>
cd <repository-directory>
npm install
```

###  :file_folder: File Structure
Add a file structure here with the basic details about files, below is an example.

```
.
├── apps
│   ├── backend
│   │   ├── config
│   │   ├── database
│   │   ├── public
│   │   ├── src
│   │   └── tsconfig.json
│   ├── docs
│   │   ├── app
│   │   │   ├── globals.css
│   │   │   ├── layout.tsx
│   │   │   ├── page.module.css
│   │   │   └── page.tsx
│   │   ├── public
│   │   │   ├── circles.svg
│   │   │   ├── next.svg
│   │   │   ├── turborepo.svg
│   │   │   └── vercel.svg
│   │   ├── next-env.d.ts
│   │   ├── next.config.js
│   │   └── tsconfig.json
│   ├── web
│   │   ├── app
│   │   │   ├── globals.css
│   │   │   ├── layout.tsx
│   │   │   ├── page.module.css
│   │   │   └── page.tsx
│   │   ├── public
│   │   │   ├── circles.svg
│   │   │   ├── next.svg
│   │   │   ├── turborepo.svg
│   │   │   └── vercel.svg
│   │   ├── next-env.d.ts
│   │   ├── next.config.js
│   │   └── tsconfig.json
├── packages
├── README.md
├── tsconfig.json
└── turbo.json
```

###  :hammer: Build
- Before going to production make sure to make the production ready build with this following commond.
```sh
npm run build
```

### :rocket: Deployment
- To deploy the application, follow these steps:
- Ensure the build step is complete.
- Upload the build artifacts to your server or hosting service.
- Configure your server to serve the built files.
- Refer to the deployment documentation specific to your hosting provider for detailed instructions.

###  :fire: Contribution

Your contributions are always welcome and appreciated. Here are ways you can contribute:

1. **Report a bug** <br>
If you think you have encountered a bug, and I should know about it, feel free to report it [here]() and I will take care of it.

2. **Request a feature** <br>
You can also request for a feature [here](), and if it will viable, it will be picked for development.  

3. **Create a pull request** <br>
It can't get better then this, your pull request will be appreciated by the community. You can get started by picking up any open issues from [here]() and make a pull request.

> If you are new to open-source, make sure to check read more about it [here](https://www.digitalocean.com/community/tutorial_series/an-introduction-to-open-source) and learn more about creating a pull request [here](https://www.digitalocean.com/community/tutorials/how-to-create-a-pull-request-on-github).


### :cactus: Branches

I use an agile continuous integration methodology, so the version is frequently updated and development is really fast.

1. **`stage`** is the development branch.

2. **`master`** is the production branch.

3. No other permanent branches should be created in the main repository, you can create feature branches but they should get merged with the master.

**Steps to work with feature branch**

1. To start working on a new feature, create a new branch github username and prefixed with `feat` and followed by feature name. (ie. `username/feat-FEATURE-NAME`)
2. Once you are done with your changes, you can raise PR.
**Steps to work with issue branch**

1. To start working on a issue, create a new branch github username and prefixed with `issue` and followed by issue name. (ie. `username/issue#Number`)
2. Once you are done with your changes, you can raise PR.

**Steps to create a pull request**

1. Make a PR to `stage` branch.
2. Comply with the best practices and guidelines e.g. where the PR concerns visual elements it should have an image showing the effect.
3. It must pass all continuous integration checks and get positive reviews.

After this, changes will be merged.


### :exclamation: Guideline
coding guidelines or other things you want people to follow should follow.

**Consistent Naming Conventions**
   - Use meaningful and descriptive names for variables, functions, and classes.
   - Follow camelCase for variables and functions, PascalCase for classes, and SCREAMING_SNAKE_CASE for constants.

**Code Formatting**
   - Use a consistent code style for indentation, spacing, and braces. Configure your IDE to use the project's `.editorconfig` or `.prettierrc`.
   - Run a code formatter like Prettier before committing your code.

**Comments and Documentation**
   - Write clear and concise comments for complex logic and important sections of the code.
   - Use JSDoc or similar tools for documenting functions, parameters, and return values.
   - Keep the documentation up-to-date with code changes.

**Modular Code**
   - Break down large functions and classes into smaller, reusable modules.
   - Use design patterns where appropriate to improve code organization and readability.

**Error Handling**
   - Implement proper error handling using try-catch blocks or error-first callbacks.
   - Provide informative error messages and log them appropriately.

**Testing**
   - Write unit tests for all critical functions and modules using testing frameworks like Jest or Mocha.
   - Ensure that your code has good test coverage and that tests are run regularly.

**Version Control**
   - Commit code frequently with clear and descriptive commit messages.
   - Use feature branches for new features or significant changes, and merge them into `stage` or `master` through pull requests.

**Code Reviews**
   - Participate in code reviews to ensure code quality and share knowledge.
   - Be open to feedback and constructive criticism to improve the codebase.

**Prototyping**
   - Create prototypes for complex features before full implementation to validate ideas and approaches.
   - Use tools like Figma for UI/UX prototyping and flow diagrams.

**Code Refactoring**
   - Regularly refactor code to improve readability, reduce complexity, and eliminate technical debt.
   - Follow the "Boy Scout Rule": Always leave the code better than you found it.

**Performance Optimization**
   - Profile and optimize critical code paths to enhance performance.
   - Use efficient algorithms and data structures to reduce computational overhead.

**Single Responsibility Principle**
   - Ensure that each function or class has a single responsibility and adheres to the SRP.
   
**DRY (Don't Repeat Yourself)**
   - Avoid code duplication by creating reusable functions, modules, and components.

**KISS (Keep It Simple, Stupid)**
   - Write simple and straightforward code. Avoid unnecessary complexity.

**YAGNI (You Aren't Gonna Need It)**
   - Do not add functionality until it is necessary. Focus on the current requirements.

### Additional Resources

- [Clean Code by Robert C. Martin](https://www.goodreads.com/book/show/3735293-clean-code)
- [Design Patterns: Elements of Reusable Object-Oriented Software](https://www.goodreads.com/book/show/85009.Design_Patterns)
- [You Don't Know JS (book series)](https://github.com/getify/You-Dont-Know-JS)

By following these guidelines and best practices, we can maintain a high-quality codebase that is easy to understand, maintain, and extend.


## :question: FAQ
You can optionally add a FAQ section about the project.
**What is Turborepo?**
    Turborepo is a high-performance build system for JavaScript and TypeScript codebases. It helps manage monorepos efficiently by providing incremental builds, caching, and parallel execution.

**What is Strapi?**
    Strapi is an open-source headless CMS that provides a flexible and customizable backend for managing content. It allows you to create APIs quickly and efficiently.

**How do I run the backend and frontend applications simultaneously?**
    To run both the backend and frontend applications, you can use Turborepo's built-in commands to start all services concurrently:
    ```sh
    npm run dev
    ```
## :star2: Credit/Acknowledgment

This project is made possible thanks to the dedication and contributions of many individuals. Special thanks to:

- **[Your Name]** - Project Lead and Primary Developer
- **[Contributor Name]** - Frontend Development and UI/UX Design
- **[Contributor Name]** - Backend Development and API Integration
- **[Contributor Name]** - Documentation and Testing

We would also like to acknowledge the following open-source projects that have been instrumental in the development of this project:

- **[Turborepo](https://turborepo.org/)** - High-performance build system for managing monorepos.
- **[Strapi](https://strapi.io/)** - Open-source headless CMS for building customizable APIs.

A huge thank you to our community for providing valuable feedback, reporting issues, and contributing code. Your support and engagement are vital to the project's success.

For a complete list of contributors, please see the [Contributors](https://github.com/your-repo/contributors) page on GitHub.

---
