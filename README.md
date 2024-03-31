# Three-level-Window-Comparator-Circuit-PCB
This project aims to create a three-level window comparator circuit with LEDs using LM741 operational amplifiers, including a power supply circuit for biasing voltages, and a fully functional PCB for the entire circuit.

Circuit Design Procedure:

Components Required:
Component Name	                                             Quantity	                               Purpose
LM741 Operational Amplifiers	                                   2	                                 Comparator IC
Resistors (R1, R2, R3, R4, R5, R6, R7)
                                                        R1 = R2 = R3 = 10kΩ 
                                                          R4 = R7 = 1kΩ 
                                                          R5 = R6 = 470Ω	                           7	Voltage Divider Network and Current Limiting
LEDs                                          (Led1 - Yellow, Led2 - Green, Led3 - Red)	             3	Visual Indication
Center-Tapped Transformer	                                       1	                                 AC to AC Step-Down Transformer
Bridge Rectifier (1N400x series)	                               1	                                 AC to DC Rectification
Filter Capacitors (100uF)	                                       2	                                 Smoothing of Rectified DC
LM7812 Positive Voltage Regulator	                               1	                                 Positive Voltage Regulation (for +12V)
LM7912 Negative Voltage Regulator	                               1	                                 Negative Voltage Regulation (for -12V)
Potentiometer 1MΩ	1	For Controlling Input Voltage

Procedure:

Power Supply Circuit:
Plug to connect transformer’s input with socket safely. 
Transformer and Rectification:
1.Connect the center tap of the transformer to the common ground.
2.Connect each end of the transformer secondary winding to the inputs of the bridge rectifier.
3.Connect the outputs of the bridge rectifier to the inputs of the filter capacitors (100uF).
4.Ensure correct polarity: Connect the positive side of the capacitor to the positive rail and the negative side to the negative rail.
Voltage Regulation:
5.Connect the output of the positive side's filter capacitor to the input of the LM7812 positive voltage regulator.
6.Connect the output of the negative side's filter capacitor to the input of the LM7912 negative voltage regulator.
7.Connect the common ground of both regulators to the common ground of the circuit.

Window Comparator Circuit:

Operational Amplifier Connections:
8.Connect the non-inverting inputs of both LM741 operational amplifiers to the single input signal source.
Resistor and LED Connections:
9.Connect resistors and LEDs as follows:
R1: Connect one end to Vcc, and the other end to the inverting input of the first LM741.
R2: Connect one end to the inverting input of the first LM741, and the other end to the inverting input of the second LM741.
R3: Connect one end to the inverting input of the second LM741, and the other end to ground.
R4: Connect one end to the end of R1 connected to Vcc, and the other end to the common end of R5 and the red LED.
R5: Connect one end to the common end of R4 and the other end to ground.
R6: Connect one end to the end of R3 connected to ground, and the other end to the yellow LED.
R7: Connect one end to the other end of the yellow LED, and the other end to -Vcc.
Led1 (yellow): Connect one end between the common end of R4 and R5, and the other end to the output of the first LM741.
Led2 (green): Connect one end to the output of the first LM741, and the other end to the output of the second LM741.
Led3 (red): Connect one end to the output of the second LM741, and the other end to one end of R7. The other end of R7 is connected to -Vcc.
Feedback Connections:
10.Connect the non-inverting inputs to the output through appropriate feedback loops.
Power Supply Connections:
11.Use the regulated +12V output from LM7812 as Vcc for the comparator circuit.
12.Use the regulated -12V output from LM7912 as -Vcc for the comparator circuit.

PCB Layout Procedure:
Trace Widths and Reason for Selection (T30):
For the PCB layout, a trace width of T30 has been selected. The reason for choosing this trace width is to ensure robustness and reliability during the fabrication and assembly processes. The thicker traces offer several advantages:
1.Current-Carrying Capacity:
Thicker traces (T30) can carry higher currents without significant voltage drops or resistive losses.
2.Heat Dissipation:
Wider traces dissipate heat more effectively, reducing the risk of overheating during operation.
3.Robustness During Etching:
Thicker traces are more resilient during the etching process, ensuring that the copper traces are well-preserved on the PCB.
4.Reliability in Manufacturing:
Thicker traces are less prone to damage during the manufacturing process, reducing the likelihood of open circuits or defects.

