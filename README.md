See Wiki page for assignment:
https://github.com/vividdev/light-resolver-dev/wiki/Assignment

### Code Structure
Solution contains some code already included:

#### LightResolver.Logic
This project should contain the optimization logic you'll be implementing. You should mostly modify this project. See class LightResolverModule method OptimizeComposition with TODO comments the starting point of code modifications. Note that these are only guidelines, you can approach the assignment however you like.

Notable Types:
- *ILightResolverModule* should be used to implement the optimization logic.
- *Composition* Model class used as basis to represent the product component hierarchy.
- *OptimizationResult* can be used to see how the electrical component division has been done.

Much of the premade code relies on Composition model class. At the start this class and underlying component hierarchy should be generated by an IInputProvider. After/During optimization logic, you should modify this model hierarchy to insert ShelfTypes, WallTypes and wattage consumption for each OuterWall. The types are used by the test cases via OptimizationResult to check the power consumption, correctness and price of the composition.

So, basically at the start you are provided a composition object which represents the shelving product with all the components and lights. Your task is to modify it to include all the type codes for shelves and outerwalls and power consumption each outer wall. Optimization logic should decide the type of components by getting the cheapest total price. 

Added IInputProvider to give composition model creation some structure. It's not mandatory to use this, you can create compositions however you like.

##### 

#### LightResolver.API
Optional module. Web interface uses NSwag libraries to provide easy web interface to execute optimization logic. For testing and development purposes.

#### LightResolver.Tests
These are premade unit tests for the optimization logic. The goal is to pass these tests. Currently there's not many of these. You can write your own tests for better coverage of the task.