# ci_multiple_app
CodeIgnitor Distribution to setup multiple application with frontend and backend support
Set up virtual host setting as :

# Configuration
### awisoft.net/admin cannot be Accessed
```
<VirtualHost *:80>
    ##ServerAdmin webmaster@dummy-host2.example.com
    DocumentRoot "C:\xampp\htdocs\frameworks\CodeIgnitor\project-1"
    ServerName awisoft.net
	<Directory C:\xampp\htdocs\frameworks\CodeIgnitor\project-1\admin>
		Order deny,allow
		Deny from all
	</Directory>
</VirtualHost>
```
### admin.awisoft.net/admin can be accessed
```
<VirtualHost *:80>
    ##ServerAdmin webmaster@dummy-host2.example.com
    DocumentRoot "C:\xampp\htdocs\frameworks\CodeIgnitor\project-1\admin"
    ServerName admin.awisoft.net
</VirtualHost>
```
### admin.awisoft.net/ default can be accessed via port 80
```
<VirtualHost *:80>
    ##ServerAdmin webmaster@dummy-host2.example.com
    DocumentRoot "C:\xampp\htdocs"
    ServerName localhost
</VirtualHost>
```

