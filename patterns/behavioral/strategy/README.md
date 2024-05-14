# Strategy Design Pattern

The Strategy design pattern is a behavioral design pattern that allows you to define a family of algorithms, encapsulate each one as a separate class, and make them interchangeable at runtime. This pattern enables the algorithm to vary independently from the clients that use it.

## Problem

In software development, there are often situations where you need to implement different variations of an algorithm or behavior. For example, consider a payment processing system that needs to support multiple payment methods such as credit card, PayPal, and bank transfer. Each payment method requires a different algorithm for processing payments.

## Solution

The Strategy design pattern suggests that you define a common interface for all the algorithms and implement each algorithm as a separate class. These classes are known as strategies. The context class, which represents the client, has a reference to one of the strategy objects and delegates the work to this object.

By doing so, the context class can switch between different strategies at runtime, depending on the specific requirements or configuration. This allows the client to be decoupled from the specific implementation details of the algorithms.

## Example

Let's consider an example where we have a `PaymentProcessor` class that needs to support different payment methods. We can define a `PaymentStrategy` interface that declares a method `processPayment()`. Each payment method, such as `CreditCardStrategy`, `PayPalStrategy`, and `BankTransferStrategy`, would implement this interface and provide their own implementation of the `processPayment()` method.

The `PaymentProcessor` class would have a reference to a `PaymentStrategy` object and delegate the payment processing to it. At runtime, we can easily switch between different payment strategies by changing the reference to a different implementation.
