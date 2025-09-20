[Video Explanation 1](https://www.youtube.com/watch?v=HQLXUyb0T2w&ab_channel=ShivKumar)


#### **Overview:**
- Creational
- Isn't polymorphic
- Treats all descendant classes in a family uniformly
- Delegates construction of descendants to the Factory class


#### Factory Class:
- Static class
- One method - create instance
	- Takes identifier as argument
	- Returns the base class of that family


**Example:**
- Business wants to set specific rules applicable to state X
	- State X is the identifier
	- Returned = rules that apply to that state


#### Code Example:
![[Pasted image 20250916212144.png]]
![[Pasted image 20250916212242.png]]

Starting off with the family code that's already been defined, unrelated to the factory class.

In the main program you'd call
`ThumbnailerBase thumbnailer = ThumbnailerFactory.CreateInstance(MimeType.Audio);`
which would, once creating the factory class, call the `CreateInstance` method with the identifier `MimeType.Audio`.

Below: `thumbnailer.CreateInstance(null);`


The factory class itself can them be created, which will be static, since it will not be changing when instantiated.

The factory class will always return the base class.
- Switch statement can be used within CreateInstance to return the correct descendant.

![[Pasted image 20250916213049.png]]

This helps because:
- Maintains client blindness to descendant information, abstracting and decoupling the client code from descendants