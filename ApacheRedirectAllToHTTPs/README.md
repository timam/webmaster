<VirtualHost _default_:80>
ServerName www.example.com

ServerSignature Off

RewriteEngine On
RewriteRule ^ https://%{SERVER_NAME}%{REQUEST_URI} [END,NE,R=permanent]

ErrorLog /var/log/httpd/redirect.error.log
LogLevel warn
</VirtualHost>
