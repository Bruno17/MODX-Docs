---
title: "MODX PHP Coding Standards"
_old_id: "1133"
_old_uri: "contribute/becoming-a-contributor/modx-php-coding-standards"
sortorder: 6
---

These coding standards primarily apply to PHP code.

## General

- Beginning brackets do NOT linebreak. They start one space after the end parenthesis, as according to traditional Unix policy.
- Do not do any real logic in object constructors. Create class methods to do so.
   null, true and false should always be lowercase.
- Avoid embedded assignments (ex: `$d = ($a = $b + $c)` is bad).
- Never use `extract()`.
- Avoid using global variables if at all possible.
- Document EVERYTHING.

## Parenthesis

- Do not put parenthesis next to keywords. Put a space between.
- Do put parenthesis next to function names.
- Do not use parenthesis in return statements when it's not necessary. Example:

``` php
if ($test) {
}
while ($test == $other) {
}
array_push($one,$two);
return $test;
```

- Do **not** use parenthesis when using `include`, `require`, `include_once`, and `require_once`.

## Classes

- All ''core'' classnames, unless stated otherwise for special conditions, will be prefixed with the "mod" prefix: ie, modChunk, modTemplate, etc.
- All method names will be camelCase and will start with a lowercase letter.
- All private methods and variables must be prefixed with the underscore \_ character.

``` php
class modFactor {
    public $publicVar;
    private $_privateVar;
    private function _privateFunc() { }
    public function publicFunc() { }
}
```

## Variables

Note these are not function arguments.

- Use all lowercase letters.
- Separate words with the underscore.

## Function Arguments and Class Variables

- The first letter is lowercase, rest are camelCase. Example:

``` php
class modFactor {
    public function testFunc($testVar, array &$anotherTest = array()) {
        $this->_privateVar = $testVar;
        $local_variable =& $anotherTest;
    }
}
```

## Arrays

- Array index names use the underscore \_, not the dash as their separator. This prevents errors with `magic\_quotes`.
- Array index names are always lowercase. Spaces are represented by an underscore.
- Array index names are always encapsulated with single quotes.
   Example:

``` php
$_lang['chunk_create_text'] = 'Test';
```

## Constants

- Constants must be in all UPPERCASE letters.
- Use only if absolutely necessary.

## File Structure

- Always name PHP class files in name.class.php format.

## Prefixing

- Lexicon strings for Components need to be prefixed:

``` php
$_lang['mycomponent.welcome_message'] = 'Welcome!';
```

- Always prefix class names; eg: 'finBank', 'finTransaction', etc.
- Always prefix [Chunk](building-sites/elements/chunks "Chunks") names; eg: 'finStatement', 'finDeposit'
