---
layout: home
title: FPGA VGA Driver Project
tags: fpga vga verilog
categories: demo
---

Hello my name is Liam Plower and this is my System on Chip Design and Verification Project.


## **Template VGA Design**

## **Week 1 Update

I started of with using both templates the striped cycle and the slideshow like cycle changing every few seconds. I stook with the stripe cycle and messed around with the colours used and changed them to get used to the code. I ended up designing a French flag(Blue, White and Red) and started working on diagonal lines also for a Jamaican flag. For the French flag it was pretty much the basics as I had to change the layout of 8 to 3 stripes. I had to change the column size from 80 pixels across for the 8 to 3 columns by dividing 640 by 3. I got to learn new colour codes and how to get the likes of Red, Green, Blue, Yellow and a few more colours using the layout which was given to me at the start of the project. At the end of the Lab I started trying to learn diagonals and the maths behind it. I tried designing the Jamaica flag as this uses two yellow diagonal lines. 

<img width="582" height="646" alt="image" src="https://github.com/user-attachments/assets/2dd742e2-46f2-4d06-afeb-dc26359421c7" />  


https://github.com/user-attachments/assets/5bf92647-7ab9-460b-9d3b-46187efbdfb3

<img width="579" height="647" alt="image" src="https://github.com/user-attachments/assets/5d11c2d0-58a3-4cf0-8b07-fe1d3a6c9c6e" />





## **Week 2 Update
This week, I worked on the Jamaican flag in Verilog, correcting the positioning of the green and black sections to match the actual flag design, i started it by mixing up the green and black in the flag and I made the yellow diaganol lines way too skinny so I had to work on fixing it. I also changed the original bright green (4'b1111) to hunter green (4'b0110) to achieve a more realistic colour. Additionally, I researched the mathematics behind the diagonal lines to better understand how the equations and pixel coordinates work. I would have broken it down and ran through each section as synthesis, implementation and generating the bitstream. Breaking down code for diagonal: <img width="750" height="441" alt="image" src="https://github.com/user-attachments/assets/b7ab1e7a-867f-4cbd-9523-b79f70628007" />                                    
This code checks the position of each pixel on the screen using its X and Y coordinates. It uses mathematical equations to detect the two diagonal lines and colours them gold if the pixel is within 100 units of either line. It then checks whether the pixel is inside either of the two triangular areas and colours those green. If the pixel does not meet any of these conditions, it remains black. As you can see this was trial and error as the flag looks nothing like the actual Jamaica Flag so it was used as practice.                                                                                                
<img width="577" height="635" alt="image" src="https://github.com/user-attachments/assets/038c1992-5e8a-48a8-b89c-d52a15a983f8" />



## **Week 3 Update
I started breaking down part by part like simulation, synthesis, implementation and bitstream. Started with simulation to get the Testbench and breaking it down to understand how it works. You can now see that the Jamaica Flag is completely finished and looks like the original. I also got the Testbench to run this week to view the graphs.

<img width="575" height="640" alt="image" src="https://github.com/user-attachments/assets/39b79181-7dc8-441b-9cdb-0d504f10fba6" />


### **Project Set-Up**
The project was created in Xilinx Vivado using the appropriate FPGA board and device settings. The Verilog sources files were added to the project, along with the required constraint files. The design was then simulated, synthesised, implementated and generated through bitstream. The project summary provides an overview of the project configuration, source files and design status.

<img width="1154" height="730" alt="image" src="https://github.com/user-attachments/assets/290f4a41-cf6a-4535-892d-0f054db4eda2" />
At the start of week 1 we were given a BASYS3 prototype board to build the project on which was connected using an HDMI to a Micro B to the college PC's and then we were also given a VGA to VGA cable to connect the BASYS3 to the college monitors.

## **My VGA Design Edit**
My initial idea was the France flag and then a more complex flag like the Jamaica flag. With starting off with the France flag it was easy to design as it was just a basic three striped flag. Adding the Jamaica flag was much more intricate as it was 4 triangles shaped all diffrently in a way with two diagonal lines splitting it up like an X.

### **Simulation**
I started the design on the board and tested it in simulation. I wrote a testbench that powers up the design, applies a reset, and feeds it a clock signal. The simulation shows clk, rst, hsync, vsync, vid_on, row, col, red, green and blue. My rows value is 0 while my columns value is counting up in 1s. Also with the addition of blue, red and green it helps create the colours, inside green and red you can see an F which basically shows and tells that they are combining to create yellow to start the simulation with the colour yellow.
<img width="1044" height="421" alt="image" src="https://github.com/user-attachments/assets/6b5e8485-b80d-44b8-bd5c-76271a74b04e" />

### **Synthesis**
After simulation, I synthesised the design, which turns the Verilog code into the actual hardware parts the FPGA has, such as logic blocks and flip-flops. I then ran implementation, where the tool places those parts on the chip and wires them together. I checked the timing report to make sure the design meets timing at the 25 MHz pixel clock, and I checked the utilisation report to see how much of the chip the design uses. Finally, I generated the bitstream, which is the file that configures the FPGA, and loaded it onto the board to test the VGA output on a monitor. Zoomed in to find out that the outputs for J17 and J18 are J17 = vgaGREEN_OBUF and J18 = vgaBlue_OBUF so these are the VGA colours output buffers.
<img width="345" height="496" alt="image" src="https://github.com/user-attachments/assets/a6218366-d1fe-4c1e-baf5-b1d48af7b51e" />
<img width="802" height="317" alt="image" src="https://github.com/user-attachments/assets/b68e63d6-a9bd-4b05-b1a2-01f9ad87e546" />
<img width="499" height="367" alt="image" src="https://github.com/user-attachments/assets/201cee32-149d-48f0-958a-ec314c58d7d8" />
<img width="479" height="354" alt="image" src="https://github.com/user-attachments/assets/7f1de0c8-751a-473b-8f0c-64cc33ec46c4" />



### **Code Adaptation**
Briefly show how you changed the template code to display a different image. Demonstrate your understanding. Guideline: 1-2 short paragraphs.

### **Demonstration**
If you get your own design working on the Basys3 board, take a picture! Guideline: 1-2 sentences.

## **More Markdown Basics**
This is a paragraph. Add an empty line to start a new paragraph.

Font can be emphasised as *Italic* or **Bold**.

Code can be highlighted by using `backticks`.

Hyperlinks look like this: [GitHub Help](https://help.github.com/).

A bullet list can be rendered as follows:
- vectors
- algorithms
- iterators

Images can be added by uploading them to the repository in a /docs/assets/images folder, and then rendering using HTML via githubusercontent.com as shown in the example below.

<img src="https://raw.githubusercontent.com/melgineer/fpga-vga-verilog/main/docs/assets/images/VGAPrjSrcs.png">
