# 1. Force File Download in WordPress via Htaccess

Add a file extension that needs to be downloaded e.g png/mp4

	<filesmatch “.(mov|mp3|jpg|pdf)$”>
	ForceType application/octet-stream Header set Content-Disposition attachment 
	</filesMatch>
  
  ### 1.1 force download for pdf only
    <FilesMatch "\.(?i:pdf)$">
       ForceType application/octet-stream
       Header set Content-Disposition attachment
     </FilesMatch>
     
  # 2. Current Year In Avia[Enfold]
    function avia_year_func( $atts ){
	return date("Y");
      }
    add_shortcode( 'current_year', 'avia_year_func' );
  creating a shortcode for dynamic year  
  Then use shortcode *[current_year]* for preview
  
  # 3. Bulk delete spam comments/ comment
    DELETE FROM wp_comments WHERE comment_approved = '0';
    '0' - unapproved
    '1' - approved
    'spam' - spamm folder
Instructions:
1. from phpmyadmin
2. select  infected  database 
3. find *wp_comments* table to equivalent
4. select SQL tab
5. paste command and edit it according
