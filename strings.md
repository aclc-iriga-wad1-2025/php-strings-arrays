# String Length & Counting

## `strlen()`
- **returns the length of a string**

### strlen() parameters
| **Parameter** | **Description**                             |
|---------------|---------------------------------------------|
| _**string**_  | **Required**. Specifies the string to check |

### `strlen() return value`
Number of characters in the string

### `strlen() example #1`
```php
$str1 = "Computer Science";
$val  = strlen($str1);

// RESULT:
// $val1 = 16
```

### `strlen() example #2`
```php
$str1 = "";
$val  = strlen($str1);

// RESULT:
// $val1 = 0
```

---

## `str_word_count()`
- counts the number of words in a string.

### `str_word_count() parameters`

| **Parameter** | **Description**                                                                                                                                                                                                                                                                                                                                |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| _**string**_  | **Required**. Specifies the string to check                                                                                                                                                                                                                                                                                                    |
| _**return**_  | **Optional**. Specifies the return value of the str_word_count() function.<br/><br/>Possible values:<br/>**0** - **Default**. Returns the number of words found<br/>**1** - Returns an array with the words from the string<br/>**2** - Returns an array where the key is the position of the word in the string, and value is the actual word |
| _**char**_    | **Optional**. Specifies special characters to be considered as words.                                                                                                                                                                                                                                                                          |

### `str_word_count() return value`
Number or Array, depending on the chosen return parameter

### `str_word_count() example #1`
```php
$str1 = "Hello world!";
$val  = str_word_count($str1);

// RESULT:
// $val = 2
```

### `str_word_count() example #2`
```php
$str1 = "Hello there world";
$val  = str_word_count($str1, 1);

// RESULT:
// $val = ["Hello", "there", "world"]
```

---

# Changing Case

## `strtolower()`
- **converts a string to lowercase**

### `strtolower() parameters`
| **Parameter** | **Description**                               |
|---------------|-----------------------------------------------|
| _**string**_  | **Required**. Specifies the string to convert |

### `strtolower() return value`
String in lowercase

### `strtolower() example #1`
```php
$str1 = "Hello WORLD";
$str2 = strtolower($str1);

// RESULT:
// $str2 = "hello world"
```

### `strtolower() example #2`
```php
$str1 = "#1, ZONE 2";
$str2 = strtolower($str1);

// RESULT:
// $str2 = "#1, zone 2"
```

---

## `strtoupper()`
- converts a string to uppercase

### `strtoupper() parameters`

| **Parameter** | **Description**                               |
|---------------|-----------------------------------------------|
| _**string**_  | **Required**. Specifies the string to convert |

### `strtoupper() return value`
String in uppercase

### `strtoupper() example #1`
```php
$str1 = "Hello World";
$str2 = strtoupper($str1);

// RESULT:
// $str2 = "HELLO WORLD"
```

### `strtoupper() example #2`
```php
$str1 = "#1, zone 2";
$str2 = strtoupper($str1);

// RESULT:
// $str2 = "#1, ZONE 2"
```

---

## `lcfirst()`
- **converts the first character of a string to lowercase**

### `lcfirst() parameters`
| **Parameter** | **Description**                               |
|---------------|-----------------------------------------------|
| _**string**_  | **Required**. Specifies the string to convert |

### `lcfirst() return value`
Converted string

### `lcfirst() example #1`
```php
$str1 = "Hello World!";
$str2 = lcfirst($str1);

// RESULT:
// $str2 = "hello World!"
```

### `lcfirst() example #2`
```php
$str1 = "#1, Zone 2";
$str2 = lcfirst($str1);

// RESULT (Unchanged when first character is not a letter):
// $str2 = "#1, Zone 2";
```

---

## `ucfirst()`
- **converts the first character of a string to uppercase**

### `ucfirst() parameters`
| **Parameter** | **Description**                               |
|---------------|-----------------------------------------------|
| _**string**_  | **Required**. Specifies the string to convert |

### `ucfirst() return value`
Converted string

### `ucfirst() example #1`
```php
$str1 = "hello World!";
$str2 = ucfirst($str1);

// RESULT:
// $str2 = "Hello World!"
```

### `ucfirst() example #2`
```php
$str1 = "#1, Zone 2";
$str2 = ucfirst($str1);

// RESULT (Unchanged when first character is not a letter):
// str2 = "#1, Zone 2"
```

---

## `ucwords()`
- **converts the first character of each word in a string to uppercase**

