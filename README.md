# JavaScript_vs_Python

**-> Difference between the JavaScript and Python**
    
    **Java script**
    ->number - 10, 9.567
    ->Boolen - true, false (starts with samll letter)
    ->String - enclosed with ( "_", '_', `_`(backticks) )
    ->Undefined -
	    reasons : 1) Variable is declared but not assigned value
		            2) Accessing non-existent object property
			              Ex: const user = { name: "Kiran" };
                			    console.log(user.age); // undefined (no 'age' property)
		            3) Function with no return statement
			              Ex : function greet() {
  				                  console.log("Hello");
			                   }
			                   let result = greet(); // Hello
                         console.log(result);  // undefined (no return value)
		          4) Function parameter not passed
              			Ex: function sayHello(name) {
  				                console.log("Hello " + name);
			                  }
			                sayHello(); // Hello undefined
		       5) Array element not initialized
			              Ex: let arr = [1, , 3];
			                  console.log(arr[1]); // undefined

    -> parseInt("") : Convert the String to Integer 
		    Ex: parseInt("20") -> typeof(20) -> number

    -> typeof() operator

    -> Conditional Statements  (uses {} ; else if)
	          let num = 10;
	          if (num > 0) {
    	          console.log("Positive");
          	} else if (num === 0) {
    	          console.log("Zero");
	          } else {
                console.log("Negative");
	          }

    -> Ternary operator
	        (condition ? True_Value : False_Value)
	        let result = (num > 0) ? "Positive" : "Negative";

    -> JavaScript Functions
	-> Function Expression : 
		1st -> Declare a variable
		2nd -> Assign a function to that variable
		3rd -> Call the Function using variable name
		Ex: 
		const greet = function(name) {
  			return "Hello, " + name + "!";
		};
		console.log(greet("Mukesh"));               // Output: Hello, Mukesh!
  
	-> Function Declaration :(Normal function)
		function greet(name) {
 	 		return "Hello, " + name + "!";
		}
		console.log(greet("Mukesh"));  // Output: Hello, Mukesh!
  
    -> Loops 
	    	-> Basic Loop (for loop)
	     		for (let i = 0; i < 5; i++) {
	  			console.log(i);
			}
	  	-> For_of Loop : Used to iterate Array
	   		const fruits = ['apple', 'banana', 'cherry'];
			for (let fruit of fruits) {
			  console.log(fruit);
			}
		-> For_in Loop : used to iterate Object
	 		const user = { name: "Alice", age: 25 };
			for (let key in user) {
			  console.log(key, user[key]);
			}
	  	-> While Loop : 
	   		let i = 0;
			while (i < 5) {
			  console.log(i);
			  i++;
			}
  
    -> Data Structures
 		JavaScript 
		-> Array holds an ordered sequence of items
		-> Array creation :  let myArray = [1,"two",3,3.5]
		-> Accessing the elements ( console.log(myArray[0]) )
		-> Modifyin the Array ( myArray[1] = 1 )   
		-> Finding the Array Length : ( myArray.length )		
		-> Adding the element into array : ( myArray.push(5) )         // [1,"two",3,3.5,5]
		-> Remove the element from array : ( myArray.pop() )           // [1,"two",3,3.5]

  	-> Object
   		-> Objects rae collections of Properties (Key & value pairs)
		-> Creating The Object 
			let person = {
		  		name: "Alice",
		  		age: 30,
		  		greet: function() {
		    			console.log("Hello " + this.name);
		  			}
				};
			person.greet();          // Hello Alice

		-> Keys are the identifiers 
			- It containe alphanumeric, _ , $ ($name, _name, name12, name)
			- It should not start with number (12name, name 12)
		-> If I want to  use invalid identifier I can specify that key in the Quotes("")
			"1" : ......,  "my name" : .......
		-> Accessing the properties in Object ( . Dot notation, [] Bracket notation )
			console.log(person.name)    // when the key is valid identifier
			console.log(person["1"])    // when the key is invalid identifier we can use bracket notation
			console.log(person["name"])  // bracket notation 
		
		-> let person = {name:"Rahul", age:28,}; let a = "name"    
			console.log(person[a])  // inside the brackets a consider as variable  // o/p Rahul
			console.log(person.a)   // o/p undefined
		-> Object Destructuring : Unpacking the properties and assigning the properties to variables
			let {name} = person;
				here : name is a variable, it should match with key in the Object
			let {gender,name} =person;       
			console.log(gender)   //     undefined
			console.log(name)     //     Rahul
		-> Modifying the Object
			person.name = "Mukesh"
			person["name"] = "Mukesh"
		-> Adding the new property to Object
			person.gender ="male"
			person['gender']="male"
		-> Property Values : we can assign the FUnction, array, object as value to the Key
			class User {
		  		constructor(name) {
		    		this.name = name;
		  		}
			}

			const person = {
		  		name: "Alice",                          // string
		  		age: 25,                                // number
		  		hobbies: ["reading", "gaming"],         // array
		  		address: { city: "NY", zip: "10001" },  // object
		  		greet: function () {                    // function
		    		     return `Hello, ${this.name}`;
		  		},
		  		isActive: true,                         // boolean
		  		score: null,                            // null
		  		details: undefined,                     // undefined
		  		userClass: new User("Alice")            // class instance
				};
	
			console.log(person.name);               // Alice
			console.log(person.hobbies[0]);         // reading
			console.log(person.address.city);       // NY
			console.log(person.greet());            // Hello, Alice
			console.log(person.userClass.name);     // Alice

		-> document.createElement() 
			Here : createElement = key 
			       createElement() = method ( calling createElement function in document Object)



    **Python**
    ->Integer type - 10
    -> float type - 9.676
    -> Boolean type - True, False (starts with capital letter)
    -> String - enclosed with ( '_', "_", '''_'''/ """_""" (Multi Line String) )

    -> int("")  : Ex : int(float("12.34")) -> Sring to Float to Int -> type(1234) -> Integer

    -> type() operator 

    -> Conditional Statements  (indentation(:) elif)
	        num = 10
	        if num > 0:
    	        print("Positive")
	        elif num == 0:
    	        print("Zero")
	        else:
              print("Negative")

    -> Ternary operator (single line if-else)
	        ( a if condition else b )
	        result = "Positive" if num > 0 else "Negative"

    -> Python Functions
	-> Normal Function 
		def greet(name):
    	     	     return f"Hello, {name}!"
		message = greet("Mukesh")
		print(message)                    # Output: Hello, Mukesh!
  
     -> Loops 
	    	-> Basic Loop (for loop)
	     		for i in range(5):
    			     print(i)
	  	-> For_in Loop : Used to iterate List
    			fruits = ['apple', 'banana', 'cherry']
			for fruit in fruits:
			    print(fruit)	
		-> dict.items() : used to iterate dictionary
	 		user = { "name": "Alice", "age": 25 }
			for key, value in user.items():
			    print(key, value)

	  	-> While Loop : 
	   		i = 0
			while i < 5:
			    print(i)
			    i += 1

    -> DataStructures in python
    	Python
	-> List holds an ordered sequence of items
	-> List creation : my_list = [1, 2, 3, 4, 5]
	-> Accessingg the List ( print(my_list[0]) )
	-> Modifyoing the List ( my_list[1] = 25 )
	-> Finding the Array length : ( len(my_list) )
	-> Add element in List : 
		1) Append() : adds one item at the end
			my_list.append(4)
		2) insert() : adds Item at specific index
			my_list.insert(1, 10)        // Insert 10 at index 1
		3) extend() : Adds multiple items
			my_list.extend([5, 6])
	-> Remove the element in List :
		1) pop(index) : It removes elemnt at specific index
			removed = my_list.pop(1)
		2) remove(value) – Removes the first occurrence of a value
			my_list.remove(20)
		3) clear() – Removes all elements
			my_list.clear()


    -> Dictionary 
    	-> Dictionary rae collections of Properties (Key & value pairs)
	-> creating Dictionary
		person = {
	    		"name": "Alice",
	    		"age": 30
			}
	
		def greet(p):
	    		print("Hello", p["name"])
	
		greet(person)  			// Hello Alice

	-> Keys can be immutable types( String, tuple, int, Boolean) 
	-> Accessing the dictionary
		print(person["name"])    // bracket notation 
	-> Unpacking in python (destructuring in JS)
		name, age = person["name"], person["age"]
	-> modify the dictionary
		person["age"] = 30 
	-> add the item/property for dictionary
		person["city"] = "New York"
	-> Property Values : we can assign the FUnction, array, object as value to the Key
		1) Assigning a List
			my_dict = {
	    			"fruits": ["apple", "banana", "cherry"]
			}
			print(my_dict["fruits"][1])    # Output: banana
		
		2) Nested Dictionary
			my_dict = {
	    			"person": {
	        			"name": "Alice",
	        			"age": 25
	    				}
				}
	
			print(my_dict["person"]["name"])  # Output: Alice
	
		3) Assigning a Function
			def greet(name):
	    		     return f"Hello, {name}!"
	
			my_dict = {
	    		     "say_hello": greet
			}
	
			print(my_dict["say_hello"]("Mukesh"))  # Output: Hello, Mukesh!

