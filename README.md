# .crypto Domain For Sale single-page

### Check out the demo: [https://creepto.github.io/forsale/](https://creepto.github.io/forsale/).

## How to deploy the site to IPFS and point your new domain to it

### Important note

At the time of this writing, only Opera browser supports .crypto domains. To see them in Chrome/Brave/Edge, install the [Unstoppable Domains Chrome Extension](https://chrome.google.com/webstore/detail/unstoppable-extension/beelkklmblgdljamcmoffgfbdddfpnnl?hl=en-US&authuser=0) from the Chrome Webstore. In the futture, more browsers will be able to redirect to .crypto domains outt of the box.

### 1. Setup

1. Clone this repo, or [download the zip](https://github.com/creepto/forsale/archive/master.zip)
1. Get your .crypto domain at [Unstoppable Domains](https://unstoppabledomains.com/) - **I do not use referral links. Ever.**
1. The easiest way to publish your HTML to IPFS is using a service called [Pinata](https://pinata.cloud). So go there, create a free user (good for 1GB)

### 2. Edit the code

Feel free to change the messaging, add initial price etc. - make the site your own. There are 2 ways to build the site:

#### 2.1 Build the site manually (beginner)

1. Edit the `index.html` and replace these strings:
    1. Replace %MYDOMAIN% -> with the domain name you're selling
    1. Replace %MYEMAIL%  -> with the email you want people to use to contact you
    1. Replace %MYTELEGRAM% -> with your Telegram user **or** remove this section if you don't have/want one
    1. Replace %MYTWITTER% -> with your Twitter user **or** remove this section if you don't have/want one
1. You can also remove the script section at the bottom of the page, if you handled the Twitter/Telegram sections manually 
1. Copy the `index.html` and the `assets` folder to a temp folder on your machine. We do this to avoid uploading the other files in this repo (like this README) to IPFS as they're not needed. In the next step we'll upload this folder

#### 2.2 Build the site automatically (advanced)

1. Install all dependencies: `yarn install` or `npm install`
1. Create a `.env` file at the root of the directory. It expects 4 variables. See the file `.env.sample`.  
The `%MYTWITTER%` and `%MYTELEGRAM%` variables can be left empty, but the domain name and email are manadatory.
1. Run the `build` command: `yarn build` or `npm run build`.  
This will replace all the strings in the HTML and create a `build` folder with all the assets. In the next step we'll upload this folder

## 3. Uploading the files
  
1. Log into Pinata, and then select [Pinata Upload](https://pinata.cloud/pinataupload) from the top menu
1. Select the "Upload Directory" button, browse to your temp folder, and type a name that will remind you what this site is (like your domain name)
1. After a few seconds, your folder is uploaded. Navigate to "Pin Explorer", and copy the IPFS Hash

## 4. Pointing our domain to the site

1. Go back to Unstoppable Domains, select "My Domains" from the menu, select your domain and click the "Manage" button
1. Click the "website" link
1. Paste the IPFS Hash, click "Save Changes" and approve the transaction
1. Depending on network traffic, the transaction will take from 30 seconds to 30 minutes. You can check the progress in the "My Transactions" view
1. Once done, you can browse to yourdomain.crypto and see the for sale page!
