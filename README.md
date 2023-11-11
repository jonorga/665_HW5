| CS-665       | Software Design & Patterns |
|--------------|----------------------------|
| Name         | Jonathan Organ             |
| Date         | 11/11/2023                 |
| Course       | Fall                       |
| Assignment # | 5                          |

## Identified patterns
- Adapter
- Facade
- Composite

## Identify the classes/interfaces in the patterns
#### Adapter

| Name in Pattern | Name in Repo      |
|-----------------|-------------------|
| ConcreteAdapter | JUnit4TestAdapter |
| Adapter         | Test, Filterable, Orderable, Describable|
| Adaptee         | SimpleTest, ListTest |

#### Facade

| Name in Pattern | Name in Repo      |
|-----------------|-------------------|
| Facade          | JUnit4TestCaseFacade|
| Component       | Describable, Test |

#### Composite

| Name in Pattern | Name in Repo      |
|-----------------|-------------------|
| Component       | Test              |
| Composite       | TestSuite         |
| Leaf            | TestCase          |


## How do the classes/interfaces in the source code collaborate?
#### Adapter
- The JUnit4TestAdapter class acts as the concrete adapter, taking the Test, Filterable, Orderable, and Describable interfaces as the Adapter interface. This allows classes such as SimpleTest and ListTest to use the JUnit4TestAdapter class and run JUnit 3 style tests in JUnit 4.

#### Facade
- The JUnit4TestCaseFacade class hides the complexity of the Describable and Test interfaces. Instantiating the JUnit4TestCaseFacade class allows for using these methods with greater simplicity.

#### Composite
- The TestSuite and the TestCase class implement the Test interface, This allows for the client to access or address either the TestSuite or the TestCase class individually, or by assigning the variable to type Test and treating both TestSuite and TestCase uniformly. 


## Where could another class be easily added? Why is that useful?
#### Adapter
- Classes could easily be added to the adapteee area of the pattern, this would be useful as it would let more classes adapt JUnit 3 test to the style of JUnit 4.

#### Facade
- Interfaces could be added to the JUnit4TestCaseFacade class to add in additional functionality. This would be useful because it would allow for the expansion of JUnit4TestCaseFacade class functions without increasing complexity.

#### Composite
- Other leaf classes could be added as long as they implement the Test interface. This would be useful as it would allow the client to address that class individually or all the Test classes uniformly.

## File locations in repo
| Name  | Location in Repo      |
|-----------------|-------------------|
|JUnit4TestAdapter |main/src/main/java/junit/framework/JUnit4TestAdapter.java |
|ListTest | main/src/test/java/org/junit/samples/ListTest.java |
|SimpleTest|main/src/test/java/org/junit/samples/SimpleTest.java |
|Test|main/src/main/java/junit/framework/Test.java|
|Filterable|main/src/main/java/org/junit/runner/manipulation/Filterable.java|
|Orderable|main/src/main/java/org/junit/runner/manipulation/Orderable.java|
|Describable|main/src/main/java/org/junit/runner/Describable.java|
|JUnit4TestCaseFacade|main/src/main/java/junit/framework/JUnit4TestCaseFacade.java|
|TestSuite|main/src/main/java/junit/framework/TestSuite.java|
|TestCase|main/src/main/java/junit/framework/TestCase.java|