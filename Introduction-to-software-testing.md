# An Introduction to Software Testing #
## A Definition ##

Our friends at the [English Oxford Living Dictionaries](https://en.oxforddictionaries.com/definition/test) describe the noun test as follows:
** *A procedure intended to establish the quality, performance, or reliability of something, especially before it is taken into widespread use.* **

This definition captures the essence of why we test and is very relevant to code. It hints at checking to make sure a product works as expected before leaving the factory. In the world of Software Testing, we extend this notion of quality checking as follows:

*a procedure intended to establish* **and maintain** *the quality, performance, or reliability of* **a piece of software or a solution** *, before being taken into widespread use* **and before shipping updates into widespread use.**

## Types of Testing ##

The type of testing we perform is defined by what we are trying to test. Consider the following, simplified, representation of a software system.
![Image](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/47af17b0deb038cda586ae3a1393df03/asset-v1:Microsoft+DEV275x+1T2018+type@asset+block/software-system.png)

This diagram illustrates a typical set of components and relationships in any software system. We can list the components/actors as follows:

* **My Code** - the code that is under the direct responsibility of the developer.
* **Software Components** - represents libraries, components, services the developer uses to implement functionality. My Code depends on these components.
* **Software Solution** - represents the package/product that ships. This is what human and software (service) consumers see and interact with. The developer's code is, at the very least, a subset of the solution being shipped.
Since many components are involved here, each with a defined relationship to other components, we need to determine how 
best to verify that everything works as expected and that this quality is maintained. For example, we said that My Code 
represents the code that is under the direct responsibility of the developer. He or she may be writing this code from scratch 
or may, as we've seen earlier in this course, have inherited code or a project that must be maintained. It contains functionality - classes, methods, properties, events. The developer must be able to verify that the code does what it said it would do and behaves in a predictable manner even under error conditions. The following table summarizes the different relationships represented in this software system and the type of testing that could be used to determine quality and other important traits.

| Relationship | Definition | What to test | Type of Test |
| ------------ | ---------- | ------------ | ------------ |
| A            | My Code contains functionality that is written, or maintained, by the developer. | Correct operation of the functionality. | Unit Testing |

