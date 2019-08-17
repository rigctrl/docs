### Connecting RigCtrl Reset device

1. Get a long enough cable to cover the distance between RigCtrl Reset and each rig
    - A great choice of cable is a UTP network cable with 4 pairs (for 4 rigs) like this:
    ![UTP Cable](img/utp.jpg?resize=400,200)

2. Extend the cable with the 2 pin jumper (which is used to connect to the rig's motherboard)
    ![2pin](img/2pin.jpg)

3. Fasten one end of the cable on the device like in the picture
    - Each port reset port has three connection, use only the connections (in green) as in the picture below
    ![Reset wiring](img/relay-wiring-c.jpg?resize=600,400)

4. Connect the 2 pin jumper on your motherboard panel in the On/Off pins
    - _Consult your motherboard manual to locate the correct On/Off pins_
    ![Motherboard](img/mb-panel-connection.png?resize=600,400)

    !!! info "Wires between Reset and motherboard do not have current so the coloring is not important"

5. Assigning a port to a rig
    - Go to **Rig/Group List** in RigCtrl menu, in Rig List for the desired rig select the port from the dropdown where it is connected to, or
    - From home page open rig menu, click on **Edit Rig** and select a port

!!! attention
    If you have more than one RigCtrl Reset devices go to **Advanced Settings** menu, at the bottom of the page select correct the **Number of RigCtrl Reset devices** and save.
