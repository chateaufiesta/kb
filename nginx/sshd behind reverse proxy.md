# cat ssh.conf
```
stream {
	upstream ssh {
		server 127.0.0.1:22;
	}

	server {
		listen 80;
		listen [::]:80;
		proxy_pass ssh;
	}
}
```
