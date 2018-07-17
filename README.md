# Usefull Drupal 8 Snippets.

This is a list of useful Drupal snippets and functions that I often reference to enhance or improve my sites.
 
 You can refer [my blog](https://thakshashila.com/) for more detailed explanation

- ### [Token Replacement in Drupal](#token-replacement-in-drupal-8)

- ### [Load Drupal 8 node object from URL alias](#load-drupal-8-node-object-from-url-alias)

## Token Replacement in Drupal
```php
//Instantiate an token object.
$token_service = \Drupal::token() ;
// Pass the string which contains the token and context(Eg: node object, user object et..)
$token_replaced = $token_service->replace($string,['node' => $node_object ]);
```
## Load Drupal 8 node object from URL alias
```php
//Your custom URL (alias).
$my_url_alias = 'about-me';
// This line will return corresponding system path.
// Lets say, '/node/15' is correcsponding path '/about-me'
$path = \Drupal::service('path.alias_manager')->getPathByAlias('/'.$ahurl);
if(preg_match('/node\/(\d+)/', $path, $matches)) {
// This will load the node object.
$node = \Drupal\node\Entity\Node::load($matches[1]);
}
```

- [Hide WordPress Update Nag to All But Admins](#hide-wordpress-update-nag-to-all-but-admins)

## Hide WordPress Update Nag to All But Admins