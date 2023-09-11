# Why Swift

## Overview

Me: A college students self learned swift for about one year, and now a iOS dev intern.

Swift: A programming language I love pretty much, made by Apple, open source 🧐; good language but with limited usablity.

Video: No Mac/iPad requirement. Teach Swift, for programmer with basic knowledge of programming. I gonna not give some Apple exclusive examples.

## Topics

### JavaScript, Python, Java, C++

```Python
import numpy as np
import matplotlib.pyplot as plt

data = np.random.randn(1000)
hist, bin_edges = np.histogram(data, None, None, False, None, False, 'bar', 'mid')

plt.hist(data, None, None, False, None, False, 'bar', 'mid')
plt.show()
```

```JavaScript
const button = document.getElementById("myButton");

button.addEventListener("click", () => {
  const randomNumber = Math.random();

  if (randomNumber < 0.5) {
    console.log("You won!");
  } else {
    console.log("You lost!");
  }
});
```

```cpp
#include <iostream>
#include <functional> // Required for std::function

// Function that takes two lambda expressions and applies them to a value
int applyLambdas(int value, std::function<int(int)> lambda1, std::function<int(int)> lambda2) {
    int result1 = lambda1(value);
    int result2 = lambda2(value);
    return result1 + result2;
}

int main() {
    // Define two lambda expressions
    auto square = [](int x) -> int {
        return x * x;
    };

    auto doubleValue = [](int x) -> int {
        return x * 2;
    };

    // Pass the lambda expressions to the higher-order function
    int value = 5;
    int result = applyLambdas(value, square, doubleValue);

    std::cout << "Result: " << result << std::endl;

    return 0;
}
```

```Java
// Base class (parent)
class Animal {
    void speak() {
        System.out.println("Animal speaks.");
    }
}

// Derived class (child)
class Dog extends Animal {
    @Override
    void speak() {
        System.out.println("Dog barks.");
    }

    void fetch() {
        System.out.println("Dog fetches.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();
        animal.speak(); // Output: Dog barks.

        Dog dog = new Dog();
        dog.speak(); // Output: Dog barks.
        dog.fetch(); // Output: Dog fetches.
    }
}
```


```swift
public enum JSColor {
    case rgb(r: UInt8, g: UInt8, b: UInt8)
    case rgba(r: UInt8, g: UInt8, b: UInt8, a: Double)
}

public protocol FillStyle: ConvertibleToJSValue {}
extension JSColor: FillStyle {}
extension CanvasPattern: FillStyle {}
extension CanvasGradient: FillStyle {}

public extension CanvasFillStrokeStyles where Self: JSBridgedClass {
    @inlinable
    func set( strokeStyle: FillStyle) {
        jsObject[Strings.strokeStyle] = _toJSValue(strokeStyle)
    }
    
    @inlinable
    func set( fillStyle: FillStyle ) {
        jsObject[Strings.fillStyle] = _toJSValue(fillStyle)
    }
}
```

- <!--@START_MENU_TOKEN@-->``Symbol``<!--@END_MENU_TOKEN@-->
