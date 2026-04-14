─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl status apache2
○ apache2.service - The Apache HTTP Server
     Loaded: loaded (/lib/systemd/system/apache2.service; enabled; preset: disabled)
     Active: inactive (dead) since Tue 2026-04-14 12:11:40 GMT; 10min ago
   Duration: 7min 15.654s
       Docs: https://httpd.apache.org/docs/2.4/
   Main PID: 2982 (code=exited, status=0/SUCCESS)
        CPU: 322ms

Apr 14 12:04:24 parrot systemd[1]: Starting apache2.service - The Apache HTTP Server...
Apr 14 12:04:24 parrot apachectl[2981]: AH00558: apache2: Could not reliably determine the server's fully qualified domain na>
Apr 14 12:04:24 parrot systemd[1]: Started apache2.service - The Apache HTTP Server.
Apr 14 12:11:40 parrot systemd[1]: Stopping apache2.service - The Apache HTTP Server...
Apr 14 12:11:40 parrot apachectl[3468]: AH00558: apache2: Could not reliably determine the server's fully qualified domain na>
Apr 14 12:11:40 parrot systemd[1]: apache2.service: Deactivated successfully.
Apr 14 12:11:40 parrot systemd[1]: Stopped apache2.service - The Apache HTTP Server.
┌─[✗]─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl disable apache2
Synchronizing state of apache2.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install disable apache2
Use of uninitialized value $service in hash element at /usr/sbin/update-rc.d line 26, <DATA> line 44.
Use of uninitialized value $service in hash element at /usr/sbin/update-rc.d line 26, <DATA> line 44.
insserv: warning: current start runlevel(s) (empty) of script `apache2' overrides LSB defaults (2 3 4 5).
insserv: warning: current stop runlevel(s) (0 1 2 3 4 5 6) of script `apache2' overrides LSB defaults (0 1 6).
Removed "/etc/systemd/system/multi-user.target.wants/apache2.service".
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl status apache2
○ apache2.service - The Apache HTTP Server
     Loaded: loaded (/lib/systemd/system/apache2.service; disabled; preset: disabled)
     Active: inactive (dead)
       Docs: https://httpd.apache.org/docs/2.4/

