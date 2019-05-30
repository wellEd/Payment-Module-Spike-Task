# Payment Module Spike Task

Platform OS Payment Module Spike Task with integration to Stripe Payment Gateway

## Installation

### Step 1
Install [Node](https://nodejs.org/en/) in your machine, to have NPM

### Step 2
Using NPM, install `marketplace-kit` CLI
Start your command-line tool (e.g. Terminal on a Mac, or Git Bash on Windows), and enter:

```bash
npm install -g @platform-os/marketplace-kit
```
If your Node.js is installed for all users you might need to use `sudo` to install NPM packages globally:
```bash
sudo npm install -g @platform-os/marketplace-kit
```

### Step 3
Extract the ZIP file into your desired directory

### Step 4
You have to get access to [Partner Portal](https://portal.apps.near-me.com/)

```bash
marketplace-kit env add [environment] --email [your email] --url [your Instance URL]
```


## Payment Module Installation

Separate modules are need to be installed to use unto your project, simply follow the steps bellow for quick installation.

### Installation with Partner Portal
1. Go to [modules marketplace](https://portal.apps.near-me.com/module_marketplace) and click on "Buy" (It's FREE) next to "PlatformOS Payments" and "PlatformOS Payments Stripe" modules.
2. Go to your Instance view and install both modules
3. In the installation process set up Stripe public and secret keys
4. Make sure enable_sms_and_api_workflow_alerts_on_staging in your instance configuration is set to true


### Manual installation

1. Open terminal and go to your instance code root directory
2. Install PlatfromOS Payment Module from GitHub repository
  ```
  git submodule add https://github.com/mdyd-dev/platformos-payments modules/payments
  ```
3. Install PlatfromOS Stripe Module from GitHub repository
```
git submodule add https://github.com/mdyd-dev/platformos-payments-stripe modules/stripe
```
4. Edit `modules/stripe/template-values.json` and set Stripe public and secret keys
5. Deploy instance.
6. Make sure enable_sms_and_api_workflow_alerts_on_staging in your instance configuration is set to true


## Usage
Deploy project to instance
```bash
marketplace-kit deploy [environment]
```

A Environment URL will be displayed in your terminal

```bash
Environment [environment_url]
```

## More Details

Read the documentation for the concept and references for Platform OS [here](https://documentation.platform-os.com/tutorials/).

Payment Module documentation are in the [readme.md](https://github.com/mdyd-dev/platformos-payments/blob/master/README.md) file of their [github repository](https://github.com/mdyd-dev/platformos-payments).