## Todos_Application-1
### Agenda : HTML input(CheckBox) -> HTML Elements(Label) -> Dom Manipulations(html for setAttributes)

#### Add Check Box Statically

	<input type="checkbox">

#### Add Label to CheckBox
	<input type="checkbox" id="checkid"> 
    	<label for="checkid">Graduated</label>

#### Create CheckBox Dynamically using JavaScript
	let checkboxElement = document.getElementById("input")
	checkboxElement.type="checkbox"
	checkboxElement.id="checkboxid"
	document.body.appendChild(checkboxElement)

 	let labelElement = document.getElementById("label")
	labelElement.htmlFor ="checkboxid"
	labelElement.textContent="Graduated"
	document.body.appendChild(labelElement)

 #### setAttribute() 
 	-> It allows to add attribute to the HTML element. if the attribute exists it will replace to that attribute
  	labelElement.setAttribute("for","checkboxid")
 	
### Agenda : InputElement (placeholder) -> Dom Manipulations(removeChild(), classList.toggle() ) -> Js Built-in function ( alert() )
#### classList.toggle() 
	-> Adds a class if it's not present and removes it if it is present
 	element.classList.toggle("className");

#### removeChild()
	-> It remove the Child Element/node from Parent Node
 	parentNode.removeChild(childNode);

