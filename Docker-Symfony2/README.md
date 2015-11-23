## Docker for Symfony2 Projects

### Features
* PHP 5.5
* Mbstring extension
* Intls extension
* SQlite 3 for Development Environment
 
### How to run
```
sudo docker run -it -p 9999:9999 -v /symfony/project/path:/usr/src/myapp afelipetrujillo\php-symfony2
```
Replace **/symfony/project/path** to your local folder where is symfony root path project.
