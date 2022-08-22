# ChasingLEDpatterns

Abstract:

Most of us have seen the chasing LED patterns around a marquee sign on the street or the entrance of a store. Our project is to make an advanced version of chasing LED patterns on a marquis sign border that can switch the pattern by pressing the push button. Our design is to configure 3 different patterns in the device. One can be the chasing pattern starting from the middle of the top of the board to the middle of the bottom, the other one can be a chasing pattern starting from the middle of the bottom of the board to the middle of the top, and the third one can be a chasing pattern on each side respectively and synchronously. The shape of the LED pattern we choose is square which is a matrix with the size of 8×8. The chasing LED feature can be achieved by using a delay function. The method to light on the correct position of LED can be achieved by using a “LED matrix method” which is illustrated below. Overall, the goal of our project is to display three different LED chasing patterns on a marquis border switch by pressing the corresponding button which attracts people’s attention.

Specifications:

A list of tentative specifications:
1. An 8×8 LED matrix would be connected with two MCUs. We will use an ATmega328PA to
achieve this.

2. There are 8 columns and 8 rows which results in an 8×8 LED matrix. Therefore, 16 terminals should be connected with the MCU. According to the schematic, LED row terminals are the positive part of the LED, whereas LED column terminals are the negative part of the LED. So if we want a specific LED turned on, the positive terminals (row terminal) should be set to 1, and the negative terminals (column terminal) should be set to 0. 

3. For each status, we created a specific matrix. For example, if we want the position of
(0,0) lighted, we will use the matrix that the (0,0) is 1 and other points are all 0. This
means only the point (0,0) will be lit. According to this, each status has its specific matrix.

4. We made a loop to repeat 50 times quickly (would not be noticed by eyes) to go through this 8×8 matrix, to check which position is 1. When 1 is observed, the second point(2.) will be used to that point. So that the LED at the specific point will be lit.

5. To achieve the “chasing” pattern, our algorithm is firstly to assign the matrix that we
expected. The corresponding LED will be lit. Then, with the delay function,
that LED will be turned on for 1 second. After lighting, the next expected matrix will be
assigned to the output. Another LED will be lit. Since the LED will be turned on as soon
as the previous one is turned off, the pattern would be regarded as “chasing”.
6. There is a button that is able to control the status of our product. When pressing the button, our product would be turned on.

7. There are three patterns of our LED matrix and are controlled by a button. When the user pressed the button the first time, the LEDs would be turned on starting from the top middle to the bottom middle. When the button is pressed for the  second time, the LEDs would be turned on starting from the bottom middle to the top middle. When the button is pressed for the third time, the LEDs should be lit on a chasing pattern on each side simultaneously. There are 3 figures to explain our 3 patterns below.
