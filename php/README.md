# PHP guidelines

- [Overview](#1-overview)
- [General](#2-general)
  + [Files](#2-1-files)
  + [Lines](#2-2-lines)
  + [Indenting](#2-3-indenting)
  + [Keywords and True/False/Null](#2-4-keywords-and-true-false-null)
- [Namespace and Use Declarations](#3-namespace-and-use-declarations)
- [Classes, Properties, and Methods](#4-classes-properties-and-methods)
- [Control Structures](#5-control-structures)
- [Closures](#6-closures)
- [Conclusion](#7-conclusion)


## 1. Overview

Files MUST use only `<?php` tag.

Files MUST use only UTF-8 without BOM for PHP code.

Code MUST use 4 spaces for indenting, not tabs.

Class names MUST be declared in `StudlyCaps`.

Class constants MUST be declared in all upper case with underscore separators.

Method names MUST be declared in `camelCase`.

There MUST NOT be a hard limit on line length; the soft limit MUST be 120 characters; lines SHOULD be 80 characters or less.

There MUST be one blank line after the `namespace` declaration, and there MUST be one blank line after the block of `use` declarations.

Opening braces for classes MUST go on the next line, and closing braces MUST go on the next line after the body.

Opening braces for methods MUST go on the next line, and closing braces MUST go on the next line after the body.

Visibility `public`, `protected` and `private` MUST be declared on all properties and methods; `abstract` and `final` MUST be declared before the visibility; `static` MUST be declared after the visibility.

Control structure keywords MUST have one space after them; method and function calls MUST NOT.

Opening braces for control structures MUST go on the same line, and closing braces MUST go on the next line after the body.

Opening parentheses for control structures MUST NOT have a space after them, and closing parentheses for control structures MUST NOT have a space before.


## 2. General

### 2.1. Files

PHP code MUST use only UTF-8 without BOM.

PHP code MUST use the long `<?php ?>` tag; it MUST NOT use the other tag variations.

All PHP files MUST use the Unix LF (linefeed) line ending.

All PHP files MUST end with a single blank line.

The closing `?>` tag MUST be omitted from files containing only PHP.

### 2.2. Lines

There MUST NOT be a hard limit on line length.

The soft limit on line length MUST be 120 characters; automated style checkers MUST warn but MUST NOT error at the soft limit.

Lines SHOULD NOT be longer than 80 characters; lines longer than that SHOULD be split into multiple subsequent lines of no more than 80 characters each.

There MUST NOT be trailing whitespace at the end of non-blank lines.

Blank lines MAY be added to improve readability and to indicate related blocks of code.

There MUST NOT be more than one statement per line.

### 2.3. Indenting

Code MUST use an indent of 4 spaces, and MUST NOT use tabs for indenting.

> N.b.: Using only spaces, and not mixing spaces with tabs, helps to avoid
> problems with diffs, patches, history, and annotations. The use of spaces
> also makes it easy to insert fine-grained sub-indentation for inter-line 
> alignment.

### 2.4. Keywords and True/False/Null

PHP [keywords](http://php.net/manual/en/reserved.keywords.php) MUST be in lower case.

The PHP constants `true`, `false`, and `null` MUST be in lower case.


## 3. Namespace and Use Declarations
When present, there MUST be one blank line after the `namespace` declaration.

When present, all `use` declarations MUST go after the `namespace`
declaration.

There MUST be one `use` keyword per declaration.

There MUST be one blank line after the `use` block.

For example:

```php
<?php
namespace Vendor\Package;

use FooClass;
use BarClass as Bar;
use OtherVendor\OtherPackage\BazClass;

// ... additional PHP code ...

```

## 4. Classes, Properties and Methods


## 5. Control Structures


## 6. Closures


## 7. Conclusion
