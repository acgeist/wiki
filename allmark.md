[Wiki Homepage](index.md)
# Allmark
---
Allmark is a lightweight markdown web server written in go by developer [Andreas Koch](https://andykdocs.de).  
To install I performed the following commands:  
```bash
sudo su
curl -s --insecure https:/allmark.io/bin/files/allmark_linux_amd64 > /usr/local/bin/allmark
chmod +x /usr/local/bin/allmark
```
I then navigated to the directory I wanted to serve and executed:
```bash
cd path/to/your/repository
allmark init
```
Next I opened `.allmark/config` and changed the "Enabled" key to true to enable livereload when the content is being edited.
```
...
"LiveReload": {
   "Enabled": true
},
...
```
Finally, I executed `allmark serve` and navigated to `http://localhost:33001`.  
Of note, when files or folders are added/renamed/deleted/etc., allmark will need to be restarted for the changes to take effect.  Go to the terminal where allmark is running and execute `CTRL+c`, then restart with `allmark serve`.

### References
[allmark website](https://allmark.io)  
[Installation Guide](https://blog.sackad.com/en/2017/09/06/allmark-the-markdown-webserver.html)
---
This page was last updated: Sat 28 Oct 2017 10:54:46 AM EDT 
