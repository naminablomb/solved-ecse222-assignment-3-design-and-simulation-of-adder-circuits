Download Link: https://assignmentchef.com/product/solved-ecse222-assignment-3-design-and-simulation-of-adder-circuits
<br>
<h1>1        VHDL Description of Adder Circuits</h1>

In this assignment, you will be asked to perform the design and simulation of the following two adder circuits: (a) a 4-bit ripple-carry adder; and (b) a one-digit binary coded decimal (BCD) adder. Details of the assignments are described below.

<h2>1.1       Ripple-Carry Adder (RCA)</h2>

In this section, you will implement a structural description of a 4-bit ripple-carry adder using basic addition components: half-adders and full-adders.

<h3>1.1.1      Structural Description of a Half-Adder in VHDL</h3>

A half-adder is a circuit that takes two binary digits as inputs, and produces the result of the addition of the two bits in the form of a sum and carry signals. The carry signal represents an overflow into the next digit of a multi-digit addition. Using the following entity definition for your VHDL code, implement a structural description of the half-adder.

<table width="673">

 <tbody>

  <tr>

   <td width="673">library              IEEE;use IEEE.STD_LOGIC_1164.ALL; use IEEE.NUMERIC_STD.ALL; entity half_adder i sport (a: in               std_logic ;</td>

  </tr>

  <tr>

   <td width="673">b: in std_logic ; s: out std_logic ; c: out std_logic );end half_adder;</td>

  </tr>

 </tbody>

</table>

After you have described your structural style of the half-adder in VHDL, you are required to test your circuit. Write a testbench code and perform an exhaustive test of your VHDL description of the half-adder.

<h3>1.1.2      Structural Description of a Full-Adder in VHDL</h3>

Unlike the half-adder, a full-adder adds binary digits while accounting for values carried in (from a previous stage addition). Write a structural VHDL description for the full-adder circuit using the half-adder circuit that you designed in the previous section. Use the following entity declaration for your structural VHDL description of the full-adder.

<table width="673">

 <tbody>

  <tr>

   <td width="673">library              IEEE;use IEEE.STD_LOGIC_1164.ALL; use IEEE.NUMERIC_STD.ALL; entity full_adder i sport (a: in                std_logic ; b: in                  std_logic ; c_in: in                  std_logic ; s: out                  std_logic ; c_out: out                  std_logic );end full_adder;</td>

  </tr>

 </tbody>

</table>

After you have described your circuit in VHDL, write a testbench code and perform an exhaustive test of your VHDL description of the full-adder.

<h3>1.1.3      Structural Description of a 4-bit Ripple-Carry Adder (RCA) in VHDL</h3>

Using the half-adder and full-adder circuits implemented in the two previous sections, implement a 4-bit carry-ripple adder. Write a structural VHDL code for the 4-bit RCA using the following entity declaration.

<table width="673">

 <tbody>

  <tr>

   <td width="208">library                IEEE;use IEEE.STD_LOGIC_1164.ALL; use IEEE.NUMERIC_STD.ALL;entity rca_structural i s port ( A: in std_logic_vector</td>

   <td width="465">(3 downto 0);</td>

  </tr>

  <tr>

   <td width="208">                  B: in                       std_logic_vector</td>

   <td width="465">(3 downto 0);</td>

  </tr>

  <tr>

   <td width="208">S: out std_logic_vector end rca_structural;</td>

   <td width="465">(4 downto 0));</td>

  </tr>

 </tbody>

</table>

Note that <em>S</em>(4) contains the carry-out of the 4-bit adder. After you have described your circuit in VHDL, write a testbench code and perform an exhaustive test of your VHDL structural description of the 4-bit RCA.

<h3>1.1.4      Behavioral Description of a 4-bit RCA in VHDL</h3>

In this part, you are required to implement the 4-bit RCA using behavioral description. One way to obtain a behavioral description is to use arithmetic operators in VHDL (<em>i.e.</em>, “+”). Write a behavioral VHDL code for the 4-bit RCA using the following entity declaration for your behavioral VHDL description.

