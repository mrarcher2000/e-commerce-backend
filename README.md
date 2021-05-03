# E-Commerce Back End
![GitHub license](https://img.shields.io/badge/license-MIT-green)

## Table of Contents

* [Description](#description)
* [Installation](#installation)
* [Usage](#usage)
* [Contributing](#contributing)
* [Questions](#questions)
* [License](#license)

## Description

This is a simple, but extremely helpful setup for the back-end workings of an E-Commerce website. It creates a server and database for your website to help store useful information about products, product categories, and even tags to help create a dynamic and easy to use API for your online store! You can create, update, review, and delete different products, categories, and tags so that the only part you have to worry about is the front-end layout and HTML!

## Installation

To install the project you must have Node.js and MySQL already installed onto your computer. 

For instructions on how to install Node, go to https://nodejs.org/. 

For instructions on how to install MySQL, go to https://www.mysql.com/.

Once you have these installed onto your computer, clone the GitHub Repository into your preffered folder for keeping the files. Open up the folders and create a new file called '.env' . In the .env file, type in your MySQL username and password in the following format:

```
DB_NAME='ecommerce_db'
DB_USER='your MySQL Username'
DB_PW='your MySQL Password'
``` 

Now your database can sync to the server we are about to set up! 

In the command line, navigate to the root directory of the project and type 'mysql -u root -p' and enter your MySQL password. You should see a success message and the version of MySQL that is installed onto your computer. From here, type 'SOURCE schema.sql;' to create the ecommerce database onto your computer. Type 'quit' to exit the MySQL terminal and then type 'npm run seed' to link the already existing Products, Categories, and Tags into the database. Now your database is fully set up and you are ready to start up the server!

## Usage

To start up the server for your E-Commerce website, open the root directory in your command line and type 'node server.js'. You should see some MySQL messages and finally a success message saying "App Listening on Port {PORT}!" This means your installation and start up was successful! The video below shows more about how to set up the server and make requests, but the api methods are as follows:

Create a product: /api/products (the body must contain the product_name, price, stock, and tagIds in JSON format) 

Review products: GET /api/products/:id (the id parameter is optional and will choose a specific product with that ID number) 

Update products PUT /api/products:id (ID parameter here is not optional) 

Delete a product DELETE /api/products/:id 

Create a Category POST /api/category (request body must include category_name) 

Review Categories GET /api/categories/:id (The ID is optional. Removing it will return all products) 

Update Category PUT /api/categories/:id (ID is not optional and the request body must include category_name) 

Delete Category DELETE /api/categories/:id 

Create a new tag POST /api/tags (request body must include the tag_name) 

Review Tags GET /api/tags/:id (ID is optional and will return a single tag with that ID number) 

Update Tags PUT /api/tags/:id (request body must include tag_name) 

Delete a tag DELETE /api/tags/:id 

These requests can be made from your application or from an API testing application like Insomnia Core. A quick walkthrough on how to run the server and make requests can be found at https://drive.google.com/file/d/1zomnIty3okyI9rlF-gXwpNkIqXc7U2lm/view. 

## Contributing

Contributions are very much welcome! To contribute to this project, send an email to me at the email found in the Questions section if you would like to further develop this project or for any other future collaborations and works. This back-end is great for creating API requests on your website, but much work is necessary still before the website is fully functional.

## Questions

For any additional questions or comments, please email the author of this project at: 
archernich@gmail.com.

*OR*

You can view other repositories made by me at https://github.com/mrarcher2000.



## License
    
This project is licensed under the Open Source MIT License.
A full overview of what this license covers can be found at https://spdx.org/licenses/MIT.html.
    