Apr 14 12:04:24 parrot systemd[1]: Starting apache2.service - The Apache HTTP Server...
Apr 14 12:04:24 parrot apachectl[2981]: AH00558: apache2: Could not reliably determine the server's fully qualified domain na>
Apr 14 12:04:24 parrot systemd[1]: Started apache2.service - The Apache HTTP Server.
Apr 14 12:11:40 parrot systemd[1]: Stopping apache2.service - The Apache HTTP Server...
Apr 14 12:11:40 parrot apachectl[3468]: AH00558: apache2: Could not reliably determine the server's fully qualified domain na>
Apr 14 12:11:40 parrot systemd[1]: apache2.service: Deactivated successfully.
Apr 14 12:11:40 parrot systemd[1]: Stopped apache2.service - The Apache HTTP Server.
┌─[✗]─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl enable nginx
Synchronizing state of nginx.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install enable nginx
Use of uninitialized value $service in hash element at /usr/sbin/update-rc.d line 26, <DATA> line 44.
Use of uninitialized value $service in hash element at /usr/sbin/update-rc.d line 26, <DATA> line 44.
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl disable nginx
Synchronizing state of nginx.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install disable nginx
Use of uninitialized value $service in hash element at /usr/sbin/update-rc.d line 26, <DATA> line 44.
Use of uninitialized value $service in hash element at /usr/sbin/update-rc.d line 26, <DATA> line 44.
insserv: warning: current start runlevel(s) (empty) of script `nginx' overrides LSB defaults (2 3 4 5).
insserv: warning: current stop runlevel(s) (0 1 2 3 4 5 6) of script `nginx' overrides LSB defaults (0 1 6).
Removed "/etc/systemd/system/multi-user.target.wants/nginx.service".
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl kill nginx -v
systemctl: invalid option -- 'v'
┌─[✗]─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl kill nginx
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl stop nginx
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl start nginx
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl enable nginx
Synchronizing state of nginx.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install enable nginx
Use of uninitialized value $service in hash element at /usr/sbin/update-rc.d line 26, <DATA> line 44.
insserv: warning: current start runlevel(s) (empty) of script `nginx' overrides LSB defaults (2 3 4 5).
insserv: warning: current stop runlevel(s) (0 1 2 3 4 5 6) of script `nginx' overrides LSB defaults (0 1 6).
Use of uninitialized value $service in hash element at /usr/sbin/update-rc.d line 26, <DATA> line 44.
Created symlink /etc/systemd/system/multi-user.target.wants/nginx.service → /lib/systemd/system/nginx.service.
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl disable nginx
Synchronizing state of nginx.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install disable nginx
Use of uninitialized value $service in hash element at /usr/sbin/update-rc.d line 26, <DATA> line 44.
Use of uninitialized value $service in hash element at /usr/sbin/update-rc.d line 26, <DATA> line 44.
insserv: warning: current start runlevel(s) (empty) of script `nginx' overrides LSB defaults (2 3 4 5).
insserv: warning: current stop runlevel(s) (0 1 2 3 4 5 6) of script `nginx' overrides LSB defaults (0 1 6).
Removed "/etc/systemd/system/multi-user.target.wants/nginx.service".
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl stop nginx
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl kill nginx
Failed to kill unit nginx.service: Unit nginx.service not loaded.
┌─[✗]─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl start nginx
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl status nginx
● nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/lib/systemd/system/nginx.service; disabled; preset: disabled)
     Active: active (running) since Tue 2026-04-14 12:25:41 GMT; 14s ago
       Docs: man:nginx(8)
    Process: 5300 ExecStartPre=/usr/sbin/nginx -t -q -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
    Process: 5301 ExecStart=/usr/sbin/nginx -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
   Main PID: 5303 (nginx)
      Tasks: 5 (limit: 4578)
     Memory: 3.3M
        CPU: 28ms
     CGroup: /system.slice/nginx.service
             ├─5303 "nginx: master process /usr/sbin/nginx -g daemon on; master_process on;"
             ├─5304 "nginx: worker process"
             ├─5305 "nginx: worker process"
             ├─5306 "nginx: worker process"
             └─5307 "nginx: worker process"

Apr 14 12:25:41 parrot systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Apr 14 12:25:41 parrot systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl kill nginx
┌─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl status apache2
○ apache2.service - The Apache HTTP Server
     Loaded: loaded (/lib/systemd/system/apache2.service; disabled; preset: disabled)
     Active: inactive (dead)
       Docs: https://httpd.apache.org/docs/2.4/

Apr 14 12:04:24 parrot systemd[1]: Starting apache2.service - The Apache HTTP Server...
Apr 14 12:04:24 parrot apachectl[2981]: AH00558: apache2: Could not reliably determine the server's fully qualified domain na>
Apr 14 12:04:24 parrot systemd[1]: Started apache2.service - The Apache HTTP Server.
Apr 14 12:11:40 parrot systemd[1]: Stopping apache2.service - The Apache HTTP Server...
Apr 14 12:11:40 parrot apachectl[3468]: AH00558: apache2: Could not reliably determine the server's fully qualified domain na>
Apr 14 12:11:40 parrot systemd[1]: apache2.service: Deactivated successfully.
Apr 14 12:11:40 parrot systemd[1]: Stopped apache2.service - The Apache HTTP Server.
┌─[✗]─[user@parrot]─[/var/www/html]
└──╼ $sudo systemctl start nginx
┌─[user@parrot]─[/var/www/html]
└──╼ $^C
┌─[✗]─[user@parrot]─[/var/www/html]
└──╼ $^C
┌─[✗]─[user@parrot]─[/var/www/html]
└──╼ $
