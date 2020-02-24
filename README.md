# Gridsome Blog Starter

> A simple, hackable & minimalistic starter for Gridsome that uses Markdown for content.

## Features
- Beautiful and simple design.
- Markdown for content.
- Tags support.
- Dark / Light toggle.
- CSS variables, SCSS & BEM for styling.
- 100, 100, 100, 100 score on Google Lighthouse.
- Uses same front-matter fields as Dev.to.

## Demo URL

https://gridsome-starter-blog.netlify.com

## Install

### 1. Install Gridsome CLI tool if you don't have

`npm install --global @gridsome/cli`

### 2. Install this starter

1. `gridsome create my-gridsome-site https://github.com/gridsome/gridsome-starter-blog.git`
2. `cd my-gridsome-site` to open folder
3. `gridsome develop` to start local dev server at `http://localhost:8080`
4. Happy coding 🎉🙌

## 🧐 What's inside?

A quick look at the top-level files and directories you'll see in a Gridsome project.

    .
    ├── package.json
    ├── gridsome.config.js
    ├── gridsome.server.js
    ├── static/
    └── src/
    ├── node_modules
    ├── .gitignore
    ├── LICENSE
    └── README.md
    

1. **`package.json`**: A manifest file for Node.js projects, which includes things like metadata (the project’s name, author, etc). This manifest is how npm knows which packages to install for your project.

2.  **`gridsome.config.js`**: This is the main configuration file for a Gridsome site. This is where you can specify information about your site like the site title, description and options for installed plugins, etc. (Check out the [config docs](https://gridsome.org/docs/config/) for more detail).

3.  **`gridsome.server.js`**: This file is optional and is used to hook into various parts of the Gridsome server. The file must export a function which will have access to the API, etc. (Check out the [config docs](https://gridsome.org/docs/server-api/) for more detail).

4.  **`static`**:  Files in this directory will be copied directly to dist during build. For example, /static/robots.txt will be located at https://yoursite.com/robots.txt

5.  **`/src`**: This directory will contain all of the code related to what you will see on the front-end of your site (what you see in the browser) such as your site header or a page template. `src` is a convention for “source code”.

6.  **`/node_modules`**: This directory contains all of the modules of code that your project depends on (npm packages) are automatically installed.

7.  **`.gitignore`**: This file tells git which files it should not track / not maintain a version history for.

8.  **`LICENSE`**: Gridsome is licensed under the MIT license.

9. **`README.md`**: A text file containing useful reference information about your project.
