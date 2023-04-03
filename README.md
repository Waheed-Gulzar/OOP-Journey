# OOP-Journey
Studying in fast islamabad. 


# OOP concepts 

## Virtual Destructors 
Assuming that both base and derived classes have virtual destructors, when the delete operator is called on a pointer to a base class (base*) that points to an object of the derived class (derived), the derived class's destructor will be called first, and then the base class's destructor will be called.
This is because the destructor of the base class should be virtual. When a class has a virtual destructor, the compiler generates a virtual table (vtable) that contains a list of virtual function pointers, including the destructor. When a derived class overrides the virtual destructor of the base class, it provides its own implementation of the destructor, which is called when the object is destroyed.
In this case, since the delete operator is called on a pointer to the base class, the destructor of the derived class will be called first, since it overrides the base class's virtual destructor. Then, the base class's destructor will be called.
This ensures that all the destructors in the inheritance hierarchy are called in the correct order and that any resources allocated by the derived class are released before the base class is destroyed.

## Virtual and pure virtual

![virtual and pure virtual](https://user-images.githubusercontent.com/124068732/229597832-1fa812b0-d473-4d63-b311-e767300cc709.PNG)
