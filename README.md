[![Build Status](https://travis-ci.org/Corollarium/validarium.svg?branch=master)](https://travis-ci.org/Corollarium/validarium)

Validarium
==========

A JQuery validation plugin: practical, simple and extensible. Validates your existing forms in HTML without headaches. 
Developed by [Corollarium](https://corollarium.com).

Licensed under the MIT license.

Some ideas and code borrowed from [jquery-validate](https://github.com/jzaefferer/jquery-validation/).

## Getting Started

Include jQuery and Validarium. Then apply Validarium to the form.

```html
<form>
	....
</form>
<script src="jquery.js"></script>
<script src="jquery.validarium.js"></script>
<script>
$(document).ready(function() {
	$("form").validarium();
});
</script>
```

You can download the package, clone the repository or use [bower](http://bower.io/).

```
bower install
```
 
## Full documentation

See https://github.com/Corollarium/validarium/wiki

## Examples

### Required fields

```html
<form>
	<input type="text" data-rules-required="true" />
</form>
```

### Required with another message

This works for all the other items, too

```html
<form>
	<input type="text" data-rules-required="true" data-rules-required-message="My message here" />
</form>
```

### Minlength, maxlength

```html
<form>
	<input type="text" data-rules-minlength="5" data-rules-maxlength="10" />
</form>
```
(note that minlength accepts empty values, if you don't want those use the "required" rule)

### Two fields must match
```html
<form>
	<input type="password" id="pw1" data-rules-equalto="#pw2"/>
	<input type="password" id="pw2" data-rules-equalto="#pw1"/>
</form>
```

### Field must obey a regexp
```html
<form>
	<input type="text" data-rules-regexp="^([a-zA-Z]{5})$" />
</form>
```

### Floating point numbers, with minimum and maximum
```html
<form>
	<input type="text" data-rules-min="4" data-rules-max="10" data-rules-number="true" />
</form>
```

### Positive integers, with minimum and maximum
```html
<form>
	<input type="text" data-rules-min="4" data-rules-max="10" data-rules-digits="true" />
</form>
```

### Strings with maximum and minimum length
```html
<form>
	<input type="text" data-rules-minlength="4" data-rules-maxlength="10" />
</form>
```

### Url, email, domain
```html
<form>
	<input type="text" name="someurl" data-rules-url="true" />
	<input type="text" name="someemail" data-rules-email="true" />
	<input type="text" name="somedomain" data-rules-domain="true" />
</form>
```

### CPF and CNPJ
```html
<form>
	<input type="text" name="customer-cpf" data-rules-cpf="true" />
	<input type="text" name="customer-cnpj" data-rules-cnpj="true" />
</form>
```

## License
Copyright (c) 2012 Corollarium Tecnologia http://www.corollarium.com
Licensed under the MIT license.
