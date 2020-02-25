# Wekinator Helpers

Two Max 8 patches to help with using the gametrak controller

## Gametrak to midi

Maps the gametrack input to midi cc values.

- Scale the output
- Filter repeated values from output stream
- Preset store/recall

## Gametrak to wekinator

Maps the gametrak input to osc messages for wekinator

- Set up projects with I/O configuration
- Input routing
- Control wekinator from max
- Footpedal options, pass through, freeze or record. 
    - Pass through sends data to wekinator
    - Freeze mode will pause the input to wekinator when the pedal is held (allows to set up starting values)
    - Record mode will activate example recording in wekinator when the footpedal is held
- Preset store/recall

## Troubleshooting

### Wekinator hid input routing

The gametrak is routed according to the values assigned on my mac (Catalina)

    route 17 18 19 20 21 22 3

It's possible that you will need to edit the patch and alter these if it differs on your system.

### Capturing Input

You can use the r object in max to receive some data from the patches if needed.

#### Raw HID input

    toGTRoute


#### Routed Input

    LX LY LX RX RY RZ FSw
