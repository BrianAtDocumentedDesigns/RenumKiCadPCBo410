# RenumKiCadPCBo410
Version 410 has been significantly rewritten as I move towards KiCad integration. 
On the journey some bugs were reported (Thanks Alan!)

These bugs which were reported and fixed are:
1) Under some circumstances KiCad uses quotes around reference designations internally. This caused RenumKiCadPCB to 
treat each refdes as a different type. 

2) Renumbering by refdes didn't work. 

3) Selecting "Sort by Refdes" wasn't remembered after exiting the program even though "Sort by Modules"was. 

Also I added a reminder warning that you have to close other versions of the relevant .sch and .kicad_pcb files before 
renumbering. KiCad doesn't refresh externally modified files and I didn't see the benefit of sorting out file lock on
Windows, Linux, and Apple given I hope to integrate the code into KiCad and therefore the issue will be moot.
