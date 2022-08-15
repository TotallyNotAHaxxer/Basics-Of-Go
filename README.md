```

 ______     ______     __         ______     __   __     ______        ______   ______     ______        ______   __  __     ______        __     __    
/\  ___\   /\  __ \   /\ \       /\  __ \   /\ "-.\ \   /\  ___\      /\  ___\ /\  __ \   /\  == \      /\__  _\ /\ \_\ \   /\  ___\      /\ \  _ \ \   
\ \ \__ \  \ \ \/\ \  \ \ \____  \ \  __ \  \ \ \-.  \  \ \ \__ \     \ \  __\ \ \ \/\ \  \ \  __<      \/_/\ \/ \ \  __ \  \ \  __\      \ \ \/ ".\ \  
 \ \_____\  \ \_____\  \ \_____\  \ \_\ \_\  \ \_\\"\_\  \ \_____\     \ \_\    \ \_____\  \ \_\ \_\       \ \_\  \ \_\ \_\  \ \_____\     \ \__/".~\_\ 
  \/_____/   \/_____/   \/_____/   \/_/\/_/   \/_/ \/_/   \/_____/      \/_/     \/_____/   \/_/ /_/        \/_/   \/_/\/_/   \/_____/      \/_/   \/_/ 
                                                                                                                                                        
                                                                       ,_---~~~~~----._         
                                                                _,,_,*^____      _____``*g*\"*, 
                                                               / __/ /'     ^.  /      \ ^@q   f 
                                                              [  @f | @))    |  | @))   l  0 _/  
                                                               \ /   \~____ / __ \_____/    \   
                                                                |           _l__l_           I   
                                                                }          [______]           I  
                                                                ]            | | |            |  
                                                                ]             ~ ~             |  
                                                                |                            |   
                                                                 |                           |   
```

# Introduction to this article 

Alot of my friends and team mates apart of the scare security team have been asking me alot to write a article on the go programming language, unloucky for them i ended up writing one for just advanced golang rather than straight up the basics of go, so this article will be directed more towards the basics of go, what it can and should be used for, how easy it is, and setting up things such as go.mod files and what not so lets get started.

# Introduction to myself 

Whoami? my name is RE43P3R/ArkAngeL i am a current game cheat developer, systems developer, upcoming cyber security expert and legacy systems developer specializing in languages like Fortran, Perl, Go, Ruby, C++, and other languages among the list. My plan in life with this skill is to teach people how to make secure robust applications with a focus on security and to even maybe make some scripts like the red rabbit framework to benefit all kinds of hackers. As i go on and go to build the golang article on advanced go you will often see me mention about the laziness in most modern day developers, which can cause issues with security and the response of an application. However here i will not be talking about that because i find it quite useless as a begginer to complain and turn you off, but that does not mean i will not be talking about general security.

# The language itself and my personal thoughts 

If you feel like skipping this because it IS VERY WELL BIAS go ahead and skip it, for the people that want to read on lets go about it. Golang has always stuck out as a programming language for me, alot of people do not know how to teach it properly or know how to use it which is why i am writing this article as well for my friends. I have had experience in ALOT of languages such as perl, python, R, Lua, C, C++, Go, Ruby, and so on the list just goes on and out of all of the languages my favorite modern day programming language has to be go. This is due to how fast go is, the architectures and systems it can compile for, the community is amazing and is not as toxic and how truly well go respects data types unlike alot of languages. It also makes you write good english which means if you want to export a variable, constant, or function from another module the first letter of that function variable or constant MUST be capitalized. 

There is a bunch i can say about go but by far golang is the most awkward but amazing language i have come across. Go is a high level language which actually gives you the speed and performance of a low level languages made to perform well.

# Starting off with go, what do you use it for? 


In short the go programming language is a statically typed programming language which means it has primitive data types like int, string, uint, float, byte and even arrays such as `[]byte` or `[]string` which is a byte or string array and even has things like aliases to the integer32 data type which is called a rune defined by `rune`.

Now i will not lie to you here and say golang has the best syntax like some people say because it does not, go especially in terms of syntax does have a learning curve but im sure you will be able to figure it out pretty easily. Go has alot of uses like the following 

