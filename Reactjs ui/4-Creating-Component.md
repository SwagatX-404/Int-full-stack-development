Downloading Libraries for React in existing web application

1. Open terminal and run the commands
    >npm install react@18 react-dom@18   --save
    >npm install @bable/standalone --save

2. Libraries are copied into "node_modules" 

3. We have to link the suitable module for our apllication

4. React 18 provides CJS and UMD module systems.
      CJS - Common JS
      UMD - Universal Module Distribution

5. NPM default enable with UMD in our project hence link the libraries from UMD.

    <script src="../node_modules/react/umd/react.development.js"> </script>
    <script src="../node_modules/react-dom/umd/react-dom.development.js">  </script>
    <script src="../node_modules/@babel/standalone/babel.js"> </script>

    # 🔹 Difference Between Single Call and Singleton in JavaScript

## 📌 1. Single Call - every request is created new object
- A function that executes **every time it is called**.  
- No state is preserved between calls.  
- Each call is **independent**.  

### ✅ Example:
```js
function greet() {
  console.log("Hello, Swagat!");
}

greet(); // "Hello, Swagat!"
greet(); // "Hello, Swagat!" again (new execution)
 
 ```

## 📌 2. Singleton - object is created for first request and the same object will be used across any no. of request. thiis mechanism is called singleton.

- A design pattern that ensures only one instance of an object exists.

- The same instance is reused across the app.

- Useful for: Database connection, Logger, Config manager.



## How to built Component .

- React is Component Based.
- A componenet comprises 
        1. Presentation  -   HTML
        2. Styles        -   CSS, Tailwind CSS
        3. Functionality -   JS   &    TS

- Component uses pre-defined services to handle various funtionalities, which include 
          1. Form Services
          2. Validation Services
          3. API Services
          4. Routing Services etc...

**Createing Component**
- React Component can be designed by using Class and Function
- Classes are supported but not recommended in modern React.

syntax:

              funtion Component(){

              }

              class Component {
                
              }

# Function Component rules:

- It can be defined as declaration or expression.
- Syntax: declaration 

          function Component ()
          {   

          }

- Syntax: expression 
            const Component = funtion () {

            }       

- Its name must start with an uppercase letter.
- It can't be void type.
- It must return a value.
- It must return a function with markup.
- Markup must be in one fragment. 

Syntax:   
funtion Login()
{
  return (
    <div>
    </div>
  );
}

- The markup returned by component function is known as JSX.
- Every component function  must return JSX element.
        

Syntax: 
         function Login(){
          return(
                  <h2> React </h2>   //invalid multiple fragments
                  <p>  JavaScript </p>
          );
         }

- JSX markup can't have void elements.

    <img>               //invalid
    <img> </img>        //valid
    </img>              //valid

    <input type="text"/>   //not
    <input type="text">  </input>   //yep

- Every element must end in JSX. 
- JSX elements can't use attributes, you have to use only properties.

          <img class="img-fluid"/>         //invalid
          <img className= "img-fluid"/>    //valid

          

