[[Programming languages]]
Any decent programming language provides these building blocks in some way:
- "Each-Of": A compound type $t$ describes values that contain each of values of type $t_1, t_2, ..., t_n$
- "One-Of": A compound type $t$ describes values that contains a value of one of the types $t_1, t_2, ..., t_n$
- "Self-reference": A compound type $t$ may refer to itself in its definitions in order to describe recursive data structures like lists and trees

Each-of example: `int * bool` (tuple contains int and bool elements). Java/C# class is the same sort of thing
One-of example: Describes the value that contains `bool` or `int`
Self-reference example: `int list` describes values that either contain nothing or contain an `int` and another `int list`. A list of integers in any language can be described in terms: `or`, `and`, `self-reference` 