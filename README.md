# CI4 Unit Testing Activity

A simple CodeIgniter 4 project demonstrating unit testing and debugging using PHPUnit.

---

## Project Overview

This project was created as part of a Week 14 activity focused on Unit Testing and Debugging in CodeIgniter 4.

The activity demonstrates how to:

* Create test cases using PHPUnit
* Verify HTTP responses
* Use assertions for validation
* Understand basic debugging techniques

---

## Technologies Used

* PHP
* CodeIgniter 4
* PHPUnit
* Composer
* XAMPP

---

## Project Structure

```plaintext
test_drive_lab/
│
├── app/
│ └── Controllers/
│ └── Home.php
│
├── tests/
│ └── app/
│ └── Controllers/
│ └── HomeTest.php ← TEST FILE
│
├── vendor/
├── phpunit.dist.xml
└── composer.json
```

---

## Sample Test Case

```php
<?php

namespace Tests\App\Controllers;

use CodeIgniter\Test\FeatureTestTrait;
use CodeIgniter\Test\CIUnitTestCase;

class HomeTest extends CIUnitTestCase
{
    use FeatureTestTrait;

    public function testHomePage()
    {
        $result = $this->get('/');

        $result->assertStatus(200);
    }
}
```

---

## How to Run the Project

### Start the Development Server

```bash
php spark serve
```

Open in browser:

```plaintext
http://localhost:8080
```

---

## How to Run Tests

Run all tests:

```bash
vendor\bin\phpunit
```

Run specific test file:

```bash
vendor\bin\phpunit tests/app/Controllers/HomeTest.php
```

Run with readable output:

```bash
vendor\bin\phpunit --testdox
```

---


## Expected Output

```plaintext
OK (1 test, 1 assertion)
```

---

## Author

April Nicole Custorio
3.2 BSIT