```
cyber security 

digital forensics such as 
   - Network forensics 
   - Image forensics 
   - File forensics

Data parsing and marshaling

Network services and tools 

Computer science for things like algorithmic implimentation

Encryption

and others...
```

Go makes it easy to do alot of those topics, especially given alot of the packages that go uses for cyber security that are third party were developed by google or members of google if you think about it, it kind of makes you a little bit more trusting of the software that you are using given it was developed by alot of skilled programmers and developers! ( Not saying there are not skilled developers outside of google )


# Writing code in go

> Golang files 

Go has 3 ways of declaring itself, Go code will be stored in files called `.go` files. These files will be used to write modules, export and import code and third party libraries as well as where your main files will be, the second file is called a `go.mod` file, go.mod files are the files go uses to declare a package name, importing and exporting of golang libraries, as well as other information about your module or workspace, visit `https://go.dev/doc/modules/gomod-ref#:~:text=The%20go.,otherwise%20select%20a%20different%20version.)` for more information on the `go.mod` files.

The last file is called a go.sum module, this is exactly what it sounds like, essentially it is a golang summary of the checksums of direct and indirect dependancies required by the go.mod file, here is an example of what a `go.sum` file would look like compared to a go.mod file 

**go.sum file**

```go
gopkg.in/yaml.v2 v2.4.0 h1:D8xgwECY7CYvx+Y2n4sBz93Jn9JRvxdiyyo8CTfuKaY=
```

**go.mod file**

```go
module main

go 1.17

require (
	gopkg.in/yaml.v2 v2.4.0 // indirect
)
```

as you can see the go.sum file just takes the required indirect or direct packages and requirements inported into the go.mod file and puts it inside of itself.

> Creating a go.mod file 

When you want to create a large project it is suggested you need modules, but in order to import and export other .go files from other filepaths you will need to create a go.mod file first so here is how we are going to do that 

say we want to make a module named hello 

`go mod init hello`

will produce the file `go.mod` and inside of the go.mod file will be 

```go
module hello

go 1.17
```

First you see the module named hello and the golang version

**How do you use a go.mod file**

Well here is how you would use it 


Using a go.mod file is easy but first we may want to create a simple program to output hello world and import the function from another go file in order to put the go.mod file to use. Now warning: there are other ways to use a go.mod file, as discussed you will need a go.mod file even when you are not importing your own modules but rather someone elses modules, We will get into that later, for now lets focus on our program.


we will have the following filepath in our home directory 

`/home/reaper/test`

inside of test is the following tree 

```
test
├── go.mod
├── main.go
└── Modules
    └── runner.go
```

we have our go.mod file which we chose to make the module name `hello` defined above, a main.go file which right now is empty, and another directory named `Modules` that has a file named runner, runner will be the file we want to import the functions from so lets get into that and start writing our very first go program but with modules!

**Modules/runner.go**

```go
package runner 

import "fmt"

func Hello() {
    fmt.Println("Hello world! i am from another module")
}
```

First we define our package name as runner, this means every single file or other .go file in this filepath `Modules` must ALSO have the package name of runner i know thats a bit confusing. Anyway we go on to define a function using the `func` keyword, and define the function name as `Hello` which takes no arguments. Then finally we throw brackets to declare a code brick and declare the fmt.Println("") function with the string `Hello world! i am from another module`. 

Go has alot of way of outputting data, formatting it, standardizing it, or prepping it for output and using the fmt package we can for sure do that! here we define `fmt.Println` which fmt stands for `format` and calls the `fmt` package, and Println simply prints data but for every bit of data you print it will print a new line after that preventing collision from other text. You do NOT need the fmt package to print data, you can simply use `println` or `print` as a standard output function without importing the `fmt` standard package. Moving on

lets hop out of the modules directory and head to our main.go file. 

**NOTE: YOUR MAIN FILE TYPICALLY NAMED `main.go` WILL ALWAYS HAVE TO HAVE THE PACKAGE NAME `main` IF THE PACKAGE NAME IS NOT MAIN IT WILL NOT RUN THE CODE**

**main.go file**

