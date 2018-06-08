## 使用 Nginx + PHP7.0 + sqlite 搭建服务器

    sudo apt-get install nginx
    sudo apt-get install php7.0-fpm php7.0-cli php7.0-curl php7.0-gd php7.0-mcrypt php7.0-cgi
    sudo /etc/init.d/nginx start
    sudo service php7.0-fpm restart

    // 修改 nginx 文件配置
    sudo nano /etc/nginx/sites-available/default
    location / {
    index  index.html index.htm index.php default.html default.htm default.php;
    }

    location ~\.php$ {
    fastcgi_pass unix:/run/php/php7.0-fpm.sock;
    #fastcgi_pass 127.0.0.1:9000;
    fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
    include fastcgi_params;
    }

    sudo service nginx restart

    // sudo apt-get install php7.0-sqlite