### `ucwords() parameters`
| **Parameter**    | **Description**                                      |
|------------------|------------------------------------------------------|
| _**string**_     | **Required**. Specifies the string to convert        |
| _**delimiters**_ | **Optional**. Specifies the word separator character |

### `ucwords() return value`
Converted string

### `ucwords() example #1`
```php
$str1 = "hello world";
$str2 = ucwords($str1);

// RESULT:
// $str2 = "Hello World"
```

### `ucwords() example #2`
```php
$str1 = "php-string-manipulation";
$str2 = ucwords($str1, "-");

// RESULT:
// $str2 = "Php-String-Manipulation"
```

---

# Trimming & Padding

## `ltrim()`
- **removes whitespace or other predefined characters from the left side of a string**

### `ltrim() parameters`
| **Parameter**  | **Description**                                                    |
|----------------|--------------------------------------------------------------------|
| _**string**_   | **Required**. Specifies the string to check                        |
| _**charlist**_ | **Optional**. Specifies which characters to remove from the string |

### `ltrim() return value`
Modified string

### `ltrim() example #1`
```php
$str1 = "   John Doe";
$str2 = ltrim($str1);

// RESULT:
// $str2 = "John Doe"
```

### `ltrim() example #2`
```php
$str1 = ":::|:Greetings!";
$str2 = ltrim($str1, ":");

// RESULT:
// $str2 = "|:Greetings!"
```

---

## `rtrim()`
- **removes whitespace or other predefined characters from the right side of a string**

### `rtrim() parameters`
| **Parameter**  | **Description**                                                     |
|----------------|---------------------------------------------------------------------|
| _**string**_   | **Required**. Specifies the string to check                         |
| _**charlist**_ | **Optional**. Specifies which characters to remove from the string  |

### `rtrim() return value`
Modified string

### `rtrim() example #1`
```php
$str1 = "John Doe   ";
$str2 = rtrim($str1);

// RESULT:
// $str2 = "John Doe"
```

### `rtrim() example #2`
```php
$str1 = "Greetings!~~~";
$str2 = rtrim($str1, "~");

// RESULT:
// $str2 = "Greetings!"
```

---

## `trim()`
- **removes whitespace and other predefined characters from both sides of a string**

### `trim() parameters`
| **Parameter**  | **Description**                                                     |
|----------------|---------------------------------------------------------------------|
| _**string**_   | **Required**. Specifies the string to check                         |
| _**charlist**_ | **Optional**. Specifies which characters to remove from the string  |

### `trim() return value`
Modified string

### `trim() example #1`
```php
$str1 = " Jane Doe   ";
$str2 = trim($str1);

// RESULT:
// $str2 = "Jane Doe"
```

### `trim() example #2`
```php
$str1 = "::Jane Doe:|::::";
$str2 = trim($str1, ":");

// RESULT:
// $str2 = "Jane Doe:|"
```
---

## `str_pad()`
- **pads a string to a new length**


### `str_pad() parameters`
| **Parameter**    | **Description**                                                                                                                                                                                                                                                                                                                                |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| _**string**_     | **Required**. Specifies the string to pad                                                                                                                                                                                                                                                                                                      |
| _**length**_     | **Required**. Specifies the new string length. If this value is less than the original length of the string, nothing will be done                                                                                                                                                                                                              |
| _**pad_string**_ | **Optional**. Specifies the string to use for padding. **Default is whitespace**                                                                                                                                                                                                                                                               |
| _**pad_type**_   | **Optional**. Specifies what side to pad the string.<br/><br/>Possible values:<br/>**STR_PAD_BOTH** - Pad to both sides of the string. If not an even number, the right side gets the extra padding<br/>**STR_PAD_LEFT** - Pad to the left side of the string<br/>**STR_PAD_RIGHT** - Pad to the right side of the string. **This is default** |


### `str_pad() example #1`
```php
$str1 = "1";
$str2 = str_pad($str1, 5);

// RESULT:
// $str2 = "1    "
```

### `str_pad() example #2`
```php
$str1 = "31";
$str2 = str_pad($str1, 8, "0");

// RESULT:
// $str2 = "31000000"
```

### `str_pad() example #3`
```php
$str1 = "31";
$str2 = str_pad($str1, 8, "0", STR_PAD_LEFT);

// RESULT:
// $str2 = "00000031"
```

---

# Substring & Position

## `substr()`
- **returns a part of a string**

### `substr() parameters`