Step-by-Step Procedure for Creating PCB Layout:
Step 1: Import the Schematic:
 Open your project in Proteus.
 Ensure that your schematic is error-free and saved.
 Click on the "Ares" (PCB Layout) button in the toolbar.
Step 2: PCB Layout Setup:
 Once in Ares, go to "Design" -> "Layer Setup."
 Set up the PCB layers as needed, including copper layers, silkscreen, and solder mask layers.
 Define board dimensions by selecting "Board Size" from the "Design" menu. And draw Board.
Step 3: Component Placement:
 Go to the "Place" menu and select "Parts."
 Place components on the PCB layout. Proteus will initially place them randomly; you can rearrange them manually.
 Adjust the position of components to optimize trace routing and minimize trace lengths.
Step 4: Configure PCB Properties:
 In ARES, navigate to "Design" > "Layer Pairs and Properties."
 Set the board to have a single layer by choosing "Single Layer (Bottom Copper)."
Step 5: Trace Routing:
 Click on the "Route Tracks" button in the toolbar.
 Begin routing traces by clicking on the pads of components.
 Proteus will automatically attempt to route the traces; you can guide it or manually route traces by clicking on the desired paths.
Step 6: Silkscreen and Labels:
 Add silkscreen markings for component outlines, reference designators, and labels.
 Double-check and ensure clear and concise labeling for better understanding.
Step 7: Design Rule Check (DRC):
 Run a Design Rule Check (DRC) to identify and rectify any violations.
 Address any clearance, spacing, or other design rule violations.
Step 8: 3D View:
 Utilize 3D views and cross-sections to verify component clearances and ensure proper layer alignment.
 Adjust component heights as needed.
Step 9: Final Review:
 Review the entire PCB layout to ensure correctness.
 Save your PCB layout.

Step by step Procedure of Creating PDF File of PCB Layout:
1. View the PCB Layout:
 Open your PCB layout in Proteus ARES.
 Ensure that the design is finalized and ready for documentation.
2. Generate Print Preview:
 Go to the "Output" menu. Then, go to “Export Graphics.”
 Select "Export Adobe PDF File."
3. Configure Print Settings:
 Adjust the print settings as needed, including paper size, orientation, and scale.
 Ensure that you are printing the bottom copper layer or the layer you want to document.
4. Print to PDF:
 If your system has a PDF printer installed (like Adobe PDF, Microsoft Print to PDF, or any third-party PDF printer), select it as the printer.
 Alternatively, choose "Microsoft XPS Document Writer" or any other virtual printer if you plan to convert XPS to PDF later.
5. Save as PDF:
 After selecting the PDF printer, click on the "Print" or "OK" button.
 Choose a location to save the PDF file.
 Provide a meaningful name for the PDF document.
6. Verify PDF Document:
 Open the generated PDF file using a PDF viewer to verify that the content is accurate.
 Check that the layers, components, traces, and labels are clearly visible.

List of Connectors Used:
Connectors are used for those components, whose PCB package doesn’t exist.
 Center-Tapped Transformer:
Connector: 3-pin connector for primary and secondary windings.
 LEDs (Led1 - Yellow, Led2 - Green, Led3 - Red):
Connector: 2-pin connectors for easy replacement or testing.

PCB Hardware Implementation Procedure:

Step-by-Step Procedure:
1.Take Printout of PCB Layout:
 Mirror print the layout.
 Print in black on the glossy side of the paper.
2.Cutting the Copper Plate:
 Cut the copper board according to the layout size.
3.Make it Smooth:
 Rub the copper side using steel wool to remove oxide layer.
4.Transfer Image to Copper Plate:
 For Iron on Glossy paper method:
 Align and place copper side on the printed layout.
 Iron the image onto the copper plate.