<table width="673">

 <tbody>

  <tr>

   <td width="208">library                IEEE;use IEEE.STD_LOGIC_1164.ALL; use IEEE.NUMERIC_STD.ALL;entity rca_behavioral i s port ( A: in std_logic_vector</td>

   <td width="465">(3 downto 0);</td>

  </tr>

  <tr>

   <td width="208">                  B: in                       std_logic_vector</td>

   <td width="465">(3 downto 0);</td>

  </tr>

  <tr>

   <td width="208">S: out std_logic_vector end rca_behavioral;</td>

   <td width="465">(4 downto 0));</td>

  </tr>

 </tbody>

</table>

After you have described your circuit in VHDL, write a testbench code and perform an exhaustive test of your VHDL behavioral description of the 4-bit RCA.

<h2>1.2       VHDL Description of a One-Digit BCD Adder</h2>

In this section, you will implement a one-digit BCD adder in VHDL. A one-digit BCD adder adds two four-bit numbers represented in a BCD format. The result of the addition is a BCD-format 4-bit output, representing the decimal sum, and a carry that is generated if this sum exceeds a decimal value of 9 (see slides of Lecture #11).

<h3>1.2.1      Structural Description of a BCD Adder in VHDL</h3>

In this part, you are required to implement the BCD adder using structural description. You are allowed to use either behavioral or structural style of coding for your implementation. Using the following entity definition. Use the following entity declaration.

<table width="673">

 <tbody>

  <tr>

   <td width="673">library              IEEE;use IEEE.STD_LOGIC_11164.ALL; use IEEE.NUMERIC_STD.ALL;entity bcd_adder_structural i s port ( A: in std_logic_vector (3 downto 0); B: in std_logic_vector (3 downto 0);S: out                                   std_logic_vector (3 downto 0);C: out          std_logic ); end bcd_adder_structural;</td>

  </tr>

 </tbody>

</table>

After you have implemented the one-digit BCD adder in VHDL, you are required to test your circuit. Write a testbench code and perform an exhaustive test of your VHDL structural description of the one-digit BCD adder.

<h3>1.2.2      Behavioral Description of a BCD Adder in VHDL</h3>

In this part, you are required to implement the BCD adder using behavioral description. You are encouraged to base your code on the VHDL code in Section 5.7.3 of the textbook, so that you learn about conditional signal assignments (these are explained in detail in the same section as well as in the Appendix in Section A.7.4). Use the following entity declaration.

<table width="673">

 <tbody>

  <tr>

   <td width="673">library              IEEE;use IEEE.STD_LOGIC_11164.ALL; use IEEE.NUMERIC_STD.ALL;entity bcd_adder_behavioral i s port ( A: in std_logic_vector (3 downto 0);B: in                        std_logic_vector (3 downto 0);S: out          std_logic_vector (3 downto 0); C: out                    std_logic ); end bcd_adder_behavioral;</td>

  </tr>

 </tbody>

</table>

After you have implemented the one-digit BCD adder in VHDL, you are required to test your circuit. Write a testbench code and perform an exhaustive test for your VHDL behavioral description of the one-digit BCD adder.

<h2>1.3       Timing Analysis and Critical Path</h2>

In this part you will learn how to perform timing analysis in the EDAPlayground platform. You will also be able to find the critical path of a given circuit.

The critical path is the longest path in the circuit which defines the speed of the circuit. The speed of a digital circuit is measured in terms of latency and throughput. Latency is the time needed for the circuit to produce an output for a given input (<em>i.e.</em>, the total propagation delay (time) from the input to the output), and it is expressed in units of time. Alternatively, throughput refers to the rate at which data can be processed. In this assignment, we only consider the latency as a metric to measure the speed of the circuit.

In general, digital circuits are subject to timing constraints dictated by the target application. Whether a circuit meets these timing constraints can only be known after the circuit is synthesized. After synthesis is performed, the designer can analyze the circuit to determine whether timing constraints were satisfied using the term slack.

Slack is the margin by which a timing requirement is met or not met; it is the difference between the required arrival time and the actual arrival time. A positive slack value indicates the margin by which a requirement was met. A negative slack value indicates the margin by which a requirement was not met.

To simulate timing constraints, we can add time constraint files to our design. Here, we will use the 4-bit RCA that we designed in Section 3.1.3 (structural description) as an example. Please note that for your assignment submission, you will be required to analyze the timing of the BCD adder, NOT the RCA that is used here as an example only.

Create a new file by clicking on the (+) icon (next to testbench.vhd).

Name the file rca.sdc. Note that sdc stands for Synopsis Design Constraints.

The maximum delay can be specified in the sdc file using the following command:

set_max_delay -from [get_ports &lt;name_of_input_port&gt;] -to [get_ports &lt;name_of_output_port&gt;] &lt;time in nano seconds&gt;

In this example, we set the delay to be 20 nsec (nano seconds) from the input <em>A </em>to the output <em>S </em>(for all possible paths), and 15 nsec from the input <em>B </em>to the output <em>S </em>(for all possible paths).

set_max_delay -from [get_ports A[*]] -to [get_ports S[*]] 20 set_max_delay -from [get_ports B[*]] -to [get_ports S[*]] 15

Update your run.do file to include time delay related information. The updated run.do file should look like this:

<table width="673">

 <tbody>

  <tr>

   <td width="673">add_input_file rca.sdcsetup_design -manufacturer Xilinx -family Artix-7 -part 7A100TCSG324 foreach arg $::argv { add_input_file $arg} compile synthesizeauto_write precision.v report_output_file_list report_area report_timing exec cat precision.v</td>

  </tr>

 </tbody>

</table>

Make sure that your system settings look like this:

Click run (remember to set the simulator to <em>Mentor Precision 2019.2 </em>for this part), and you will be able to see the timing analysis information in the compiler log. In this example, the log looks like this:

For example, the critical path from input <em>A(3) </em>to output <em>S(4) </em>exhibits a positive slack of 15.019 ns, which means that the circuit meets the requirement.




<h1>3        Questions</h1>

Please note that even if some of the waveforms may look the same, you still need to include them separately in the report.

<ol>

 <li>Briefly explain your VHDL code implementation of all circuits.</li>

 <li>Show representative simulation plots of the half-adder circuit for all possible input values.</li>

 <li>Show representative simulation plots of the full-adder circuit for all possible input values.</li>

 <li>Show representative simulation plots of both behavioral and structural descriptions of the 4-bit RCA for all possible input values.</li>

 <li>Show representative simulation plots of both behavioral and structural descriptions of the one-digit BCD adder circuit for all possible input values.</li>

 <li>Perform timing analysis of the one-digit BCD adder and find the critical path(s) of the circuit. What is the delay of the critical path(s)? Assuming that an additional delay of 10 ns can be added to the critical path(s) due to wiring, what should be the <em>set<sub>m</sub>ax<sub>d</sub>elay </em>command to ensure a positive slack of 5 ns for the circuit (write the complete <em>set<sub>m</sub>ax<sub>d</sub>elay </em>command).</li>

 <li>Report the number of pins and logic modules used to fit your BCD adder designs on the FPGA board.</li>

</ol>

<table width="484">

 <tbody>

  <tr>

   <td width="176"> </td>

   <td colspan="2" width="154">RCA</td>

   <td colspan="2" width="154">One-digit BCD adder</td>

  </tr>

  <tr>

   <td width="176"> </td>

   <td width="76">Structural</td>

   <td width="78">Behavioral</td>

   <td width="76">Structural</td>

   <td width="78">Behavioral</td>

  </tr>

  <tr>

   <td width="176">Logic Utilization (in LUTs)</td>

   <td width="76"> </td>

   <td width="78"> </td>

   <td width="76"> </td>

   <td width="78"> </td>

  </tr>

  <tr>

   <td width="176">Total pins</td>

   <td width="76"> </td>

   <td width="78"> </td>

   <td width="76"> </td>

   <td width="78"> </td>

  </tr>

 </tbody>

</table>


