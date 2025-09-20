
### **Overview:**
- Structural pattern
- Lets you attach new behaviors to objects by placing them inside wrapper objects for the behaviors

### **Problem:**
Typically, extending a class will help with altering an object behavior, but that can be an issue if you want to altar the behavior at runtime or if there are subclasses/multiple classes.

- Aggregation or Composition could help instead of using Inheritance
- ![[Pasted image 20250918160308.png]]

A wrapper is an object linked to a target object that contains the same set of methods as the target but may alter the result by doing something before/after passing request to target.
- Implements same interface as wrapped object
- Client sees objects as identicle
- Wrapper's reference accepts any object that follows that interface
- Can cover object in multiple wrappers

![[Pasted image 20250918160656.png]]
![[Pasted image 20250918160703.png]]

![[Pasted image 20250918160719.png]]
![[Pasted image 20250918160729.png]]

![[Pasted image 20250918160738.png]]

[Pseudocode can be found here.](https://refactoring.guru/design-patterns/decorator)


### **How To:**