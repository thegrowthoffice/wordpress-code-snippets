# 1. Force File Download in WordPress via Htaccess
Instructions:
 1. The snippet below is added to Htaccess file via cpanel (file manager)
 2. Heads up!! Don't forget to back up htaccesss file before editing
Add a file extension that needs to be downloaded e.g png/mp4
  ### 1.1 force download for any file
     <filesmatch “.(mov|mp3|jpg|pdf)$”>
     ForceType application/octet-stream Header set Content-Disposition attachment 
     </filesMatch>
  
  ### 1.2 force download for pdf only
    <FilesMatch "\.(?i:pdf)$">
       ForceType application/octet-stream
       Header set Content-Disposition attachment
     </FilesMatch>
     
  # 2. Current Year In Avia[Enfold]
    function avia_year_func( $atts ){
	return date("Y");
      }
    add_shortcode( 'current_year', 'avia_year_func' );
  Instructions:
  1. add the fuction above in child theme functions file
  This creats a shortcode for dynamic year  
  2. Then use shortcode *[current_year]* for preview anywhere in text editor
  
  # 3. Bulk delete spam comments/ comment
    DELETE FROM wp_comments WHERE comment_approved = '0';
    where:
    '0' - unapproved
    '1' - approved
    'spam' - spamm folder
Instructions:
1. from phpmyadmin
2. select  infected  database 
3. find *wp_comments* table to equivalent
4. select SQL tab
5. paste command and edit it according
