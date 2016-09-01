# wget_dropbox
this is how to upload a file to dropbox using only wget command tool

```
wget --header="Authorization: Bearer your_access_token" 
https://content.dropboxapi.com/2/files/upload 
--header "Content-Type: application/octet-stream" 
--post-file=c:\myfile.txt 
--no-check-certificate 
--header "Dropbox-API-Arg: {\"path\": \"/myfile.txt\",\"mode\": \"add\",\"autorename\": true,\"mute\": false}"
```
download:
```
wget https://content.dropboxapi.com/2/files/download 
  --header "Authorization: Bearer your_access_token" 
  --header "Dropbox-API-Arg: {\"path\": \"/myfile.txt\"}" 
  --no-check-certificate
```
"myfile.txt" is your file name.

Just replace "your_access_token" with access token string for your app generated at 
https://www.dropbox.com/developers/apps
