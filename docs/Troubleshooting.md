# Troubleshooting

## Problems with player script

| Problem | Cause | Solution |
|----------------------------------------|--------|----------|
| Player not moving | `CharacterController` has not been assigned | Drag your Player object’s `CharacterController` into the script field in the Inspector |
| Player not moving | Script not attached to player | Attach the `PlayerMove` script to your Player GameObject |
| Sprint not working | Shift key not detected | Ensure the Game window is focused |
| Player not jumping | Not grounded | Check `groundCheck` position and `groundMask` layer |
| Player keeps falling | Ground not detected | Make sure ground objects are on the correct layer used in `groundMask` |
| Player floating slightly above ground | Ground check too high | Lower the `groundCheck` object slightly below the player |
| Player falls through floor | `CharacterController` misconfigured | Check `Center`, `Height`, and `Radius` values |
| Player not rotating with camera | Movement uses player transform only | Add mouse look script to rotate player/camera |
| Ground detection inconsistent | Sphere too small | Increase `groundDistance` slightly (e.g. change 0.4 to 0.5) |
| Player clips into walls | Controller step offset too high | Lower `Step Offset` in CharacterController |
| Console errors (NullReferenceException) | Missing references | Ensure `controller` and `groundCheck` are assigned |

## Problems with Camera Script
| Problem | Cause | Solution |
|----------------------------------------|--------|----------|
|Unity error `NullReferenceException`|Variable expecting assignment is unassigned| Double check you've referenced PlayerBody in the editor|
|Unity error `error cs1002: ';' expected`|missing semicolon|find where it's missing and add a semicolon|
|Unity error `cs0103: the name '[variable name]' does not exist in the current context`|Misspelled or unknown variable name| Double check spelling of [variable name] to be consistent|
|cursor not locking to screen automatically|This happens on older versions of Unity|click on *game* window|
|cursor not dissapearing|Unity's `cursor.lockState` isn't causing this automatically|add `Cursor.visible = false;` on the line above `cursor.lockState`|