| **Parameter** | **Description**                                                                                                                                                                                                                                                                                                                                     |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| _**string**_  | **Required**. Specifies the string to return a part of                                                                                                                                                                                                                                                                                              |
| _**start**_   | **Required**. Specifies where to start in the string<br/><br/>**A positive number** - Start at a specified position in the string<br/>**A negative number** - Start at a specified position from the end of the string<br/>**0** - Start at the first character in string                                                                           |
| _**length**_  | **Optional**. Specifies the length of the returned string. Default is to the end of the string.<br/><br/>**A positive number** - The length to be returned from the start parameter<br/>**Negative number** - The length to be returned from the end of the string<br/>**If the length parameter is 0, NULL, or FALSE** - it return an empty string |


### `substr() return value`
Extracted part of a string, or FALSE on failure

### `substr() example #1`
```php
$str1 = "Hello world";
$str2 = substr($str1, 6);

// RESULT:
// $str2 = "world"
```

### `substr() example #2`
```php
$str1 = "Bachelor of Science in Computer Science";
$str2 = substr($str1, 23, 8);

// RESULT:
// $str2 = "Computer"
```

### `substr() example #3`
```php
$str1 = "Bachelor of Science in Computer Science";
$str2 = substr($str1, -16, -8);

// RESULT:
// $str2 = "Computer"
```

---

## `strpos()`
- **finds the position of the first occurrence of a string inside another string**

### `strpos() parameters`
| **Parameter** | **Description**                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| _**string**_  | **Required**. Specifies the string to search                                                                            |
| _**find**_    | **Required**. Specifies the string to find                                                                              |
| _**start**_   | **Optional**. Specifies where to begin the search. If start is a negative number, it counts from the end of the string. |

### `strpos() return value`
The position of the first occurrence of a string inside another string,
or FALSE if the string is not found.


### `strpos() example #1`
```php
$str = "Hello world! Goodbye world!";
$val = strpos($str, 'world');

// RESULT:
// $val = 6
```

### `strpos() example #2`
```php
$str = "Hello world! Goodbye world!";
$val = strpos($str, 'WORLDS');

// RESULT:
// $val = false
```

---

## `stripos()`
- **finds the position of the first occurrence of a string inside another string (case-insensitive)**

### `stripos() parameters`
| **Parameter** | **Description**                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| _**string**_  | **Required**. Specifies the string to search                                                                            |
| _**find**_    | **Required**. Specifies the string to find                                                                              |
| _**start**_   | **Optional**. Specifies where to begin the search. If start is a negative number, it counts from the end of the string. |

### `stripos() return value`
The position of the first occurrence of a string inside another string,
or FALSE if the string is not found.

### `stripos() example #1`
```php
$str = "Goodbye World! Hello World!";
$val = stripos($str, 'world');

// RESULT:
// $val = 8
```

### `stripos() example #2`
```php
$str = "Goodbye World! Hello World!";
$val = stripos($str, 'worldS');

// RESULT:
// $val = false
```

---

## `strstr()`
- **searches for the first occurrence of a string inside another string**

### `strstr() parameters`
| **Parameter**       | **Description**                                                                                                                                                  |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| _**string**_        | **Required**. Specifies the string to search                                                                                                                     |
| _**search**_        | **Required**. Specifies the string to search for. If this parameter is a number, it will search for the character matching the ASCII value of the number         |
| _**before_search**_ | **Optional**. A boolean value whose default is "false". If set to "true", it returns the part of the string before the first occurrence of the search parameter. |

### `strstr() return value`
The rest of the string (from the matching point), or FALSE, if the string to search for is not found.

### `strstr() example #1`
```php
$str1 = "Hello world!";
$str2 = strstr($str1, "world");

// RESULT:
// $str2 = "world!"
```

### `strstr() example #2`
```php
$str1 = "Hello MyWorld!";
$str2 = strstr($str1, "World", true);

// RESULT:
// $str2 = "Hello My"
```

### `strstr() example #3`
```php
$str1 = "Hello MyWorld!";
$str2 = strstr($str1, "world");

// RESULT:
// $str2 = false
```

---

# `stristr()`
- **searches for the first occurrence of a string inside another string (case-insensitive)**

### `stristr() parameters`
| **Parameter**       | **Description**                                                                                                                                                  |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| _**string**_        | **Required**. Specifies the string to search                                                                                                                     |
| _**search**_        | **Required**. Specifies the string to search for. If this parameter is a number, it will search for the character matching the ASCII value of the number         |
| _**before_search**_ | **Optional**. A boolean value whose default is "false". If set to "true", it returns the part of the string before the first occurrence of the search parameter. |

### `stristr() return value`
The rest of the string (from the matching point), or FALSE, if the string to search for is not found.

