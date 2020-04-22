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
sense to extract out that behavior using the strategy pattern. Finally, this will allow our system to adapt to change, as we can add more implementations of
the IntegrationStrategy when the customer requests a new integration method.

#### Cons

Will require us to significantly change our integrate method, and how we are calling that method. This is because we are now passing in a strategy instead of a
 string to represent our actual integration methods.

### Candidate Design 2: 

For candidate design 2, we could try making the actual NumericalIntegration class a Strategy, and have the classes that implement the Strategy have their own
integrate function. This eliminate the need for the IntegrationMethod class, as NumericalIntegration classes would have different versions which would each
perform a different type of numerical intergration.