```go
package main 

import Runner "hello/Modules"

func main() {
   Runner.Hello()
}
```

This is a quite simple file, it declares that this is the main file, and imports ALL go files within the directory `Modules` by declaring Runner. we declare our main brick of code with `func main() {}` NOTE: MAIN CAN NOT TAKE ANY ARGUMENTS, IF ANY ARGUMENT IS DECLARED IN THE MAIN FUNCTION IT WILL NOT RUN GO WILL SEE THIS AS A FATAL ERROR AND MISTAKE. under our brackets we declare the word `Runner` which again Runner is a variable that now holds all data we imported from the filepath `Modules` from other `.go` files. and we call the function `Hello()`

to run this program we can do one of two things, compile or just run it raw without compiling to a binary 

to compile the code just for your machine use 

`go build` along with your main file to compile it and make it an executeable file so here is an example for our case

to compile and run the main.go file we need to build it 

`go build main.go` will produce `main` which we can execute with `./main` which will output 

```
(~/test)$>go run .
Hello world! i am from another module
```

## End discussion of this section  | Section 0x001 ##

Making modules is simple but there are a few rules that apply such as the following 

> All functions that are imported or exported from another module or `.go` file must start with a capital letter, like i have shown you in the function `Hello` in the `Runner.go` file

> All variables, structures, and other forms of data like functions must start with a capital letter to be exported or imported.

> go.mod files can only be used in one workspace at a time, for example you can not import other modules from outside of that current folder for example say you are in file `home/reaper/test` but want to import modules from another filepath like `/home/reaper/Desktop/Modules` even if there was another go.mod file in that filepath you still could not import that module filepath so the folder `Modules` would have to be in `/home/reaper/test` and imported as `hello/Modules`

> Using `go get`, `go get` is a really nice command, it allows you to install third party modules from things like github, go.pkg.dev.io, and other various websites, as long as their is a go.mod file declaring that software you can go get it :) **Pun intended**

In summary as said above making modules can be tedious despite it being simple, however you can get the hang of it, and throughout this tutorial we will be using modules alot


# Working with variables, constants and data types | Section 0x002

I know i went a bit far above but let me slow down a bit and start explaining basic concepts to you, this section will talk about how variables work, how to modify them and when and how you can use them, same goes for the constants and data types in the go programming language.

## Variables ##



Working with variables can be a bit weird in go especially if you never use them. Go makes sure that you use EVERY single variable you declare, if not go will atually error out kinda like the way perl will also warn you about un used variables. 



### Declaring variables ### 

declaring a variable is simple in go, simply just use the `:=` operator to declare one, for example, say we want to declare a name `jake` with a variable called `name`

```go
package main 

func main() {
	name := "jake"
}

```

you can also use the var keyword to cluster variables like so 

```go
package main

var (
   name := "jake"
   age := 18
   name2 := "json"
   age2 := 15
)

func main() {}
```

this really comes in handy when declaring things like data type variables and what not even reaching data structures.

you can also define a variables data type with the var keyword or its value like so 


```go
package main 

func main() {
	var name string // define a empty variable and its data type which is a string
}
```

or

```go
package main 

func main() {
	var name = "jake" // declaring the variable name with its value
}
```

### Info moment -> taking a second to address go's security ###





Go respects alot of the code you write as long as you respect it yourself. Go is like a knife in order to use it properly and have the knife respect you, you must respect it first. Golang immediately will error out if a variable is not used, and will not be able to run or compile that is if the variable is declared but unused. you will get the error 

```
variable_name declared but not used | compiler
```

why does is go one of the few languages out there to do this? I have always seen it as a security issue / code / op issue, when you are developing code and do not use variables some compiles will erase it from the code, others will leave it in there which can cause clutter, and in the sense of debugging it can make your code way weirder to read especially if you do not use a variable. Not using variables can also lead to bugs which in a certian scenario can lead to a security vulnerability within the program, it is always good to make sure you use your variables in go or c or c++ or any language like that, however it just is better that go makes it mandatory to not allow you to make or declare variables without them being used, respect that and the language will come easier for you to learn and use.





### Constants ###