### `stristr() example #1`
```php
$str1 = "Hello world!";
$str2 = stristr($str1, "WOrLD");

// RESULT:
// $str2 = "world!"
```

### `stristr() example #2`
```php
$str1 = "Hello MyWorld!";
$str2 = stristr($str1, "my", true);

// RESULT:
// $str2 = "Hello "
```

### `stristr() example #3`
```php
$str1 = "Hello MyWorld!";
$str2 = stristr($str1, "worLds");

// RESULT:
// $str2 = false
```

---

## `str_contains()`
- **determines if a string contains a given substring (PHP 8+)**

### `str_contains() parameters`
| **Parameter**  | **Description**                                            |
|----------------|------------------------------------------------------------|
| _**haystack**_ | **Required**. The string to search in.                     |
| _**needle**_   | **Required**. The substring to search for in the haystack. |

### `str_contains() return value`
Boolean: true if needle is in haystack, false otherwise

### `str_contains() example #1`
```php
$str = "Computer Programming";
$val = str_contains($str, "Programming");

// RESULT:
// $val = true
```

### `str_contains() example #2`
```php
$str = "Computer Programming";
$val = str_contains($str, "programming");

// RESULT:
// $val = false
```

---

## `str_starts_with()`
- **checks if a string starts with a given substring (PHP 8+)**

### `str_starts_with() parameters`

| **Parameter**  | **Description**                                            |
|----------------|------------------------------------------------------------|
| _**haystack**_ | **Required**. The string to search in.                     |
| _**needle**_   | **Required**. The substring to search for in the haystack. |

### `str_starts_with() return value`
Boolean: true if haystack begins with needle, false otherwise.

### `str_starts_with() example #1`
```php
$str = "09123456789";
$val = str_starts_with($str, "0912");

// RESULT:
// $val = true
```
### `str_starts_with() example #2`
```php
$str = "Web Development";
$val = str_starts_with($str, "w");

// RESULT:
// $val = false
```

---

## `str_ends_with()`
-  **checks if a string ends with a given substring (PHP 8+)**

### `str_ends_with() parameters`
| **Parameter**  | **Description**                                            |
|----------------|------------------------------------------------------------|
| _**haystack**_ | **Required**. The string to search in.                     |
| _**needle**_   | **Required**. The substring to search for in the haystack. |

### `str_ends_with() return value`
Boolean: true if haystack ends with needle, false otherwise

### `str_ends_with() example #1`
```php
$str = "www.example.com";
$val = str_ends_with($str, ".com");

// RESULT:
// $val = true
```

### `str_ends_with() example #2`
```php
$str = "my.email@example.com";
$val = str_ends_with($str, "@example.net");

// RESULT:
// $val = false
```

---

# Splitting & Joining Strings

## `str_split()`
- **splits a string into an array**

### `str_split() parameters`

| **Parameter** | **Description**                                                            |
|---------------|----------------------------------------------------------------------------|
| _**string**_  | **Required**. Specifies the string to split                                |
| _**length**_  | **Optional**. Specifies the length of each array element. **Default is 1** |

### `str_split() return value`
Array of splitted strings

### `str_split() example #1`
```php
$str1 = "Hello";
$str2 = str_split($str1);

// RESULT:
// $str2 = ["H", "e", "l", "l", "o"]
```

### `str_split() example #2`
```php
$str1 = "09123456789";
$str2 = str_split($str1, 4);

// RESULT:
// $str2 = ["0912", "3456", "789"]
```

---

## `explode()`
- **breaks a string into an array**

### `explode() parameters`
| **Parameter**   | **Description**                                   |
|-----------------|---------------------------------------------------|
| _**separator**_ | **Required.** Specifies where to break the string |
| _**string**_    | **Required.** The string to split                 |

### `explode() return value`
Array of strings

### `explode() example #1`
```php
$str = "Hello world. It's a beautiful day.";
$arr = explode(" ", $str);

// RESULT:
// $arr = ["Hello", "world.", "It's", "a", "beautiful", "day."];
```

### `explode() example #2`
```php
$data = "John|Doe|male|22";
$arr  = explode("|", $data);

// RESULT:
// $arr = ["John", "Doe", "male", "22"]
```

### `explode() example #3`
```php
$data = "John|Doe|male|22";
$arr  = explode("%", $data);

// RESULT (separator not found):
// $arr = ["John|Doe|male|22"]
```

---

## `implode()`
- **returns a string from the elements of an array**

