# PHP Require (Include)

## If you are using Codespaces <a name="codespaces"></a>

- Open your existing codespace (DON'T CREATE A NEW ONE) [https://github.com/codespaces](https://github.com/codespaces).
- In the terminal enter

```
git clone https://github.com/CIT2202/using-require
```

This will copy the contents of this repository into your codespace.

- Open _connect.php_. Change the connection settings to match your database and environment. This is the line you need to change

```
    $conn = new PDO('mysql:host=localhost;dbname=MyDatabase', 'MyUsername', 'MyPassword');
```

You will need to change it to:

```
    $conn = new PDO('mysql:host=db;dbname=cht2520', 'root', 'secret');
```

- Start Apache (`apache2ctl start`)

Now move onto [Completing the practical work](#practical)

## If you are using XAMPP <a name="xampp"></a>

Now move onto [Completing the practical work](#practical).

## Completing the practical work <a name="practical"></a>

PHP provides a number of statements that allow us to insert other files in our PHP pages. This provides a simple way to remove duplicate code in our applications.

- Open _require-demo.php_ in a browser.
- Look at the source code for both _require-demo.php_ and _message.html_.
- Note how _require-demo.php_ displays content from _message.html_ using the line:

```php
require "message.html";
```

Here are a couple of things about including files:

- We can include _html_ and _php_ files.
- There are several different statements that can be used to include content from different files:
  - _include_
  - _include_once_
  - _require_
  - _require_once_
  - At the moment it doesn't really matter which one we use. See the following link for a discussion of the differences https://stackoverflow.com/questions/2418473/difference-between-require-include-and-require-once

## Using `require`

- In a browser open the 'All About Huddersfield' website. It is a very simple PHP website.
- Re-structure the website to use the PHP require statement.
  - Start with the _index.php_ page.
  - Think which parts of the HTML are duplicated in different pages.
  - Create separate include files e.g. header.php, footer.php.
  - Use these included files in index.php e.g.
    ```php
       require "header.php";
    ```
  - Test this works
- Modify the other pages in the site to also use `require`.
- Add another page to the site e.g. a page about the University.
  - Make sure you build this page by using the `require` statement.
- Modify the navigation bar so that it also features a link to the University page you have just created. You should find that changing one file updates the entire site.
- One problem with the above is that every single page has the same page title. How can you modify your site so that each page has a unique title while still using an included header.
