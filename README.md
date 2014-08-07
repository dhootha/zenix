Zenix
=====

Fast and ultra-compact web server with Lua scripting based on Nginx.

Why Zenix and not just Nginx or Openresty? Because:

Zenix has a smaller memory footprint, ideal for memory-conscious environments, especially when coupled with Redis.

Zenix is smaller than Openresty, even with LuaJIT included (8MB and 1.7MB compressed).

I don't know man I'm tired.. I'll get back to write something more.

How to install
==============

Untar if necessary. Cd to the folder and type **./install** in your command line, then enter.

This will install LuaJIT and Zenix on /usr/local/zenix.

You will also get a nice command line control script.

Access it by typing **/etc/init.d/zenix** in your command line. You'll given many options such as: *status*,*start*,*restart*,*stop*,*start-reload*.

The last one is meant for auto-reloading functionality, currently working on $HOME/jembaz folder. You may change that in the script easily.

Look **zenix_info** to see what was changed.
