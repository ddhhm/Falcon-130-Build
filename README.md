# Falcon-130-Build

Note: I have had a successful flight.  https://youtu.be/MfE_hjf2OHk

Progress on my quadcopter based on the Falcon 130 frame

I want to build my first true "drone".  Basically, it's an RC model that I will fly with a Taranis radio and FatShark goggles.  It will not have capabilities like a camera drone such as GPS navigation and cannot be controlled via my mobile phone, but it will be faster than a phantom and the Taranis has less latency than a mobile phone.

Parts I have:

    Frame   Falcon 130
    Motors  4x EMAX "red bottom" 4000kv 1306 motors
    ESCs    20A Cicada 4-in-1 ESC
    FC      Betaflight 3 flight controller
    VTX     FX799T 200mW 
    RX      FrSky XSR
    Camera  Diatone 600TVL 120° Mini Camera Black

Notes:

The ESCs are not arranged in the same order as betaflight FC expects.  However, I can reverse 2 signal wires to compensate, so I can solder the motors normally (1 to 1, 2 to 2, 4 to 3, 3 to 4).

Example motor layout discrepancy:

      Cicada ESC               Betaflight
      
      M3      M2               M4      M2
      
      
      M4      M1               M3      M1
      
Reversinmg signal wires for 3 and 4 in the ESC should work.  BEWARE: The only labeling for the signal wire pinouts is on the heatshrink shielding which I have cut off.  Don't lose that scrap of heatshrink!!!


The motors might not turn the correct direction.  This can be fixed in the Blheli firmware program for Windows.  This is described by "Project Blue Falcon" (RIP).

https://www.youtube.com/watch?v=al4G6XJPD9c

I can still get telemetry for current using the 4in1 ESC and the Betaflight F3 board, but it is tricky.  This is something that is simply not done normally, but Joshua Bardwell describes it here:

https://www.youtube.com/watch?v=1SvbZNU72FE

Camera.  Wiring of these mini cameras (and removal of the microphone) is talked about by HyphPV in this build video:

https://youtu.be/cVldRv-DDuk?list=PLcs2SVI9Fg5Bx08ZxAD2ofqBIjhT891Wz

Great video from Project Blue Falcon for wiring the receiver to the Betaflight F3 controller.  Note, our "X" series controller is going to run on a UART, and will be configured in the betaflight software as SmartPort.

https://www.youtube.com/watch?v=fENayvv9-cg&t=7s#t=327.12439
