# Router-Design-and-Verification

## Design
#### Router was designed with the signals: clk, reset, dut_inp, inp_valid, dut_outp, outp_valid, busy, error.
#### The 'dut_inp' and 'dut_outp' signals are the ones carrying the data. Signals 'inp_valid' and 'outp_valid' are present to indicate the validity of data on both sides (when the processing of data begins and ends).
#### The verification environment was created with a self-checking testbench that prints out the result of whether the test has been passed or not. 
#### The toal no.of packets sent must match the ones received.

## Working
#### Initially, an environment is created for testing.
#### Each time, a packet is generated, driven and collected at the testbench. The number of packets sent here are 10. It can be changed as per need.
#### Monitor classes written to continuoulsy check the transmission of the packet.
#### The packet is compared with the original each time using a compare() method. If the packet data matches, the matched variable in incremented. Else, mis_matched is incremented. 
#### Scoreboard keeps track of which packet is matched and which isn't. 
#### Report prints the information from input and output monitors regarding the no.of packets matched/mismatched. It also prints the Functional Coverage.

## Results
#### All ten packets have been generated, driven and collected without error at the testbench.
#### The output waveform has been attached for reference. 

![image](https://github.com/user-attachments/assets/a36667f1-8f39-414e-864c-0413ec348f15)
