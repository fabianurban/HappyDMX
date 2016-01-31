The idea ist that -unlike any other DMX Tool- you work with zones of fixtures instead with scenes, that is very good for live performances and doing things on the Fly. 

a zone can be a Physical Area like the Stage or the Lounge, but also a logical "Area" like all Movingheads or PARs

the zones inherit all the properties of their parents. So if you set a property on the zone "Partyarea" all Fixtures in this area react to that. After that you can set the property on childzones.

The fixtures can also be in multiple zones, the last property which has been set "wins", or you do bool logic on them.

a property can be many things, like 
* Color: RGB(W/A/UV), HSV Colors, Strobe, Shutter for Light Fixtures
* Movement: Pan, Tilt, Speed, Focus, Zoom, Gobo, Gobo rotation. for things Like Movingheads and Scanners
* Atmospheric: Fogs, Fans, Dimmerpacks, Motors,...


some examples in pseudocode for the "Live Mode": 

* set Venue/Partyarea HSV(120,100,50) //everything on the Partyarea is green
* set Venue/Stage AND NOT Venue/Left Strobe(10) //lets every fixture on the Stage except for the left part Strobe at ~10Hz, the korrelation from DMX Value to Frequency is stored in the Fixturedefinition.
* set Venue fazer(70) fan(100) // lets the pump work at 70 percent and the Fan of the Fazer at full load
* set Venue fazer(b180) fan(b255) //same as the thing above, but with the raw dmx values