In a few we will talk about modifying the data type of variables, converting them and transporting them but unlike variables constants can not be modified which brings me to this next section which is talking about the use case of constants.

If you dont know this constants in ANY form mathematical, scientifical, or computational SHOULD NEVER BE ABLE TO CHANGE, constants should always live up to their name staying constant or static unlike variables which are fluid (constantly changing or of right to chnage)

constants are declared in go using the const keyword followed by the `=` symbol, then the variable or the variable and the data type, let me explain

here we simply use the const keyword to define a variable hello which has a value of hello, this variable is known as an untyped string because its data type is assumed not assigned

```go
const hello = "hello"
```

have you ever heard of implicit typing? I would not assume so if you have never programmed before or never took mathematics since it is a term that is very VERY rarely used in moder day programming languages today. Implicit typing is simple to understand, if you do not declare a data type before a variables value it becomes implicit or assumed which causes the `untyped string` as the data type of the constant. 




### Optional side of implicit typing if you are interested ###

**if you do not want to learn about legacy languages or learn how implicit typing is used and implimented skip this section and move on, if else continue reading**

Implicit typing was first implimented in the programming language fortran, for those who do not know fortran stands for FORMula TRANslation, Which means it was a programming language designed for exactly what it is, formula translation. A great way fortran would impliment data types is by assuming the variables data type based on its first letter using implicit typing.

for example follow the following program in fortran95 

```f90
PROGRAM main
	CHARACTER :: name
END PROGRAM main
```

fortran has a keyword you should always use in your programs called `implicit none` this tells fortran to NOT assume the data type of a variable based on its first letter. You see fortran without the decleration of `implicit none` would assume the variables data type based on the first letter of the variable, if the first letter was any of the following | `i, j, k, l, m, n` fortran would AUTOMATICALLY assume the variable to be a integer, if else it would be `REAL` which kinda translates to modern languages except the real meaning of implicit typing is not used, variables that are NOT defined with a data type before have their data types pre assumed. 

### concluding the implicit typing brick above | this is a seperation statement ### 




how do we fix this and prevent our data type from being assumed? Simple! all we do is just declare the constant keyword followed by the variable name, then its type which is followed by its value. As said before go really respects data types, and if you do not respect them as well you can cause fatal errors with your programs, so lets correct the constant hello to a propper more formal form and type 

```go
const hello string = "hello"
```

pretty simple right? Now we went from assuming the data type of the constant to assigning it which can make it alot less bugy in the future when working with more higher end programs and functions. like the `var` keyword you can also use the `()` to create a list of constants 

```go
package main 

const (
   name string = "jake"
   age int = 18
   name string = "john"
   age int 15
)
```

### Data types ###

Data types in go are pretty simple to understand and quite frankly are like plain english, if you know common mathematics or you have previous experience in other programming languages like c, c++, perl, C#, F#, Z#, Fortran, OCAML, Crystal, Obj-C, Swift or other languages like those then you should be able to grasp them and the different categories, if not let me explain.

In programming there are multiple fields of data types such as the following 

**Basic data types**

this branches off into 

```
| Integers 
| Strings and characters 
| Booleans (true or false)
```

**Aggregated types**

these branch off into 

```
| Arrays
| Structures 
```

**Reference types**

these branch off into 

```
| Pointers
| Slices
| Maps
| Functions
| Channels
```

### the XDR standard | signed and unsigned integers ###



When getting into data types alot of the way data types are made inside of a programming language are based on the XDR standard which is defined as the external representation of data or `External Data Representation`. This standard is the standard protocol for the description and encoding of data, it allows us to say and proove the difference between a signed and a unsigned integer. When you start compiled languages you deal lots with bits and type bits such as 32, 8, 16, 64, etc for example in go you have the following bits and integer data types 



