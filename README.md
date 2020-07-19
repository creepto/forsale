# .crypto Domain For Sale single-page

## How to deploy

1. Edit `index.html` and replace these strings:
    1. Feel free to change the messaging, add initial price etc. - make this your own
    1. Replace MYDOMAIN -> with the domain name you're selling
    1. Replace MYEMAIL  -> with the email you want people to use to contact you
    1. Replace MYTELEGRAM -> with your Telegram user **or** remove this section if you don't have/want one
    1. Replace MYTWITTER -> with your Twitter user **or** remove this section if you don't have/want one
1. Get your .crypto domain at [Unstoppable Domains](https://unstoppabledomains.com/)
1. The easiest way to publish your HTML to IPFS is using a service called [Pinata](https://pinata.cloud). So go there, create a free user (good for 1GB) and sthen log in select [Pinata Upload](https://pinata.cloud/pinataupload) from the top menu
1. Let's upload our files:
    1. Copy the `index.html` and the `assets` folder to a temp folder on your machine. We do this to avoid uploading the other files in this repo (like this README) to IPFS as they're not needed
    1. Select the "Upload Directory" button, browse to your temp folder, and type a name that will remind you what this site is (like your domain name)
    1. After a few seconds, your folder is uploaded. Navigate to "Pin Explorer", and copy the IPFS Hash
1. Let's point your .crypto domain to the page you just uploaded:
    1. Go back to Unstoppable Domains, select "My Domains" from the menu, select your domain and click the "Manage" button
    1. Click the "website" link
    1. Paste the IPFS Hash, click "Save Changes" and approve the transaction
    1. Depending on network traffic, the transaction will take from 30 secoonds to 30 minutes. You can check the progress in the "My Transactions" view
1. Once done, you can browse to yourdomain.crypto and see the for sale page!

### Important

At the time of this writing, only Opera browser supports .crypto domains. To see them in Chrome/Brave/Edge, install the [Unstoppable Domains Chrome Extension](https://chrome.google.com/webstore/detail/unstoppable-extension/beelkklmblgdljamcmoffgfbdddfpnnl?hl=en-US&authuser=0) from the Chrome Webstore. In the futture, more browsers will be able to redirect to .crypto domains outt of the box.
