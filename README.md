# 1. Force File Download in WordPress via Htaccess

Add a file extension that needs to be downloaded e.g png/mp4

  > <filesmatch “.(mov|mp3|jpg|pdf)$”>ForceType application/octet-stream Header set Content-Disposition attachment </filesMatch>```
  
  ## for pdf
    <FilesMatch "\.(?i:pdf)$">
       ForceType application/octet-stream
       Header set Content-Disposition attachment
     </FilesMatch>
     
  # Current Year In Avia
      function avia_year_func( $atts ){
	return date("Y");
      }
    add_shortcode( 'current_year', 'avia_year_func' );
