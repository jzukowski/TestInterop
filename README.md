# TestInterop
create a c# interop wrapper from a c file using SWIG

1. open a terminal window and go to /testInterop/cFiles directory
2. run the following SWIG command on the interface file:
'''
swig -csharp example.i
'''
This will generate the following files: 'example.cs', 'examplePINVOKE.cs', and 'example_wrap.c'.
3. compile the wrapper code by using the following command:
'''
gcc -c -fpic example.c example_wrap.c -I/usr/include
gcc -shared example.o example_wrap.o -o example.dylib
'''
4. Copy the 'example.cs', 'example.dylib', and 'examplePINVOKE.cs' files into the root of your c# project








