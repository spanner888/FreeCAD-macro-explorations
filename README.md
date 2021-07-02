# FreeCAD-macro-explorations
Macros I created (ie not official FreeCAD macros...but likely inspired by them)

## feeds_and_speeds_integration.FCMacro
	Demonstration script to run Feed and Speed Calculator FreeCAD addon, 
	which must be installed from https://github.com/dubstar-04/FeedsAndSpeeds, although see bug note below for alternate version.

	It uses the Feed and Speed Calculator to produce rpm, feed and power information.
	The Feed and Speed Calculator FreeCAD addon has a nice GUI that is accessed from FreeCAD Path menu, 
	but there is currently no integration with FreeCAD to use tool (or material) information in it's calculations
	nor does it place results into a FreeCAD Path ToolController.
	It is also the first stage of automating Tool -> Feed and Speed -> Tool Controller, which is coming in about one week :)
	Script also adds features:-
	  - Adds intial Feed Per Tooth based on material
	  - Automatic over ride of maximum Spindle Power, Feed Rate and max & min Spindle rpm, based on User settings
	  - Print all input vars in the FreeCAD report pane using showInputs()
	  These added features should be added to Feed and Speed Calculator, once everything bedded down.
	Plunge feed rates are not calculated.

	STATUS:-
	version 1.0
	Fully functional, except for bug noted below & easy fix available. Lots more planned - see notes at EOF "more TODOs & ideas:-"
	BUG: rpm over ride(s) do not work until this issue fixed https://github.com/dubstar-04/FeedsAndSpeeds/issues/7
	  Easy DIY fix is just change return value from rpm to calc_rpm. 
	  Alternatively get patched code from https://github.com/spanner888/FeedsAndSpeeds

## Below refer to older, functional, but pretty bad code, which might give you some usefull ideas.
### Curved slot example images:
![Sketch example](https://github.com/spanner888/FreeCAD-macro-explorations/blob/master/CurvedSlot/curvedSlot1.png)

![Sketch example 3D](https://github.com/spanner888/FreeCAD-macro-explorations/blob/master/CurvedSlot/curvedSlotPaddedSlots1.png)

![Sketch example](https://github.com/spanner888/FreeCAD-macro-explorations/blob/master/CurvedSlot/ExistingShapePlusSlots.png)

![Tabbed slot](https://github.com/spanner888/FreeCAD-macro-explorations/blob/master/CurvedSlot/notched%20Tabs%20inner%20%26%20outer%2C%20curved%20Slot.png)

### CNC Bed.
![CNC Bed, with paths](https://github.com/spanner888/FreeCAD-macro-explorations/blob/master/CNC_BED_upperY_16mm_longBearings_SKETCH_v1.png)