### `implode() parameters`
| **Parameter**   | **Description**                                                                                     |
|-----------------|-----------------------------------------------------------------------------------------------------|
| _**separator**_ | **Optional**. Specifies what to put between the array elements. **Default is "" (an empty string)** |
| _**array**_     | **Required**. The array to join to a string                                                         |

### `implode() return value`
String from elements of an array

### implode() example #1
```php
$arr = ["Hello", "world.", "It's", "a", "beautiful", "day."];
$str = implode(" ", $arr);

// RESULT:
// $str = "Hello world. It's a beautiful day."
```

### `implode() example #2`
```php
$arr  = ["John", "Doe", "male", "22"];
$data = implode("|", $arr);

// RESULT:
// $data = "John|Doe|male|22"
```

### `implode() example #3`
```php
$arr = ["John", "Doe", "male", "22"];
$str = implode($arr);

// RESULT (No separator provided):
// $str = "JohnDoemale22"
```

#### NOTE: The `join()` function is an alias of the `implode()` function. You can use `join()` instead of `implode()`, as it accepts the same parameters and performs the same operation.

---

# Replacing Text

## `str_replace()`
- **replaces some characters with some other characters in a string**

### `str_replace() parameters`
| **Parameter** | **Description**                                                |
|---------------|----------------------------------------------------------------|
| _**find**_    | **Required**. Specifies the value to find                      |
| _**replace**_ | **Required**. Specifies the value to replace the value in find |
| _**string**_  | **Required**. Specifies the string to be searched              |
| _**count**_   | **Required**. Specifies the string to be searched              |

### `str_replace() return value`
String with the replaced values

### `str_replace() example #1`
```php
$str1 = "Hello world!";
$str2 = str_replace("world", "Rodrigo", $str1);

// RESULT:
// $str2 = "Hello Rodrigo!"
```

### `str_replace() example #2`
```php
$str1 = "Bachelor of Arts in Computer Arts";
$str2 = str_replace("Arts", "Science", $str1);

// RESULT:
// $str2 = "Bachelor of Science in Computer Science"
```

---

## `str_ireplace()`
- **replaces some characters with some other characters in a string (case-insensitive)**

### `str_ireplace() parameters`
| **Parameter** | **Description**                                                |
|---------------|----------------------------------------------------------------|
| _**find**_    | **Required**. Specifies the value to find                      |
| _**replace**_ | **Required**. Specifies the value to replace the value in find |
| _**string**_  | **Required**. Specifies the string to be searched              |
| _**count**_   | **Required**. Specifies the string to be searched              |

### `str_replace() return value`
String with the replaced values

### `str_ireplace() example #1`
```php
$str1 = "Hello WoRlD!";
$str2 = str_ireplace("world", "Robin", $str1);

// RESULT:
// $str2 = "Hello Robin!"
```

### `str_ireplace() example #2`
```php
$str1 = "Bachelor of artS in Computer Arts";
$str2 = str_ireplace("Arts", "Science", $str1);

// RESULT:
// $str2 = "Bachelor of Science in Computer Science"
```

---

# Formatting & Reversing

## `number_format()`
-  **formats a number with grouped thousands**

### `number_format() parameters`

| Parameter          | Description                                                                                                                                                            |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| _**number**_       | **Required**. The number to be formatted. If no other parameters are set, the number will be formatted without decimals and with comma (,) as the thousands separator. |
| _**decimals**_     | **Optional**. Specifies how many decimals. If this parameter is set, the number will be formatted with a dot (.) as decimal point                                      |
| _**decimalpoint**_ | **Optional**. Specifies what string to use for decimal point                                                                                                           |
| _**separator**_    | **Optional**. Specifies what string to use for thousands separator. Only the first character of separator is used. For example, "xxx" will give the same output as "x" |


### `number_format() return value`
String (the formatted number)

### `number_format() example #1`
```php
$val = 31104175;
$str = number_format($val);

// RESULT:
// $str = "31,104,175"
```

### `number_format() example #2`
```php
$val = 31104175.808;
$str = number_format($val, 2);

// RESULT:
// $str = "31,104,175.81"
```

### `number_format() example #3`
```php
$val = 31104175.808;
$str = number_format($val, 2, "-", "*");

// RESULT:
// $str = "31*104*175-81"
```

---

## `strrev()`
- **reverses a string**

### `strrev() parameters`
| **Parameter** | **Description**                               |
|---------------|-----------------------------------------------|
| _**string**_  | **Required**. Specifies the string to reverse |

### `strrev() return value`
The reversed string

### `strrev() example`
```php
$str1 = "computer science";
$str2 = strrev($str1);

// RESULT:
// $str2 = "ecneics retupmoc"
```