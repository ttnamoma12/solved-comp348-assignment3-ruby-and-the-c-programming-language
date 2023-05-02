Download Link: https://assignmentchef.com/product/solved-comp348-assignment3-ruby-and-the-c-programming-language
<br>
This assignment covers both Ruby and The C Programming Language, imperative as well as multi-paradigm programming.




<h1><a name="_Toc5002"></a>2             Your Assignment</h1>

This assignment consists of two parts:

<ol>

 <li>The C Programming Language,</li>

 <li>Ruby</li>

</ol>

<h2><a name="_Toc5003"></a>2.1            The C Programming Language</h2>

Q 1. Pointers

You know in Java, a called method from main can not change the value of an integer declared in main. For example:

public static void main() {

int a = 3;

CallFun( some parameters );

System.out.println(a);

}

The above code will always print 3 on the screen no matter what happens in CallFun or its arguments.

Using pointers, rewrite the above program in C so that when CallFun is invoked the value of a is changed to 17 in the main function. You need to pass only one parameter to CallFun.

You decide what that parameter is and what its type is.

Q 2. Pointers arithmetic &amp; pointers to arrays and array elements

Use ONLY pointer arithmetic to implement the Selection Sort algorithm. You will also need to implement DisplayArray function that takes an array as a parameter and the number of elements it has and displays its content on the screen. The DisplayArray function should ONLY use pointer arithmetic.

For example:

int main() { int arr[5] = {1, 13, 5, 17, 11};

DisplayArray (arr, 5);

SelectionSort (arr);

DisplayArray (arr, 5);

}

Output:

1, 13, 5, 17, 11

1, 5, 11, 13, 17

Q 3. Memory management and records

Create a struct to represent a Book. The book has a title of type char* and a price of type oat. The main program reads the number of books n to store. Then the program creates an array with exactly n elements.

The program then reads the information of each book and store them one by one in the array.

Develop a function Display that takes an array of Book and the number of books in the array. The Display function displays the content of the array on the screen.

Develop another function AverageBookPrice that takes an array of Book and the number of books in the array and returns the average book price of all books in the array.

Develop a function Add that reads the info of a Book from the user and:

<ol>

 <li>Expands the size of the array by 1</li>

</ol>

Hint: create a new array and copy all books from old to new. Do not forget to free the old array

<ol start="2">

 <li>Adds the new book at the end of the newly created array</li>

</ol>

<h2><a name="_Toc5004"></a>2.2            Ruby</h2>

This section consists of three parts that are related, but may be implemented independently.

Q 4. Classes in Ruby

De ne the following class hierarchy in Ruby

<ol>

 <li>Shape

  <ul>

   <li>: the class constructors receives no parameter.</li>

   <li>: method print(): prints the name of the shape, perimeter, and area of the shape.The name of the shape is the class name (i..e Shape for this class).</li>

   <li>: method perimeter(): default method to be implemented by child classes; returning nil by default.</li>

   <li>: method area(): default method to be implemented by child classes; returningnil by default.</li>

  </ul></li>

 <li>Circle

  <ul>

   <li>: the class constructor receives the radius as the only parameter.</li>

   <li>: method perimeter(): overridden, returns the perimeter of the circle.</li>

   <li>: method area(): overridden, returns the area of the circle.</li>

  </ul></li>

 <li>Rectangle

  <ul>

   <li>: the class constructor receives the height and width of the rectangle.</li>

   <li>: method perimeter(): overridden, returns the perimeter of the rectangle.</li>

   <li>: method area(): overridden, returns the area of the rectangle.</li>

  </ul></li>

 <li>Ellipse

  <ul>

   <li>: the class constructor receives the semi-major and semi-minor axes (<em>a </em>and <em>b</em>).</li>

   <li>: method perimeter(): not to be implemented.</li>

   <li>: method area(): overridden, returns the area of the ellipse (<em>A</em>=<em>πab</em>).</li>

   <li>: method eccentricity(): additional method that returns the eccentricity of the</li>

  </ul></li>

</ol>

√ ellipse (<em>e</em>= <em>a</em><sup>2 </sup>−<em>b</em><sup>2</sup>).

Q 5. File / Text Processing

Write a Ruby program that reads text le that contains the shape information (see previous question). Every line in the text le consist of shape name and parameters to construct the shape. The program create every shape and calls the print method and displays the result on the screen. In case of errors (i.e. having negative values for sides, radius, etc.), and error message may be displayed. An example given below:

Input:

shape

rectangle 10 20 rectangle 0 10 circle 2 ellipse 2 4

ellipse -1 4

Output:

Shape, perimeter: undefined, area: undefined

Rectangle, perimeter: 60, area: 200

Rectangle, perimeter: 0, area: 0

Circle, perimeter: 12.5663706144, area: 12.5663706144

Ellipse, perimeter: undefined, area: 25.1327412287

Error: Invalid Ellipse

Q 6. Arrays and Hash

Extend the above program to display a statistics of the shapes after the text          le is processes.

An example is given in the following Output:

Statistics:

Shape(s): 5

Rectangle(s): 2

Circle(s): 1

Ellipse(s): 1

Use hashes to implement the above structure in memory.

Note that rectangles, circles, and ellipses are counted as shapes as well.