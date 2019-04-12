# Yo Uganda Phone Validator PHP

Yo Uganda Phone Validator is a PHP library that can be included in your PHP project to determine whether a phone number is valid and to which Ugandan telephone network it belongs.

## Getting Started

### Installing

Copy the YoPhoneValidator.php file into one of the ```include_path``` directories specified in your PHP project.

If you don't use git, click the 'zip' button at the top of the page in GitHub.

## A Simple Example

Validate a phone number

```
require '/path/to/YoPhoneValidator.php';

$phone_number = '0712345678';
YoPhoneValidator::validate($phone_number); 
print_r($phone_number); // Prints true or false
```
Get Internationally Formatted Phone number

```
require '/path/to/YoPhoneValidator.php';

$phone_number = '0712345678';
$phone_validator = new YoPhoneValidator($phone_number);
$formatted_phone_number = $phone_validator->get(true);
print_r($formatted_phone_number); // Prints 256712345678
$unformatted_phone_number = $phone_validator->get(false);
print_r($unformatted_phone_number); // Prints 0712345678
```

Get Phone Network

```
require '/path/to/YoPhoneValidator.php';

$phone_number = '0712345678';
$phone_validator = new YoPhoneValidator($phone_number);
$phone_network = $phone_validator->getOperator();
print_r($phone_network); // Prints MTN, Airtel, UTL, AFRICELL
```

That's it! You should now be ready to use YoPhoneValidator

## Built With

* [PHP](http://www.php.net/) - PHP Programming Language 

## Authors

* **Aziz Kirumira** - *Initial work* - [Yo (U) Ltd](https://github.com/YO-Uganda)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Gerald Begumisa
* Ronald Sebuhinja
