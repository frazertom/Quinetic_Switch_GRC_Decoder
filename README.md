# Quinetic_Switch_GRC_Decoder
## Description
GNU Radio companion flowgraphs which use a basic RTL SDR to receive, demdodulate and decode the output from a Quinetic wireless switch.  
The switches are sold by [TLC Electrical](https://www.tlc-direct.co.uk/Main_Index/Quinetic/index.html#) in the UK.  
Currently this has only been tested on basic push button light switches. The switches tested are listed below.
- QU WS1: Single paddle switch
- QU WS2: Double paddle switch
- QU GDMK: Grid switch MK style
- QU GDVL: Grid switch Varilight style

The output from each flow graph is a tagged stream and also a print to the console of the data contained within the transmitted packet.
Each packet transmitted contains the following
- 16bit Switch ID (For the paddle switches this is the ID printed on the back within the barcode)
- 8bit Data section which contains pressed/released info as well as which switch was pressed for multi switch models
- 16bit CRC check sum