5.Etching:
Wear gloves.
Dissolve Ferric chloride in water.
Dip the PCB into the etching solution for about 30 minutes.
Check and repeat until all unmasked copper is etched.
6.Disposal:
 Dilute etching solution before disposal.
7.Final Touch:
 Use thinner to remove toner.
 Rinse and dry the PCB.
 Drill holes and solder components.

Precautions:
 Avoid direct contact with the hot copper plate.
 Use gloves when handling the etching solution.
 Dispose of the etching solution properly.
 Be cautious while using the iron.

Power Supply Circuit Working:
1.AC to DC Conversion (Transformer and Rectification):
 The center-tapped transformer steps down the input AC voltage, providing two secondary windings.
 The bridge rectifier converts AC to pulsating DC, allowing current flow in one direction.
2.Smoothing (Filtering):
 Filter capacitors (100uF) smooth out the pulsating DC, charging during peaks and discharging during dips, reducing ripples.
3.Voltage Regulation (LM7812 and LM7912):
 LM7812 Positive Voltage Regulator stabilizes the positive output at +12V.
 LM7912 Negative Voltage Regulator stabilizes the negative output at -12V.
 The regulators ensure a constant output despite variations in input or load.
4.Output Stage:
 Stable and regulated +12V and -12V outputs are available for the entire circuit.
Window Comparator Circuit Working:
5.Operational Amplifier Biasing:
 The regulated +12V and -12V serve as biasing voltages for the operational amplifiers (LM741) in the window comparator circuit.
6.Comparator Operation:
 The window comparator compares the input voltage (Vin) with two reference voltages, Vref1 and Vref2, set by the resistor network.
 The non-inverting inputs of both LM741s are connected to Vin, and the inverting inputs are connected to the outputs through appropriate feedback loops.
7.LED Indication:
 Led1 (Yellow) lights up when Vin is less than Vref1.
 Led2 (Green) lights up when Vin is between Vref1 and Vref2.
 Led3 (Red) lights up when Vin is greater than Vref2.

Vin (Input Voltage)	Vref1 (8V)	Vref2 (4V)	Vref (Vref1 + Vref2)	LED3 (Red)	LED2 (Green)	LED1 (Yellow)	Potentiometer Value (ohm)
         0V	             8V	         4V	             12V	            ON	         OFF	          OFF               	-
         1V	             8V	         4V	             12V	            ON           OFF           	OFF              	90.9
         2V              8V	         4V	             12V	            ON	         OFF	          OFF	              200
         3V	             8V	         4V	             12V	            ON	         OFF	          OFF	              334
         4V	             8V	         4V	             12V	            OFF	         ON	            OFF	              500
         5V	             8V	         4V	             12V	            OFF	         ON	            OFF	              714
         6V	             8V	         4V	             12V	            OFF	         ON	            OFF	              1000
         7V	             8V	         4V	             12V	            OFF	         ON	            OFF	              1400
         8V	             8V          4V	             12V	            OFF	         ON	            OFF	              2000
         9V	             8V	         4V	             12V	            OFF	         OFF	          ON	              3000
         10V	           8V	         4V	             12V	            OFF	         OFF	          ON	              5000
         11V	           8V	         4V	             12V	            OFF	         OFF	          ON	              11000
         12V	           8V	         4V	             12V	            OFF	         OFF	          ON	              1M
         
8.Feedback and Amplification:
 The feedback loops in the operational amplifiers play a crucial role in adjusting the output based on Vin and the reference voltages.
9.AC to DC Conversion:
 The power supply converts the input AC to stable and regulated +12V and -12V outputs.
10.Window Comparator Operation:
 The window comparator circuit provides visual indication through LEDs based on the comparison between Vin and the reference voltages.
11.Conclusion:
 The combined circuit offers a reliable power supply along with a window comparator for monitoring and signaling based on predefined voltage thresholds.

Summary:
The circuit seamlessly integrates power supply and window comparator functionalities, making it suitable for applications where precise voltage monitoring and indication are required. Each stage plays a critical role in ensuring stability, regulation, and effective comparison of input voltages.
