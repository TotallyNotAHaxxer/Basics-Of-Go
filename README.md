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

pretty simple right? Now we went from assuming the data type of the constant to assigning it which can make it alot less bugy in the future when working with more higher end programs and functions.


  
