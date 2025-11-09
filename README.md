# Cyclone V SoC MIPI CSI-2 IMX291

## If this project is constructive, welcome to donate a drink to PayPal.

<img src="images/qrcode.png" style="height:20%; width:20%"/>

or 

paypal.me/briansune


# Quartus Project Resource

To reduce the usage of PLL, 74.25MHz oscillator can be used.

Where both HDMI core and MIPI CSI 2 for SONY based CMOS uses 74.25M integer frequency division.

74.25Mhz 148.5MHz 37.125MHz etc, hence, integer PLL is only required.

```
+-----------------------------------------------------------------------------------+
; Flow Summary                                                                      ;
+---------------------------------+-------------------------------------------------+
; Revision Name                   ; ddr512_base                                     ;
; Top-level Entity Name           ; top                                             ;
; Family                          ; Cyclone V                                       ;
; Device                          ; 5CSEBA5U19C6                                    ;
; Timing Models                   ; Final                                           ;
; Logic utilization (in ALMs)     ; 2,291 / 32,070 ( 7 % )                          ;
; Total registers                 ; 5066                                            ;
; Total pins                      ; 175 / 205 ( 85 % )                              ;
; Total virtual pins              ; 0                                               ;
; Total block memory bits         ; 1,529,856 / 4,065,280 ( 38 % )                  ;
; Total DSP Blocks                ; 6 / 87 ( 7 % )                                  ;
; Total HSSI RX PCSs              ; 0                                               ;
; Total HSSI PMA RX Deserializers ; 0                                               ;
; Total HSSI TX PCSs              ; 0                                               ;
; Total HSSI PMA TX Serializers   ; 0                                               ;
; Total PLLs                      ; 5 / 6 ( 83 % )                                  ;
; Total DLLs                      ; 1 / 4 ( 25 % )                                  ;
+---------------------------------+-------------------------------------------------+
```

# Hardware

| HW no | Description | Image |
|-|-|-|
| 1 | CMOS (camera) | <img src="images/imx291.png" width="200"/> |
| 2 | Development Board | <img src="images/EVM.JPG" width="200"/> |

# Feature and Support

1) LW-H2F register controlled R-G-B gain.
2) Simple CMOS debayer
3) Loop-back to HDMI via FPGA2SDRAM
4) I2C control and adjust via HPS2FPGA fabric.
5) Reset\Power control pin via HPS to FPGA fabric IO.

# CMOS Capture image

<img src="images/frame_color.png" width="600"/>

# ToDo

- Very simple no V4L2 driver is used and no Linux control layer is supported.
- No frame buffering, current design can easily use more SDRAM space to hold CMOS capture frame.

# Contact

> briansune@gmail.com
