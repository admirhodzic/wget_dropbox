# wget_dropbox
this is how to upload a file to dropbox using only wget command tool

wget --header="Authorization: Bearer your_access_token" 
https://content.dropboxapi.com/2/files/upload 
--header "Content-Type: application/octet-stream" 
--post-file=c:\myfile.txt 
--no-check-certificate 
--header "Dropbox-API-Arg: {\"path\": \"/myfile.txt\",\"mode\": \"add\",\"autorename\": true,\"mute\": false}"

