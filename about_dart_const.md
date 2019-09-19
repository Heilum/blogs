## Something about Dart's const

First,let's look at this code snippet

```
void main() {
  var constantList = const [1, 2, 3];  // line 1
  //constantList[0] = 1;               // line 2
  constantList = [50];                 // line 3
}
```

When you paste the above code in [DartPad](https://dartpad.dev), it can be compiled without any error.
Line 1 tells us that the "const" keyword declares a constant array and because 'constantList' is a variable,we can let it refer to 
another array(line 3).

If we uncomment line 2, the code can't be compiled because 'constantList' refers to a constant array and we can't change the elements
of this constant array.
