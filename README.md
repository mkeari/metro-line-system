# Metro-Line-System
The implementation of Metro Line using Ladder Logic Diagram in CODESYS software.

[![Demo](https://img.youtube.com/vi/aJh3SQjZNfQ/0.jpg)](https://youtu.be/aJh3SQjZNfQ)

## General Info

Underground system represents tightly interconnected system, where each operation command has effect on the overall system; additionally system can be subdivided into task groups according to assigned task. This model can be viewed from the perspective of the underground system operator, however it also provides the necessary information to potential passengers. Some additional safety features such as door closing prevention and emergency stop are exploited.

CODESYS programming environment allows to exploit functions and as well as visualizations required to successful accomplishment of above-mentioned project. Structure text PLC programming language was chosen, due to it’s intuitiveness in comparison with alternatives; besides, although LLD (ladder logic diagram) is visually more convenient, such a complex system will create a significant amount of distractions, and will prevent focus concentration

<img src="/images/metro-line-map.png" alt="Metro Line Map" width="350"/>

Figure above demonstrates the final visualization implemented in CODESYS, it includes 4 stations with time boards on them, train control boards and moving train visualizations.

## Implemented logic conditions and functions

Design process of this system included, perspective of the train operator as well as general passenger view and experience that he/she has or could have or see in the generic tube line. Also some more specific functions were considered as potentially usable for instance the door closing mechanism that is implemented in most of the metro lines.

- For train to begin ride operator must manually press the ’Go’ button, and will go with constant speed
- Trains operate in a closed loop
- Trans are on the two parallel lines from each other
- Train visualization is implemented via images and door visualization is also crucial part of the code
- When Emergency stop is pressed, operator will not be able to press ”Go” on both trains
- If Photo Eye is activated doors will not close for some amount of time
- If some object is located between the doors, they will not be able to close. Then it will automatically
    wait for 3 seconds, and will try to close again. In case if some object appears again, logic will repeat
    itself, till there will be nothing
- Stations are designed in such way, that distance and respectively time for train to get to some
    station are not equal
- Operator and passengers will have information about time left for next train to come
- Information boards time will adjust to operate only if trains are active

<img src="/images/final-visualization.png" alt="Vizualization" width="800"/>



