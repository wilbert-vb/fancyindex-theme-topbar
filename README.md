# fancyindex-theme-topbar
Add the following location to your Nginx server config:
```
location / {
	fancyindex on ;
	fancyindex_exact_size off ;
	fancyindex_localtime on ;
	fancyindex_default_sort name ;
	fancyindex_directories_first on ;
	fancyindex_footer /theme/footer.html ;
	fancyindex_header /theme/header.html ;
	fancyindex_hide_parent_dir on ;
	fancyindex_ignore favicon.ico scripts styles ;
	fancyindex_show_path off ;
	fancyindex_time_format "%b %d %Y" ;
	}
	
location /theme {
	alias /${YOURPATH}/fancyindex-topbar ;
	}
}
```
