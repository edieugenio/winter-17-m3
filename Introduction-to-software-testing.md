# An Introduction to Software Testing #
## A Definition ##

Our friends at the [English Oxford Living Dictionaries](https://en.oxforddictionaries.com/definition/test) describe the noun test as follows:
***A procedure intended to establish the quality, performance, or reliability of something, especially before it is taken into widespread use.***

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
| A | My Code contains functionality that is written, or maintained, by the developer. | Correct operation of the functionality. | Unit Testing |
| B | My Code depends on software components. This is code the developer is not maintaining. | The functionality our code depends on works. | Functional Testing |
| C | My Code is used in a software solution. It may be a subset of the solution, or the complete solution being shipped | Verify that the group of components that are combined to form the software solution function correctly together to produce the desired output. | Integration Testing, System Testing |
| D | Our solution is consumed by humans and software. | Verify that the solution behaves as expected both in terms of functional accuracy and also in terms of desired experience | Integration Testing, System Testing, Usability Testing, Beta Testing |

As you can see from the preceding table, the boundary between each part of our software solution is validated using different test types to verify everything is in working order. The Quality Control checks done on a factory floor operate in a similar manner. Often each testing "station" is responsible for verifying one aspect of the entire "product" and a seal of quality is given to the product when it makes it through all of the stations or "quality gates". In software, we can repeat this process for our code by setting up some automation to run each test gate when, for example, a significant commit is made to the code in our master or developer branch.

A primary tool in the developer's toolbox to make sure code quality is verified and maintained is the Unit Test. We'll spend a lot of time in this module diving deeper into this testing type.

The preceding table does not cover all types of testing that have evolved over the years. Some other testing types include:

* Performance Tests - tests designed specifically to help us measure the throughput of a part of our system. An analogy is measure how fast we can push water through a pipe.
* Stress Tests - tests designed to observe what happens to our software under a heavy load or stress. This is equivalent to measuring how much water we can push through a pipe before the pipe bursts.
* Beta Tests - this is typically the name given to a program or period of time when a select subset of users are given an opportunity to try the software application, or service, and give feedback before the final release is completed and delivered.
* Fuzzy Tests - testing the behavior of a software system or program, by inputting large amounts of random data and watching for crashes, unexpected behavior and unexpected resource usage, such as memory leaks.
* A/B testing - If you have ever seen TV commercials for taste tests between two soda brands then you have seen this kind of testing in action. Users are split into (at least) two groups and interact with similar, but different, versions of your software. The goal is to measure the impact the subtle differences in behavior, design and User Experience (UX) in each version have on the satisfaction of the customer.

As you progress in your career as a Software Developer, you'll come across many of these test types and may even be involved in building test harnesses for them. In this course, however, we'll focus on writing Unit Tests, since these are very much about verifying the code we own or write. That said, there are a set of characteristics that all test types share and we'll take a look at those next.
