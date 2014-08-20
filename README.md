OSR-Reflection
==============

Candidate for Official SRL OSR Reflection, to be used with Simba(https://github.com/MerlijnWajer/Simba) and SMART(https://github.com/BenLand100/SMART).

Smart references are stored in an global array and then freed on script terminate(debugging will show what was leaked).
NOTE: All object loading functions allow the object to be named in the array, to help trace those elusive leaks.
The include will loosely follow RS's object hierarchy.
All objects loaded from the client will be extended from TRSObject, as it contains the pointer(smart reference) to the object.
Object accessors will be in the wrapper module, general use methods will be in the api module, and constants/hooks will be in data folder.
