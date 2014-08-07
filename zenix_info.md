###############################################
## Zenix features and changed functionality: ##
###############################################

    **get** -> to define a route **get** is used instead of **location**

    **no check on accept_mutex** -> removed accept_mutex check (except for the worker_processes value check) and option to set it off - there's no need to. It is automatically disabled in the case where *worker_processes < 2* or in a simple way that you set more than a worker process in zenix.conf (there is no sense in having accept_mutex enabled for a single worker).
    
    
    
    
    




##############################################
## Zenix removed functionality and modules: ##
##############################################

*The following removed functionality and modules can be fully or partially replicated with the builting Lua(JIT) scripting if needed or are better accomplished in other ways*


	**satisfy**
	**auth_basic**
	**auth_request**
	**msie_padding**
	**msie_refresh**
	**alias** (can be replicated with the *root* directive if needed)
     ----------------------  
	| location /static/ {  | *requested* -> /static/nonce.png
	|   root /dt/files;    | 
	| }				       | *served from* -> /dt/files/nonce.png
     ----------------------
		    
    **internal**
    **max_ranges**
    **optimize_server_names** (which is also deprecated)
    **postpone_output**
    **ngx_threads (it was never intended to be a threaded web server and it's still experimental)**
    **auto_index**
	**limit_except (including ngx_method_names)**
	**limit_rate (thus "X-Accel-Limit-Rate")**
	**limit_rate_after**
