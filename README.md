# definition
The language definition for orchid

# Syntax

Semi-colons are optional, so if you see them used sometimes but not always thats why.

## Functions

Functions are defined using this syntax
```orchid
start function name takes () gives ()
defined as {} end
```

In this the function name would go where `name` is.
Takes is the arguements a function accepts. This is how it is supposed to look `(type param: default)`.
Gives is the types the function can return. For example, here is a function called helloworld it takes an integer as input, then returns a string or another number.
```orchid
start function helloworld takes (int given: 0) gives (string, int)
defined as {
  if (given == 0) then {
    return "Hello";
  } end
  if (given == 1) then {
    return "World";
  }
  return given + 5;
}
end
```

## lambda functions

A lambda function works like `start lambda define as {} end`. It may not take any arguements.
There is a shorthand for when used in an if statement, read about that in the if statement section.

## if

The if statement works as follows `if (condition) function`
This can be donne with a function name `if (condition) helloworld`. However you can't parse arguements like this.
Instead you can use a lambda function, or the shorthand `then`. For example:
```orchid
if (1 + 1 == 2) start lambda define as {
  print("Lambda functions!")
} end

if (2 + 2 == 4) then {
  print("Wow! Still a lambda function!")
} end
```

In this scenario, `then` is just shorthand for `start lambda define as`


