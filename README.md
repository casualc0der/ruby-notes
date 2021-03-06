# Ruby Notes


## Chapter 1 

* Ruby or ruby, never RUBY
* Use RVM, rbenv or chruby to install Ruby
  * [RVM](https://rvm.io/)
  * [rbenv](https://github.com/rbenv/rbenv)
  * [chruby](https://github.com/postmodern/chruby)
* Windows users encouraged to use the RubyInstaller
  * [RubyInstaller](https://rubyinstaller.org/)

Practice files will be saved in this Repo

irb is Rubys REPL, great for trying out code snippets and prototyping quickly. Simply type 'irb' at the command line 

```
$ irb
```
And the REPL will open ready for commands 

```
2.7.0 :001 >

```

Type 'exit' or Ctrl-D to go back to the command line.

Ruby uses standard operators + - / * etc

Everthing is an object (mostly). Ruby passes messages around the program using method calls. 

Method calls (messages) are invoked on an object by using the dot . notation. In the example below, we send the message to the String object that we would like Ruby to convert it into an Integer. 

```
"100".to_i
```

To get a list of available messages that you can send to an object, you can type `Object.methods` in the irb

Classes are used as a template for bbjects. They instantiate (create) an object with a set of pre-defined attributes and methods.

**Methods can be added to objects after they are instantiated!** Just think of classes as the DNA of objects, but we can teach the newly born object to speak with methods :baby_chick:

Before running a Ruby program you can check the syntax by running the below command

```
$ ruby -cw testfile.rb
```
* -c checks for syntax errors
* -w checks for formatting issues

### **Simple** File I/O

Read from a file: `x = File.read("test.dat")`

Write to a file `file = File.new("test.out", "w")`

Ruby config can be used to scout through the Ruby source code. 

```
$ irb --simple-prompt -r rbconfig
```
```
>> RbConfig::CONFIG["_HASHKEY_"]
```

HASHKEYS to check the file paths of Ruby source files 


HASHKEY | Contents |
--------|----------|
 rubylibdir | Ruby standard library|
 bindir | Ruby command-line tools| 
 archdir | Architecture-specific extensions and libraries (compiled, binary files)| 
sitedir |Your own or third-party extensions and libraries (written in Ruby)| 
 vendordir |Third-party extensions and libraries (written in Ruby)|
 sitelibdir |Your own Ruby language extensions (written in Ruby)|
 sitearchdir | Your own Ruby language extensions (written in C)|
 




 
