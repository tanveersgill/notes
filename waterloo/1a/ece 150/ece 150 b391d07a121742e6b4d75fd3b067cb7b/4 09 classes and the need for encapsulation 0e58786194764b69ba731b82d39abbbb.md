# 4.09 classes and the need for encapsulation

Nothing special here, just that we should keep variables private so we may change the underlying structure of those variables whenever needed

- since the user interacts with the member functions this way and not directly with the variable, if we wanted to do something like combine three variables into an array, we can do that and just make the getter functions return array indices