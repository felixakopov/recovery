
### **Overview**
- Creational design
- A class only has one instance
- Global access to instance


### **How To**
- Make the default constructor private
- Create a static creation method for the constructor
	- This method calls the private constructor to create the object and save it in a static field
	- All following calls to this method return the cached object

![[Pasted image 20250918145122.png]]
![[Pasted image 20250918145653.png]]

