# 1. Force File Download in WordPress via Htaccess

Add a file extension that needs to be downloaded e.g png/mp4

  ```<filesmatch “.(mov|mp3|jpg|pdf)$”>ForceType application/octet-stream Header set Content-Disposition attachment </filesMatch>```
  
  ## for pdf
    <FilesMatch "\.(?i:pdf)$">
       ForceType application/octet-stream
       Header set Content-Disposition attachment
     </FilesMatch>