| Data type decleration | Bits allowed  | Full name of representation | Description                                                                  |
| --------------------- | ------------- | --------------------------- | ---------------------------------------------------------------------------- |
|        int8           |  8            | 8 bit signed Integer        |  8-bit integers or other data units are those that are 8 bits wide (1 octet) |
|        int16          |  16           | 16 bit SIGNED Integer       |  numerical tags where variables have the potential for negative or positive  | 
|        int32          |  32           | 32 bit SIGNED Integer       | 32-bit. This means that the number is represented by 32 separate one’s and zero’s. 32 bits of 2 possible states = 2^32=4,294,967,296 possible values. | 
|        int64          |  64           | 64 bit SIGNED integer       | 	A 32-bit signed integer. It has a minimum value of -2,147,483,648 and a maximum value of 2,147,483,647 (inclusive).|
|        uint8          |  8            | 8 bit UNSIGNED Integer      |  Unsigned whole or natural numbers ranging from 0 to +255 can not be 0/-255  |
|        uint16         | 16            | 16 bit UNSIGNED Integer     | Unsigned whole or natural numbers ranging from 0 to +65535                   |
|        uint32         | 32            | 32 bit UNSIGNED Integer     | a 32-bit datum that encodes a nonnegative integer in the range 0 to 4294967295 | 
|        uint64         | 64            | 64 bit UNSIGNED Integer     | has a minimum value of 0 and a maximum value of (2^64)-1 (inclusive)         | 


there is a clear difference between unsigned and signed integers, in summary the difference between a signed and unsiged is defined by the XDR standard below.

The XDR standard defines signed integers as integer. A signed integer is a 32-bit datum that encodes an integer in the range [-2147483648 to 2147483647]. An unsigned integer is a 32-bit datum that encodes a nonnegative integer in the range [0 to 4294967295].

The signed integer is represented in twos complement notation. The most significant byte is 0 and the least significant is 3.

for a better representation see here by IBM for more info `https://www.ibm.com/docs/en/aix/7.2?topic=types-signed-unsigned-integers`


### Implimenting Unsigned and Signed integers in go ####

go is very specific with data types as i have said more than enough times, which means you can not disobey the rules behing signed and unsigned integers. say you want to define a netmask for an IP address, you would want to use uint8 because this allows numbers to the limit of 255 and nothing more, if we define the constant as a uint8 but say have a false netmask of 298 which is invalid go will error out and say this is the wrong data type for the job. let us look at some decent examples of using data types and whats a wrong code example and a right code example


#### uint 8 wrong and right example ####

**WRONG**

```go
const mask uint8 = 2558 // go will error out and say cannot use 2558 (untyped int constant) as uint8 value in constant declaration (overflows)
```

the term `overflows` means it overflows the dimension of that decleration. for example the dimension of the variable `uint8` would be `255` if that dimension exceeds `255` then uint8 is clearly unfit for the job. a correct representation of this would be 

**CORRECT**

```go
const mask uint8 = 255
```

#### uint16 wrong and right example ####

**WRONG**

```go
const number uint16 = 650000 //cannot use 650000 (untyped int constant) as uint16 value in constant declaration (overflows)
```

**CORRECT**

```go
const number uint16 = 650000 
```

#### uint32 wrong and right example ####

**WRONG**

```go
const age uint32 = 6500000000 // cannot use 6500000000 (untyped int constant) as uint32 value in constant declaration (overflows)
```

**CORRECT**

```go
const age uint32 = 650000000
```

you get the idea right? Data types when it comes to signed and unsigned integers may be confusing however they can for sure come easy to you! 


### basic data types and basic implimentation ### 

**IN case you forgot**


BASIC DATA TYPES 

this branches off into 

```
| Integers 
| Strings and characters 
| Booleans (true or false)
```

lets start off with strings, golang has no concept of a char it rather uses byte and rune to represent character values but we wont get into those right now. Lets start working with strings and continue with go along the way. 

lets make a program to say hello to someone based on a name by using the string data type to define the function argument along with its type so it can be formatted.

**Function arguments**

Function arguments in go are quite simple, just define the function name followed by a data type for example our function will be 

```go
func hello(name string) {} // defines the variable name as a function argument with a data type of string
```

this means this function can now accept only ONE variable and that variable or argument MUST be a string.

Side note: this is often in older terms defined as a dimension of a function or subroutine. When you say a function can take 4 or 5 values you can say that function has a dimension of 5, for those who are new to that term in a sense and summary a dimension is just the arguments an array can take, and in this case our functions `()` can be represented as an argument array, and the dimension of that array is technically infinite however we can limit how much the dimension allows and in this case its one. The program does not limit this until the user limits it. 

