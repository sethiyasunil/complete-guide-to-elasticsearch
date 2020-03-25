create ecommerce index

 curl -H "Content-Type: application/x-ndjson" -XPOST 'http://localhost:9200/ecommerce/product/_bulk' --data-binary "@legacy-products.json"
 
 install php https://windows.php.net/download/
 install composer https://getcomposer.org/Composer-Setup.exe
 run larvel 
	composer global require "laravel/installer=~1.1"
 install dependencies
	composer install
	
 
