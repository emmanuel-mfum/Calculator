# Calculator

This is a small project realised with the help of Node.js and the framework Express. These are the files for a server (calculator.js) running on Node that can be reached on a local machine using the local port 3000. From this port, two routes can be accessed : the home route "/", which brings the user to an html page (index.html) containing a form that expect the user to input two numbers, one in each input fields ; the other route "/bmicalculator" leads to an html page (bmiCalculator.html) and the user is expected to enter its weight in kg and height in meters (decimal ,like 1.xx).

Once the user submit the two numbers on the homepage, the server will respond by displaying the sum of these two numbers on the same page ( the route "/") with the message "The result of the calculation is ", followed by the sum.

For the BMI calculator, once the user inputs its weight and height, the server will calculate the user's BMI based on the values inputed by the user. The formula followed for such calculation is bmi = weight/(height * height). The message "Your BMI is " followed by the BMI value will be then displayed on the same page.

In order to manipulate the data sent by the user, we have to require the Express module bodyParser, thus allowing us to tap into the data sent as part of POST request. We retrieve the exact values by using the "name" attribute we assigned to our input fields such as n1, n2, weight or height.

We also have to cast these values retrieved from the request to the server from strings into numbers using the method Number();

For the BMI calculator, we casted our String values into floating numbers using parseFloat();

As Github Pages can only support static HTML pages, thus Node.js applications cannot be run on the Github Pages hosting service as outlined in this answer on StackOverFlow : https://stackoverflow.com/a/15719098

So while I find an appropriate hosting service for my modest Node.js app, I will just post the source code in this repository.

PS: The "node_modules" file containing all the modules installed for the app is missing as it is very voluminous. Thus if anyone wants to run this app, they will have to run "npm i" before "ng serve" as mentioned here : https://stackoverflow.com/a/50701585.
For this app I have just installed and used Node, Expressand Nodemon in order to run my server more efficiently using the command line npm in the Hyper Terminal
