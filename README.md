# Usefull Drupal 8 snippets
 

## Token Replacement in Drupal.
<pre>
//Instantiate an token object.
$token_service = \Drupal::token() ;
// Pass the string which contains the token and context(Eg: node object, user object et..)
$token_replaced = $token_service->replace($string,['node' => $node_object ]);
</pre>
