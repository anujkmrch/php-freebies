# php-freebies

## Synopsis
Request response library to access content from remote server, with the help of library you can request html, json, xml or anything over web service.

## Code Example
To create new connection write

<?php 
$hostname = 'locahost'; // it can be the ip address of the system
$port = 80; // it may be any port, number, default port for apache web is 80
$domain = 'codebloop.com';
$path = '/';

$requester = new Curl_Connection($hostname,$port,$domain,$path); 
$fields = array('say'=>"hello");

$response = $request->get($fields);
//or 
$response = $request->post($fields);
/*
 * Do what ever operation your want to do with your result
 * For the sake of request
 */
 //result is an array of statuscode in case of http status code
 $result = $request->parse_result($result['result']);
 list($header,$content) = $result;
 
 // if you requested html content, the you can print it by typing to see result in browser
 echo $content;
 
 // or you can see any response
?>

## Motivation
A short description of the motivation behind the creation and maintenance of the project. This should explain **why** the project exists.

## Installation
Just download this file into your project, create connection and Provide code examples and explanations of how to get the project.

## License
A short snippet describing the license (MIT, Apache, etc.)
