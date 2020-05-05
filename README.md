# magento2-migration-tar-command-with-exclusion
Magento 2 - List of exclusion paramters for tar command. Command with directories to exclude when tarballing a site for migration

# Exclusion List

List of exclusion paramters for tar command. Focus put on 
image cache directories, tmp files, log files, and generated 
source files. 

- --exclude="./pub/media/\*/\*/cache"
- --exclude="./pub/media/js"
- --exclude="./pub/media/tmp"
- --exclude="./pub/media/wysiwyg/.thumbs"
- --exclude="./pub/static"
- --exclude="./var/cache"
- --exclude="./var/di"
- --exclude="./var/generation"
- --exclude="./var/log"
- --exclude="./var/page_cache"
- --exclude="./var/report"
- --exclude="./var/view_preprocessed"

# Tar Magento 2 completely excluding unnesessary files

tar -cvf sitebackup-`date +%Y%m%d`.tar --exclude="./pub/media/*/*/cache" --exclude="./pub/media/js" --exclude="./pub/media/tmp" --exclude="./pub/media/wysiwyg/.thumbs" --exclude="./pub/static" --exclude="./var/cache" --exclude="./var/di" --exclude="./var/generation" --exclude="./var/log" --exclude="./var/page_cache" --exclude="./var/report" --exclude="./var/view_preprocessed" .


# Tar Magento Media directory excluding cache files

tar -cvf media-`date +%Y%m%d`.tar --exclude-vcs --exclude='*.htaccess' --exclude='*/cache/*' --exclude='*/cache' --exclude='*/.thumbs/*' --exclude='*/.thumbs' --exclude='*/tmp/*' --exclude='*/tmp' --exclude='*/js/*' --exclude='*/js' --exclude='*/css/*' --exclude='*/css' --exclude='*/captcha/*' --exclude='*/captcha' --exclude='*/css_secure/*' --exclude='*/css_secure' --exclude='*/customer/*' --exclude='*/customer' --exclude='*/dhl/*' --exclude='*/dhl' --exclude='*/downloadable/*' --exclude='*/downloadable' --exclude='*/xmlconnect/*' --exclude='*/xmlconnect' media