#### PlaceHolder
	<input type="text" placeholder="What need to be done"/>

#### alert()
	displays a popup dialog with a message and an OK button

### Agenda : Local Storage(setItem(),getItem()) -> Value(null) -> HTML Element(textArea Element)
#### Reloads :
	When the user reloads the page the data(variables,objects,functions) got destroyed. The data Should be Persisted(data has been saved)
#### Local Storage
	Execution Context : It is the Environment where the Js Code is Executed. It contains all the variables,functions,Objects
 			   - When the user reloads the page Execution Context is Destroyed(all variables, functions... gone) and Again execution starts from line 1 Onwards again it will create   			     variables and functions..(memeory is freeUp)
       
       Storage Mechanisms : Client-Side Data Storage 
       				- Storing the Data on the Client(Users's machine/personal Laptop)
	   			- Storage Mechanisms : Local Storage, Session Storage, Cookies, IndexedDB,....
	   		  : Server-Side Data Stroage
				- Storing the Data on Servers using DataBases
    				- Storage Mechanisms : Sql Databases, NoSql Databases

 	Local Storage : To store the data Locally within the User's Browser
  			- It is the Storage Object. It store the Data in the form of Key-Value pairs. (note: Value Should be in String)
     			- methods provided by th JS for Local Storage (setItem(), getItem(), clear(), removeItem())

 	setItem()  : Used to set the key-value in the localStorage
  		     - syntax: localStorage.setItem("key","Value");
		Access the LocalStorage : Inspect -> Application -> Local storage

  	getItem() : used to get item from Local Storage
   		    - syntax : localStorage.getItem("key")
	 	    - If we get the key which is not present. It returns 'null'

	removeItem() 
      			- Syntax : localStorage.removeItem(key)

        null      : When to use the null -> when the user want to assign the value to variable after some time we can use null(initially - empty value, Later- real Value)
       		   Ex : let userData = null;
                        userData = { name: "Kiran", age: 25 };
		   - console.log(userData) o/p : null
     		   - console.log(typeof(userData)) o/p: object

	textArea Element(HtML)  : Multiple- line of Input
 				 - syntax : <textarea rows="8" cols="55"></textarea>

### Agenda : JSON Methods(JSON.parse(), JSON.stringify()) -> Local Storage(Storing TodoList in LocalStorage)

#### JSON (JavaScript Object Notation)
	-> It is a Data Representation Format
 	-> Used for :
  		- Storing the Data(Client/Server)
    		- Exchanging the Data Between the Client and Sever
      	-> Supported Types
	       		JavaScript	JSON
		 	- 10		- 10
	   		- "Hello"	- "Hello"
	     		- true		- true
	       		- [1,2,3]	- [1,2,3]
		 	- null 		- null
	   		- {		- {                              // key in Json Should be in String format
	     		    name:"Mukesh",   "name":"Mukesh",
		            age:23,          "age":23,
		     	    male:true        "male":true
		   	  }               }
       	-> To convert the Data into JSON format We have JSON method provided by JavaScript
			- JSON.parse()
	  		- JSON.stringify()
     	-> JSON.stringify() : Convert the Object into String
     		Ex: let profile = { name:"Mukesh",age:23,male:true}
       		    let strinifyProfile = JSON.stringify(profile)
	     	    console.log(stringifyProfile)             // '{name:"Mukesh",age:23,male:true}'   //So that we can Store this String has value in localStorage
 		    console.log(typeof(stringifProfile))      // String
		-> JSON.parse() : Convert String to Object
	 		Ex : let Profile = '{name:Mukesh",age:23,male:true}'
	   		     let parseProfile = JSON.parse(Profile)
		  	     console.log(parseProfile)               // {name:"Mukesh",age:23,male:true}
		 	     console.log(typeof(parseProfile))       // Object

 ### Agenda : splice(), findIndex()
 	-> Splice Method :  used to change the context of an Array(Add,Remove,Replace items)
  			    -> It returns Deleted items Array
  			Syntax : Removing 
     				arr.splice(Start,DeleteCount)
     				Start : Index
	 			DeleteCount : Number of items should be delete 
     			Example : 
	     			let fruits = ["apple", "banana", "cherry", "mango"];
				fruits.splice(1, 2); 	// Start at index 1, remove 2 items
				console.log(fruits); 	// Output: ["apple", "mango"]

    			Syntax : Adding  (DeleteCount=0)
       				arr.splice(Start,DeleteCount,Item1,Item2)       
	   			Items1,2 : Items to be added from Start Index
       			Example :
	  			let colors = ["red", "blue", "green"]; 
				colors.splice(1, 0, "yellow", "orange");     // Add "yellow" and "orange" at index 1
				console.log(colors);     	            // Output: ["red", "yellow", "orange", "blue", "green"]

     			Syntax : Replacing (DeleteCount = n.o of Items)
				 arr.splice(Start,DeleteCount,Item1,Item2)  
     			Example : let fruits = ["apple", "banana", "cherry", "mango"];
				  fruits.splice(1, 2, "grape", "kiwi");// Replace "banana" and "cherry" with "grape" and "kiwi"
				  console.log(fruits); // Output: ["apple", "grape", "kiwi", "mango"]

       	-> findIndex() : It returns the First Item in Array that Satisfys the Condition. If the Condition is not satisfy it returns -1
			-> Syntax : arr.findIndex(fuunction(element,index,array){} / callback(element,index,array))
   			-> Example : 
      					let numbers = [10, 25, 60, 40];
					let index = numbers.findIndex(function(num) {
					  return num > 50;
					});
     					console.log(index);      // Output: 2

 	-> find()   : Returns the first element in the array that matches the condition.
  			Syntax : arr.find(function(element,index,array){.....})
     			Example :
					let numbers = [1, 3, 5, 6, 8];
					let result = numbers.find(num => num % 2 === 0);
					console.log(result);  // Output: 6


### Aggenda : includes(), concat()
		-> To check the lement present in array/string, it returns boolean value
		-> syntax : arr.includes(value/item/element)
  		-> Example :
	    			const fruits = ['apple', 'banana', 'mango'];
				console.log(fruits.includes('banana'));  	// true
				console.log(fruits.includes('grapes'));  	// false
    		concat() : 
      			-> Syntax : let newArray = array1.concat(array2, array3, ...);

### Array Methods
		-> lastIndexOf() : It returns last index of given number
  			Example :
	    				let str = "hello world";
					let index = str.lastIndexOf("l");        // Output: 9

      		-> sort() : acending and Decending order
					- arr.sort()   // lexicographic
		   				Example :
		       						let numbers = [10, 2, 5, 1];
								numbers.sort();  // Output: [1, 10, 2, 5] → NOT numerical!
		      			- arr.sort((a,b)=>a-b)     // ascending
			 		- arr.sort((a,b)=>b-a)     // decending

	 			In Python :  list.sort(key=None, reverse=False)
     					Example: 
	  					numbers = [5, 2, 9, 1]
						numbers.sort(reverse=True)
						print(numbers)  # Output: [9, 5, 2, 1]

    		-> join() :  join elements of a list or array into a single string, using a separator
      				Example: 
	  					let arr = [1, 2, 3];
						arr.join("-");  // Output: "1-2-3"
						arr.join("");   // Output: "123"

      				In Python : separator.join(iterable)
						words = ["Hello", "World"]
						result = " ".join(words)
						print(result)  			# Output: "Hello World"


		-> slice(start,end)  : extract a portion of an array, list, or string without modifying the original.
  
  				Example :
      						let arr = [10, 20, 30, 40, 50];
						let result = arr.slice(1, 4);          // Output: [20, 30, 40]
      						arr.slice(-3);       // Output: [30, 40, 50]
						arr.slice(-4, -1);   // Output: [20, 30, 40]

      				In Python : [start:end:step]
	  					list = [10, 20, 30, 40, 50]
						result = list[1:4]  # Output: [20, 30, 40]
		
		-> push(),pop(),shift(),unshift() 
  					-> Add element at last  ( arr.push(element) )
       					-> Remove the lement at last (arr.pop())
	    				-> Remove the element at first  ( arr.shift())
	 				-> Add element at first ( arr.unshift(element) )

	  			In python : push(),pop(), pop(0), list.insert(0, element)

      		-> 


	 
## **DOM**
	-> How to Access the HTML Element using JavaScriprt
 		using : document.getElementById()
   		Ex : let pElement = document.getElementById("id_name")
     		     pElement.textContent = "ParaEmenet"
	    	     pElement.style.color ="blue"
	   	     pElement.src = "ImgUrl"
	-> How to Create HTML element using JavaScript
		Ex :
		let h1Element = document.createElement("h1");        // 1. Create a new element
		h1Element.textContent= "WebTechnologies"             // 2. Set text content
		console.log(h1Element) // <h1>WebTechnoligges</h1>
		document.body.appendChild(h1Element)		     // 3. Append to body

		let containerElement = document.getElementById("my_container")
		containerElement.appendChild(h1Element)              // 4. Appending the element to specific container(div)


	-> Adding the event Listener Dynamically
	
		let btnElement = document.createElement("button")
		btnElement.textContent = "Clickme";
		btnElement.onClick = function(){
			console.log("click event is clicked")
		}
		document.getElementById("my_container").appendChild(btnElement);

	-> Add class attribute to element ( <h1 class="heading">head</h1> )
		h1Element.classList.add("heading");
	
	-> Remove the class attribute
		h1Element.classList.remove("heading");
  

	->setAttribute() : It allows to add attribute to the HTML element. if the attribute exists it will replace to that attribute
		labelElement.setAttribute("for","checkboxid")

   	-> classList.toggle()  :  Adds a class if it's not present and removes it if it is present
    		element.classList.toggle("className");

      	-> removeChild() : It removes the Child Node(element) from the Parent Node(element)
 			parentNode.removeChild(childNode);

