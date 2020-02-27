# code design for level 2 and level 3 of chord trainer

These will be pared down versions of the code that I had set up for level 4. The main issue will be whether or not I [Lyn] want to copy the code and reimplement, or gate the possible outputs depending on the level choice. Right now we are leaning toward reimplementing the code, since Max/MSP is relatively inefficient anyway and the file size of an exported executable is already dwarfed by the Max runtime. This may be something to consider more if we change codebases but for now we will most likely do a simple copy paste of the data.

An issue we are running into as we expand the code is organization. As Max is a visual coding language we will run into organization issues as the size of the code increases. We may also run into runtime issues as max runs its code from right to left, which I did run into when I was coding version 0.1.
