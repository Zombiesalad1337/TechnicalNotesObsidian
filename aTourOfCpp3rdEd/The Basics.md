non-zero `main()` return value -> Error code.
Linux/unix environments make use of this return val, windows one dont.

```cpp
import std; //import directive new in c++20

int main(){
	std::cout << "hell world"`
}
```
operator `<<` ("put to") writes its second argument into its first.

`import` directive - instructs compiler to make the declarations of standard library available. But presenting all of std library as a module is not yet standard.

### Functions

Function declarations do not need argument names. They are ignored by the compiler.
`double sqrt(double);`

type of a function = return type + **sequence** of argument types
`double get(const vector<double>& vec, int index); // type: double(const vector<double>&,int)`

For member function, type includes class.
`char& String::operator[](int index); // type: char& String::(int)`

>Turning a piece of computation into a function forces us to:
	1. Name the activity.
	2. Document its dependencies.
   If you cannot find a suitable name, then most likely you have a design problem.


More + shorter functions ~= less buggy code

#### Overloaded functions
**Overloaded functions** should implement the **same** **semantics**.

Compiler chooses the most appropriate overloaded function based on argument types.

If two alternative overloaded functions can be called, but neither is better than the other, then the call is deemed ambiguous and compiler gives an error.

```c++
void print(double, int);
void print(int, double);

void user2(){
print(0, 0) //error: ambiguous
}
```
