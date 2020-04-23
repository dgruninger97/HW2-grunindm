# CSSE374 Homework 2 - Part 1

## Strategy Pattern

Date: 4/22/2020

### Candidate Design 1: 

For candidate design 1, we should consider using the Strategy Pattern for the the new interagration methods that are being provided to our system. We could create
a class, called IntegrationStrategy, which would replace the "integrationMethod" string that is currently passed into the integrate method. That way we could simply
call that IntegrationStrategy's integrate method, and it would call the appropriate strategy pattern to handle the proper integration.

#### Pros

This will eliminate having to check what type of integrationMethod that the integrationMethod String was (located in Integrate()).
Also, this apply's the principle of separating what changes from what stays the same. We know that the integration method will continue to change, so it makes
sense to extract out that behavior using the strategy pattern. Finally, this will allow our system to **adapt to change**, as we can add more implementations of
the IntegrationStrategy when the customer requests a new integration method.

#### Cons

Will require us to significantly change our integrate method, and how we are calling that method. This is because we are now passing in a strategy instead of a
 string to represent our actual integration methods.

### Candidate Design 2: 

For candidate design 2, we could try making the actual NumericalIntegration class a Strategy, and have the classes that implement the Strategy have their own
integrate function. This eliminate the need for the IntegrationMethod class, as NumericalIntegration classes would have different versions which would each
perform a different type of numerical intergration.

#### Pros

Could get rid of an entire class and just do the work in the NumericalIntegraiton strategies. Different strategies will have their own integrate methods and be
able to perform different forms of integration, per the customer.

#### Cons

This also may require **significant** change in the other parts of the system in order to properly adapt to removing an entire class. Additionally, this will mean
that we will have to move where the integration is being done, since now the NumericalIntegration class is responsible for doing the specific integration, and will
no longer have the integrate() method. This could lead to more design problems in the future.

### Design Preference

I prefer candidate design 1. I believe it does a better job **separting what changes from what stays the same.** Additionally, I think it will be less of a hassle
for us to maintain, since all we would have to do is add another integration method strategy when the customer wants something else. **No other code will have
to change.** It is simple a matter of adjusting our initial program to be able to handle the strategy pattern instead of using strings to parse the integration
type.

### Class & Sequence Diagram Sketches

Class Diagram:

![Strategy Class Diagram](images/StrategyClassDiagram.png)

Sequence Diagram:

![Strategy Class Diagram](images/StrategySequenceDiagram.png)

### Citations

https://sourcemaking.com/design_patterns/strategy

https://refactoring.guru/design-patterns/strategy


### Time Spent -- 2 hours

## Observer Pattern

Date: 4/23/2020

### Candidate Design 1

#### Pros


#### Cons


### Candidate Design 2

#### Pros

#### Cons