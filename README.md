📝 Installing Stencil CLI for Mac - Documentation 🖥️

✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨

📖 Introduction 🌟

This documentation provides step-by-step instructions for installing the Stencil Command-Line Interface (CLI) on macOS. It covers the process of downloading the base theme "Cornerstone," initializing the CLI, and launching it. For detailed instructions and additional information, please refer to the official Stencil developer portal.

⚙️ Prerequisites 🛠️

Before installing the Stencil CLI on your Mac, make sure you have the following dependencies installed:

Xcode Development Tools: Install the latest stable version of Xcode Development Tools from the App Store. 💻

Node.js (NPM): Install the recommended version of Node.js. Check the documentation for the current recommended version. 🌐

🚀 Installation Steps 🛠️

Open Terminal on your macOS. 🖥️

Install the Stencil CLI globally by executing the following command in the Terminal:

bash
Copy code
npm install -g @bigcommerce/stencil-cli
During the installation process, you might see some warnings about deprecated components. You can safely ignore these warnings. ⚠️

Once the CLI installation completes, clone the base theme "Cornerstone" to your local environment. In the Terminal, navigate to the desired installation directory and run the following command:

bash
Copy code
git clone https://github.com/bigcommerce/cornerstone.git
🎨 Theme Setup 🎨

Navigate to the theme directory using Terminal:

bash
Copy code
cd /path/to/theme/directory
Install the Stencil Utils module for the theme by running the following command:

bash
Copy code
npm install @bigcommerce/stencil-utils
Note: If you later clone a new version of Cornerstone, remember to rerun this command in the new theme directory before initializing Stencil.

⚙️ API Account Creation ⚙️

Before initializing Stencil, you need to create an API account for the BigCommerce store you will be developing on:

Log in to the store's control panel and go to Advanced Settings > API Accounts. 🔑

Click the Create API Account button in the upper left corner.

Provide a username (e.g., "stencil") and set the theme's scope. For local development, choose Read-Only to connect to the store using browser sync.

Read-Only: Allows you to preview changes on the storefront using browser sync. 👀
Modify: Enables applying themes to a store via the command-line interface (CLI).
Save the settings. A pop-up window will display your client ID and access token. Save these credentials and the accompanying text file in a secure location, as you won't be able to view the token information again. 📝🔒

🚀 Initializing Stencil 🛠️

Make sure you are still in the theme directory in Terminal.

Run the following command to initialize Stencil:

bash
Copy code
stencil init
When prompted, enter the homepage URL of the store you will be developing against locally.

When asked for the port to run the local store, you can press Enter to use the default value (3000) or specify a different port.

Enter your API credentials as follows:

Client ID: Enter the client ID obtained during API account creation.
Access Token: Enter the access token obtained during API account creation.
After entering the credentials, you should receive a confirmation that Stencil has been successfully initialized. ✅

🚀 Launching the Theme 🚀

With Stencil initialized, launch your theme using the following command:

bash
Copy code
stencil start
After starting, Terminal will display a list of URLs to access the local store, including external URLs for testing on other devices.

Open one of the URLs (e.g., http://localhost:3000) in a browser to preview the production store with the locally installed Stencil. 🌐
