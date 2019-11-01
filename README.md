REST API example project.

Please modify config/database.php and create database and tables using config/database_def.sql file.

Usage:

Read all available products:
http://localhost/api/product/read.php

Create product:
http://localhost/api/product/create.php
    POST message:
        {
            "name" : "Amazing Pillow 2.0",
            "price" : "199",
            "description" : "The best pillow for amazing programmers.",
            "category_id" : 2,
            "created" : "2018-06-01 00:35:07"
        }
        
Read one product by id:
http://localhost/api/product/read_one.php?id=60

Update specific product:
http://localhost/api/product/update.php
    POST message:
        {
            "id" : "106",
            "name" : "Amazing Pillow 3.0",
            "price" : "255",
            "description" : "The best pillow for amazing programmers.",
            "category_id" : 2,
            "created" : "2018-08-01 00:35:07"
        }

Delete product by id:
http://localhost/api/product/delete.php
    POST message
        {
            "id" : "106"
        }

Search in description or name:
http://localhost/api/product/search.php?s=shirt

Read all products with pagination:
http://localhost/api/product/read_paging.php