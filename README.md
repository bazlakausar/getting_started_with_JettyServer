# getting_started_with_JettyServer
   # INSTALLATION OF A STANDALONE JETTY SERVER
   
 1) Download Jetty from https://www.eclipse.org/jetty/download.html and extract the zip file somewhere to your filesystem.
 2) To start Jetty, switch on the command line to the installation directory and issue the following command
     
     java -jar start.jar
   This starts jetty on
   
   
   
   ![2](https://user-images.githubusercontent.com/79251268/131337935-dfd8ad56-b706-46b9-9e11-4ccf42517dcf.png)

   
   
  
 3) Now open a browser and go to localhost to check if Jetty was installed sucessfully:
   
     ```http://localhost:8080/```
      
  
  
  

  
  
 ![1](https://user-images.githubusercontent.com/79251268/131337335-50b88401-1eba-4829-8241-dfb4f7c2e72f.png)
 
 
 This error occurs since we don't have any data in the webapp directory.
 
 
 # Now that you have Jetty running, you can add web apps to it!
 
 1) Inside your jetty-base folder, we have a webapps directory.This is where your web apps will go.
      To add a web app to your server:
         a) create a folder inside the webapps directory.
         b) add your files inside your folder.

For example, create a HelloWorld folder inside your webapps directory. Inside the HelloWorld directory, save this HTML to a file named index.html
 
  
  ```<!DOCTYPE html>
<html>
	<head>
		<title>Testing Jetty</title>
	</head>
	<body>
		<h1>Happy Coding</h1>
		<p>Hello world!</p>
	</body>
</html>
```

2) Now open your web browser:
    
    ```http://localhost:8080/HelloWorld/index.html```
    
    
    
    
    
    ![3](https://user-images.githubusercontent.com/79251268/131339556-10fa34dd-2779-4aa9-a08e-b86e98cb296b.png)

# ROOT WEBAPP

   In case of multiple web apps running on the same server, you can might create a “top level” web app that doesn’t include its name in its URL. To do this follow the below steps:
   1) In your webapps directory, create another folder named root.
   2) Inside the root folder, save this HTML to another file named index.html as shown below:
   
   
   ```<!DOCTYPE html>
<html>
	<head>
		<title>Root Web App</title>
	</head>
	<body>
		<h1>Root Web App</h1>
		<p><a href="http://localhost:8080/HelloWorld/index.html">Here</a> is a link to the Hello World app.</p>
	</body>
</html>
```

Now open web browser to:
    ```http://localhost:8080/index.html``` 
    
    
    
    
    
   
   ![4](https://user-images.githubusercontent.com/79251268/131340831-994d7755-778a-4cea-ba69-f60b282aa924.png)

   

    
    
    

   
