# Test_demo_std_ptional_vs_pointers
two pieces of code demonstrating some use of std::optional of std::reference_wrapper vs the same functionality achieved traditionally through using pointers, combined with standard library containers


Class CAnimal: abstract class: 
an animal can or cannot eat another animal and can or cannot be eaten from another
Herbivore cannot eat another animal
Carnivores can eat only herbivores
Ferocious can eat both herbivores and carnivores, except animal of its species
Cannibals can eat every animal except itself
The code sample below implements this:
You cannot place place animals that can be eaten in the same shelter with animals that can eat them (except you expect to be be used as food, for example but the example doesn't cover this case)
If you made a new shelter, the type of the shelter is auto set after the type of the first animal placed out there (if the first animal ever placed there is herbivore, then is a herbivore shelter and you cannot place any carnivore after that, if you place a carnivore, you cannot place any herbivore nor ferocious,  etc)
The shelter looses its type when empty
The code tries to avoid an animal to figure at the same time in two or more different shelters
An animal with no shelter is however possible

The derived: herbivores, carnivores etc (described above)

The code tries to explain and copmare the pointer case (when a shelter contains pointers of the animals it contains) or optional references instead
