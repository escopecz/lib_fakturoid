Fakturoid Joomla Library
========================

Installable library package for [Fakturoid.cz](https://www.fakturoid.cz/). 

[API documentation](http://docs.fakturoid.apiary.io/).
[Forked from Fakturoid's Github](https://github.com/fakturoid/php).

## Usage

```php
jimport('fakturoid.fakturoid');

$f = new Fakturoid('..subdomain..', '..user@email.cz..', '..api_key..', 'PHPlib <your@email.cz>');
$subject = $f->create_subject(array('name' => 'Firma s.r.o.', 'email' => 'aloha@pokus.cz'));
$lines   = array(array('name' => 'Big sale', 'quantity' => 1, 'unit_price' => 1000));
$invoice = $f->create_invoice(array('subject_id' => $subject->id, 'lines' => $lines));
```