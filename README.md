Instagram Parser
=================
[![Latest Stable Version](http://poser.pugx.org/aunhurian/instagram-parser/v)](https://packagist.org/packages/aunhurian/instagram-parser) [![Total Downloads](http://poser.pugx.org/aunhurian/instagram-parser/downloads)](https://packagist.org/packages/aunhurian/instagram-parser) [![Latest Unstable Version](http://poser.pugx.org/aunhurian/instagram-parser/v/unstable)](https://packagist.org/packages/aunhurian/instagram-parser) [![License](http://poser.pugx.org/aunhurian/instagram-parser/license)](https://packagist.org/packages/aunhurian/instagram-parser) [![PHP Version Require](http://poser.pugx.org/aunhurian/instagram-parser/require/php)](https://packagist.org/packages/aunhurian/instagram-parser)

The Instagram parser gives you an easy interface to parse all the Instagram's
data. Like an API, but without being it! You can get posts by a tag, all user posts 

## Setup
```shell
composer require aunhurian/instagram-parser:dev-master
```
Before run your parsers, you first need a **query hash**. Follow this 5 steps to 
get yours: [How to get a query hash](/docs/setup.md#how-to-get-your-query-hash-old-query-id).

## Start parsing!
Let's parse all data tagged with the string "github" for instance. You will get a scaled infinite 
loop of posts related to it until they are finished.
```php
use Mineur\InstagramParser\Instagram;
use Mineur\InstagramParser\Model\InstagramPost;

$queryHash = '298b92c8d7cad703f7565aa892ede943';

Instagram::createTagParser($queryHash)
    ->parse('github', function(InstagramPost $post) {
        dump($post);
    });
```
### The console dump will be like this:
![](docs/img/example.gif)


## Motivation
Since Instagram has restricted its API only to registered and verified applications, 
you can't get all of its public data being an experimental user or a data science 
analyst who just wants to play with that, you only have access to the API sandbox mode.

So I decided to create an alternative parser on top of GuzzleHttp library to access 
to the entire data with a nice interface.

## Documentation
For more information about this library [see the docs](/docs/index.md).
