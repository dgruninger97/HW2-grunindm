# CSSE374 Homework 2 - Part 1

## Strategy Pattern

Date: 4/22/2020

### Candidate Design 1: 

For candidate design 1, we should consider using the Strategy Pattern for the the new interagration methods that are being provided to our system. We could create
a class, called IntegrationStrategy, which would replace the "integrationMethod" string that is currently passed into the integrate method. That way we could simply
call that IntegrationStrategy's integrate method, and it would call the appropriate strategy pattern to handle the proper integration.

#### Pros

This will eliminate having to check what type of integrationMethod that the integrationMethod String was (located in Integrate()).

#### Cons

### Candidate Design 2: 

For candidate design 2, we could try making the actual NumericalIntegration class a Strategy, and have the classes that implement the Strategy have their own
integrate function. This eliminate the need for the IntegrationMethod class, as NumericalIntegration classes would have different versions which would each
perform a different type of numerical intergration.