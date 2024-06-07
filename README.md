# G-Code

A reference sheet for CNC G-code that aims to be universal (lol)

I found
[this guide from How To Mechatronics](https://howtomechatronics.com/tutorials/g-code-explained-list-of-most-important-g-code-commands/)
super helpful.

# Milling G-Codes (Quick Reference)
I'm going to do my best to identify the common/generic codes here. I may
miss some or have some wrong, so use these codes at your own risk.

I've built this list from the following resources:
* [CNC Cookbook](https://www.cnccookbook.com/g-code-m-code-reference-list-cnc-mills/)
* [Marlin](https://marlinfw.org/meta/gcode/)
* [Carbide Depot](https://www.carbidedepot.com/formulas-gcodes.htm)

Another great tool is [NCViewer](https://ncviewer.com/), which allows you to
visualize G-code in your browser.

## G Codes
G codes are "Geometry Codes" and are used to control the movement of the tool

| Command | Description                                | Mode             | Parameters             | Notes                                         |
|---------|--------------------------------------------|------------------|------------------------|-----------------------------------------------|
| G00     | Linear Movement (non-machining)            | Milling, Turning | X, Y, Z, F, S          |                                               |
| G01     | Linear Movement                            | Milling, Turning | X, Y, Z, F, S          |                                               |
| G02     | Circular Interpolation (Clockwise)         | Milling, Turning | X, Y, Z, I, J, R, F, S |                                               |
| G03     | Circular Interpolation (Counter-clockwise) | Milling, Turning | X, Y, Z, I, J, R  F, S |                                               |
| G04     | Dwell (programmed time delay)              | Milling, Turning | P, S                   |                                               |
| G05     |                                            |                  |                        |                                               |
| G06     |                                            |                  |                        |                                               |
| G07     |                                            |                  |                        |                                               |
| G08     |                                            |                  |                        |                                               |
| G09     | Exact Stop Check                           | Milling, Turning |                        |                                               |
| G10     |                                            |                  |                        |                                               |
| G11     |                                            |                  |                        |                                               |
| G12     |                                            |                  |                        |                                               |
| G13     |                                            |                  |                        |                                               |
| G14     |                                            |                  |                        |                                               |
| G15     | Disable Polar Coordinates                  | Milling          |                        |                                               |
| G16     | Enable Polar Coordinates                   | Milling          |                        |                                               |
| G17     | XY Plane Selection                         | Milling, Turning |                        |                                               |
| G18     | ZX Plane Selection                         | Milling, Turning |                        |                                               |
| G19     | YZ Plane Selection                         | Milling, Turning |                        |                                               |
| G20     | Use Inches As Unit Distance                |                  |                        |                                               |
| G21     | Use Millimeters As Unit Distance           |                  |                        |                                               |
| G22     |                                            |                  |                        |                                               |
| G23     |                                            |                  |                        |                                               |
| G24     |                                            |                  |                        |                                               |
| G25     |                                            |                  |                        |                                               |
| G26     |                                            |                  |                        |                                               |
| G27     | Reference Point Return Check               | Milling, Turning | X, Y, Z                |                                               |
| G28     | Return To Reference Point                  | Milling, Turning | X, Y, Z                |                                               |
| G29     | Return From Reference Point                | Milling, Turning | X, Y, Z                |                                               |
| G30     | Return To Alternate Reference              | Milling, Turning | X, Y, Z                |                                               |
| G31     |                                            |                  |                        |                                               |
| G32     |                                            |                  |                        |                                               |
| G33     |                                            |                  |                        |                                               |
| G34     |                                            |                  |                        |                                               |
| G35     |                                            |                  |                        |                                               |
| G36     |                                            |                  |                        |                                               |
| G37     |                                            |                  |                        |                                               |
| G38     |                                            |                  |                        |                                               |
| G39     |                                            |                  |                        |                                               |
| G40     | Cutter Compensation Off                    | Milling          |                        |                                               |
| G41     | Cutter Compensation Left                   | Milling          | D, H                   |                                               |
| G42     | Cutter Compensation Right                  | Milling          | D, H                   |                                               |
| G43     |                                            |                  |                        |                                               |
| G44     |                                            |                  |                        |                                               |
| G45     |                                            |                  |                        |                                               |
| G46     |                                            |                  |                        |                                               |
| G47     |                                            |                  |                        |                                               |
| G48     |                                            |                  |                        |                                               |
| G49     |                                            |                  |                        |                                               |
| G50     |                                            |                  |                        |                                               |
| G51     |                                            |                  |                        |                                               |
| G52     |                                            |                  |                        |                                               |
| G53     | Machine Coordinate System                  | Milling, Turning |                        |                                               |
| G54     | Work Coordinate System 1                   |                  |                        |                                               |
| G55     | Work Coordinate System 2                   |                  |                        |                                               |
| G56     | Work Coordinate System 3                   |                  |                        |                                               |
| G57     | Work Coordinate System 4                   |                  |                        |                                               |
| G58     | Work Coordinate System 5                   |                  |                        |                                               |
| G59     | Work Coordinate System 6                   |                  |                        |                                               |
| G60     |                                            |                  |                        |                                               |
| G61     |                                            |                  |                        |                                               |
| G62     |                                            |                  |                        |                                               |
| G63     |                                            |                  |                        |                                               |
| G64     |                                            |                  |                        |                                               |
| G65     | Custom Macro Call                          | Milling, Turning |                        | May not be supported                          |
| G66     |                                            |                  |                        |                                               |
| G67     |                                            |                  |                        |                                               |
| G68     | Coordinate System Rotation ON              | Milling          | X, Y, R                |                                               |
| G69     | Coordinate System Rotation OFF             | Milling          |                        |                                               |
| G70     |                                            |                  |                        |                                               |
| G71     |                                            |                  |                        |                                               |
| G72     |                                            |                  |                        |                                               |
| G73     |                                            |                  |                        |                                               |
| G74     |                                            |                  |                        |                                               |
| G75     |                                            |                  |                        |                                               |
| G76     |                                            |                  |                        |                                               |
| G80     | Canned Cycle Cancel                        |                  |                        |                                               |
| G81     | Drilling Cycle (No Dwell)                  | Milling, Turning |                        |                                               |
| G82     | Drilling Cycle (Dwell)                     | Milling, Turning |                        |                                               |
| G83     | Peck Drilling Cycle (Full Retract)         | Milling, Turning |                        |                                               |
| G84     |                                            |                  |                        |                                               |
| G85     |                                            |                  |                        |                                               |
| G86     |                                            |                  |                        |                                               |
| G87     |                                            |                  |                        |                                               |
| G88     |                                            |                  |                        |                                               |
| G89     |                                            |                  |                        |                                               |
| G90     | Absolute Dimension Input                   | Milling, Turning |                        |                                               |
| G91     | Incremental Dimension Input                | Milling, Turning |                        |                                               |
| G92     | set absolute zero point                    | Milling, Turning | X, Y, Z                | To reset, call again with negative dimensions |
| G93     |                                            |                  |                        |                                               |
| G94     | Units Per Minute (Feed Mode)               | Milling, Turning |                        |                                               |
| G95     | Units Per Revolution (Feed Mode)           | Milling, Turning |                        |                                               |
| G96     |                                            |                  |                        |                                               |
| G97     |                                            |                  |                        |                                               |
| G98     | Set Canned Cycle Return Point: Initial Z   |                  |                        |                                               |
| G99     | Set Canned Cycle Return Point: R plane     |                  |                        | Must be set when starting cycle               |

## M Codes
M codes are "Machine Codes" and are used to control the machine itself

| Command | Description                  | Mode             | Parameters | Notes                                                          |
|---------|------------------------------|------------------|------------|----------------------------------------------------------------|
| M00     | Program Stop                 | Milling, Turning |            |                                                                |
| M01     | Optional Program Stop        | Milling, Turning |            |                                                                |
| M02     | Program End                  | Milling, Turning |            |                                                                |
| M03     | Spindle On Clockwise         | Milling, Turning | S          |                                                                |
| M04     | Spindle On Counter-clockwise | Milling, Turning | S          |                                                                |
| M05     | Spindle Stop                 | Milling, Turning |            |                                                                |
| M06     | Tool Change                  | Milling, Turning | T          |                                                                |
| M07     | Mist Coolant On              | Milling, Turning |            |                                                                |
| M08     | Flood Coolant On             | Milling, Turning |            |                                                                |
| M09     | Coolant Off                  | Milling, Turning |            |                                                                |
| M10     |                              |                  |            |                                                                |
| M11     |                              |                  |            |                                                                |
| M12     |                              |                  |            |                                                                |
| M13     |                              |                  |            |                                                                |
| M14     |                              |                  |            |                                                                |
| M15     |                              |                  |            |                                                                |
| M16     |                              |                  |            |                                                                |
| M17     |                              |                  |            |                                                                |
| M18     |                              |                  |            |                                                                |
| M19     |                              |                  |            |                                                                |
| M20     |                              |                  |            |                                                                |
| M21     |                              |                  |            |                                                                |
| M22     |                              |                  |            |                                                                |
| M23     |                              |                  |            |                                                                |
| M24     |                              |                  |            |                                                                |
| M25     |                              |                  |            |                                                                |
| M26     |                              |                  |            |                                                                |
| M27     |                              |                  |            |                                                                |
| M28     |                              |                  |            |                                                                |
| M29     |                              |                  |            |                                                                |
| M30     | End Of Program               |                  |            |                                                                |
| M31     |                              |                  |            |                                                                |
| M32     |                              |                  |            |                                                                |
| M33     |                              |                  |            |                                                                |
| M34     |                              |                  |            |                                                                |
| M35     |                              |                  |            |                                                                |
| M36     |                              |                  |            |                                                                |
| M37     |                              |                  |            |                                                                |
| M38     |                              |                  |            |                                                                |
| M39     |                              |                  |            |                                                                |
| M40     |                              |                  |            |                                                                |
| M41     |                              |                  |            |                                                                |
| M42     |                              |                  |            |                                                                |
| M43     |                              |                  |            |                                                                |
| M44     |                              |                  |            |                                                                |
| M45     |                              |                  |            |                                                                |
| M46     |                              |                  |            |                                                                |
| M47     |                              |                  |            |                                                                |
| M48     |                              |                  |            |                                                                |
| M49     |                              |                  |            |                                                                |
| M50     |                              |                  |            |                                                                |
| M51     |                              |                  |            |                                                                |
| M52     |                              |                  |            |                                                                |
| M53     |                              |                  |            |                                                                |
| M54     |                              |                  |            |                                                                |
| M55     |                              |                  |            |                                                                |
| M56     |                              |                  |            |                                                                |
| M57     |                              |                  |            |                                                                |
| M58     |                              |                  |            |                                                                |
| M59     |                              |                  |            |                                                                |
| M60     |                              |                  |            |                                                                |
| M61     |                              |                  |            |                                                                |
| M62     |                              |                  |            |                                                                |
| M63     |                              |                  |            |                                                                |
| M64     |                              |                  |            |                                                                |
| M65     |                              |                  |            |                                                                |
| M66     |                              |                  |            |                                                                |
| M67     |                              |                  |            |                                                                |
| M68     |                              |                  |            |                                                                |
| M69     |                              |                  |            |                                                                |
| M70     |                              |                  |            |                                                                |
| M71     |                              |                  |            |                                                                |
| M72     |                              |                  |            |                                                                |
| M73     |                              |                  |            |                                                                |
| M74     |                              |                  |            |                                                                |
| M75     |                              |                  |            |                                                                |
| M76     |                              |                  |            |                                                                |
| M77     |                              |                  |            |                                                                |
| M78     |                              |                  |            |                                                                |
| M79     |                              |                  |            |                                                                |
| M80     |                              |                  |            |                                                                |
| M81     |                              |                  |            |                                                                |
| M82     |                              |                  |            |                                                                |
| M83     |                              |                  |            |                                                                |
| M84     |                              |                  |            |                                                                |
| M85     |                              |                  |            |                                                                |
| M86     |                              |                  |            |                                                                |
| M87     |                              |                  |            |                                                                |
| M88     |                              |                  |            |                                                                |
| M89     |                              |                  |            |                                                                |
| M90     |                              |                  |            |                                                                |
| M91     |                              |                  |            |                                                                |
| M92     |                              |                  |            |                                                                |
| M93     |                              |                  |            |                                                                |
| M94     |                              |                  |            |                                                                |
| M95     |                              |                  |            |                                                                |
| M96     |                              |                  |            |                                                                |
| M97     |                              |                  |            |                                                                |
| M98     | Call Subprogram              |                  | P          | Calls Subprogram identified by O code matching the P parameter |
| M99     | End Subprogram               |                  |            |                                                                |

## O Codes
O codes are used to denote subprograms

| Command | Description  | Notes |
|---------|-------------|-------|
| O<number> | Mark Subprogram Start | 0-9999 |
