# static::foo

In PHP, `static::foo` is a way to call a static method `foo` from within a class hierarchy. This usage is part of the
late static binding feature, which allows you to reference a class's methods and properties based on the context of the
calling class rather than the class in which the code is written.

Here's how `static::foo` works:

1. **Late Static Binding:**
   In object-oriented programming, late static binding refers to the ability to reference a static method or property
   based on the class that is calling it at runtime. This is useful when you have a class hierarchy with inheritance and
   want to invoke methods dynamically based on the calling class.

2. **Using `static::` to Call a Static Method:**
   When you use `static::foo` within a class method, it calls the static method `foo` based on the class that's
   currently calling the method, rather than the class in which the code is written. This is especially relevant in
   situations where the method might be overridden in subclasses.

Here's an example to illustrate the concept:

```php
class ParentClass {
    public static function hello() {
        echo "Hello from ParentClass!";
    }
}

class ChildClass extends ParentClass {
    public static function hello() {
        echo "Hello from ChildClass!";
    }

    public static function callHello() {
        static::hello(); // Calls the appropriate hello() based on the calling class
    }
}

ChildClass::callHello(); // Outputs: Hello from ChildClass!
```

In this example, when `callHello()` is called from `ChildClass`, the `static::hello()` call resolves to the `hello()`
method of `ChildClass` due to late static binding.

It's important to note that `self::foo` would not have the same behavior. Using `self::foo` would always refer to
the `foo` method defined in the class where the code is written, regardless of the calling class.

Late static binding is particularly useful when you have a class hierarchy and you want to ensure that overridden
methods in subclasses are invoked correctly based on the calling class.