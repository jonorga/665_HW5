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


## Where could another class be easily added? Why is that useful?