**Making our program**

take the following file 

*main.go*

```go
package main 

import  "fmt"

func Writer(name string) string {
	message := "hello there %s"
	formatted_message := fmt.Sprintf(message, name)
	return formatted_message
} 

func main() {
     a := Writer("jake")
     fmt.Println(a)
}
```


in this code brick we use a function called writer, this function will be the main building block of our program defined with an argument defined as `name` with a data type of string, and outside of the `()` is another data type `string`, anytime you define a single or multiple data types outside of the `()` in a function you are telling that function to return a value. then after the brackets we define a variable named message with a value of `hello there %s`, the `%s` is like a placeholder / format sign, like a function it acts as an argument. 

then we define `formatted_message` which defines a function called `Sprintf`, the `Sprintf` function allows us to utilize the `%s` or like symbols and insert values into it. so when we use `fmt.Sprintf(message, name)` we are telling the program to insert the value of the function argument `name` into the variable `message` which before we return it looks like `hello there jake` since when we call the function in our main block we define the argument to be `"jake"`

now we use the `return` keyword in the function to tell us to return a variable of type string which in this case is `formatted_message`

we call our main block and assign a variable `a` with the value of the output returned from a function. When we define or assign a variable like the one in our program to a function, the variable `a` will hold the output and results of that function, then we print it. when  we run our program 

```
go run main.go
```

we get 

```
> hello jake 
```

** Defining and returning multiple values in a function **

lets make a function where we can allow the user to input a integer as an age and a name as a string but also return a message and a integer of a string.

okay okay woah that was a brain fuck sorry about that LOL

what i mean is our function will look like this 

```go
func Ret_Age_and_Name(name string, age int) (string, string) {}
```

the string will be an integer? yeah, we will use type conversion to return the integer as a string using the strconv package by go! so lets use that 

take the following function and code block 

```go
package main

import (
   "fmt"
   "reflect"
   "strconv"
)

func Return_Function(name string, age int) (string, string) {
	message := "%s is %d | just %s the age limit"
	tf_value := age < 18
	switch tf_value {
	case true:
		message = fmt.Sprintf(message, name, age, "below the legal")
		break
	default:
		message = fmt.Sprintf(message, name, age, "above or at the legal")
		break
	}
	s := strconv.Itoa(age)
	return message, s
}


func main() {
	a, b := Return_Function("jake", 17)
	fmt.Println(a)
	fmt.Println("Data type of the age which was first a integer -> ", reflect.TypeOf(b))
}

```


i suprised you there didnt i? i went from showing small functions to a weird ass function that may or might not be new to you let me explain. so first we define our function as Return_Function which holds to arguments which are `name` of data type `string` and `age` of data type integer. we then define that the function MUST return two variables of type string. `(string, string)` 

we kick the function off by defining a variable names `mesage` with the value `"%s is %v | just %s the age limit"`, the %s will be the name, the %v will be the age `%d` representing a integer formatter and another %s for another string statement. We then impliment boolean logic, if you do not know boolean logic is true or false or 1 and 0. we make this logic by declaring a variable followed by `age < 18` this variable now either holds true or false depending on our function argument, if the age is greater than 18 then it will come back false, if it is below 18 then it will be true because age in that case would be LESS THAN `<` or equal to `=<` the number or integer `18`.

we create a switch statement which is like a better way than if statements, we can say something like this 

```go
if age <= 18 {
   // do something
}
if age >= 18 {
  // do something
}
```

however i always urge people to stay as far away from if statements as you can. anyway this switch statement tells us that if the statement was true which means the age was NOT equal to or greater than 18 then to format the following message 

```go
		message = fmt.Sprintf(message, name, age, "below the legal")
		break
```

so now our variable message is 

```
jake is 17 | just below or at the legal the age limit 18
```

note we re define `message` with a `=` sign because we are CHANGING the variables contents and values. so instead of the message being empty and just `is | just the age limit`

it can now be 

`jake is 17 | just below or at the legal the age limit 18`




