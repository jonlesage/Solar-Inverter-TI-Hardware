# Model-based Design for Solar Power Control with Hardware

This demo shows how you can quickly design a new power control system using Simulink&reg; and Embedded Coder&reg; from MathWorks&reg; and the C2000&trade; platform of microcontrollers from Texas Instruments&reg;. We walk through a solar inverter demo, where we design and simulate a maximum power point tracking (MPPT) control in Simulink, and then deploy the control with Embedded Coder to a Texas Instruments C2000 Piccolo&trade; MCU.

![Solar Explorer Development Board](https://github.com/mathworks/Solar-Inverter-TI-Hardware/blob/main/5_IntroCodeGen/SolarExplorerBoard.png)

Hardware kit is available from TI: 
https://www.digikey.com/en/products/detail/texas-instruments/TMDSSOLARPEXPKIT/3028945

## Getting Started

To get started, clone this repository to directory:
1) Install the Texas Instruments Hardware Support Package and complete the Setup Process - https://www.mathworks.com/matlabcentral/fileexchange/43096?download=true
2) Plug-in USB to C2000 and ensure power cord jumpers are installed to connect the PV emulator, the DC-DC Boost converter, and the Single-Phase Inverter.
    - PV to DC-DC: Vpv -> Vin-b
    - DC-DC to Inverter: Vo-b -> V-Inv
3) Open "PV_MPPT_C2000_Algorithm.slx" and "PV_MPPT_C2000_Host.slx". Algorithm is deployed to the C2000 and the Host model allows for data visualization from the Development Board
4) Build and Deploy the "PV_MPPT_C2000_Algorithm.slx" model to the C2000
5) Run the Host Model (you might need to change the Serial COM port to match the development board serial) to interact with the solar inverter hardware

## Recording

A recording of this demo can be found in the "Developing Solar Inverter Control with Simulink" video series:
https://www.mathworks.com/videos/series/developing-solar-inverter-control-with-simulink.html

A modified version of this demo is available in the shipping TI Support Package Documentation now which can be used for further reference:
https://www.mathworks.com/help/releases/R2020a/supportpkg/texasinstrumentsc2000/ug/photovoltaic-inverter-mppt-solar-explorer-kit.html"# Solar-Inverter-TI-Hardware" 
