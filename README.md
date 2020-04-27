# GoIndex
Google Drive Directory Index, combining the power of [Cloudflare Workers](https://workers.cloudflare.com/) and [Google Drive](https://www.google.com/drive/) will allow you to index your files on the browser on Cloudflare Workers.  

`index.js` is the Workers script.  

# Deploy
1. Install `rclone` software locally  
2. Follow [https://rclone.org/drive/](https://rclone.org/drive/) bind a drive  
3. Run `rclone config file` to find the path of `rclone.conf`  
4. Find `root_folder_id` and `refresh_token` in the given path  
5. Download [index.js](index.js) and fill in `root_folder_id` and `refresh_token  `
6. Deploy the code to [Cloudflare Workers](https://workers.cloudflare.com/)

# Access Passwords
Add `.password` in the drive to set up a password for that directory.  
The passwords only prevents unauthorized directory listing for the sole directory, not for the child directories, nor does it prevent unauthorized file download.

`root_pass` in [index.js](index.js] is only for `/`, and is preferred over `.password` file.

# Updates
* Fixed that the project being unusable because hardcoded values that depended on original authors repo
* Fix the url where they should've been urlencode'd
* Translated into English

# About
The active author deleted the repository. I'll be maintaining this on my own. There will likely be no new features, just bug fixes.  
This is an open source project. Any of the authors or contributors are not responsible for any consequences.
