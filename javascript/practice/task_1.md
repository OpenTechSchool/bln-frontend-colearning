##JS Calculations

#### Problem One: Vegetable Market

A gardener is selling his harvest on the vegetable market. He is selling vegetables for **N** Dollar per Kilo and fruits for **M** Dollar per Kilo. Write a program that calculates the earnings of the harvest in **Euro**. (Assume that 1 Euro is equal to 2.94 Dollar).

**Input**

Four arguments are passed to the function:

```bash
    Vegetable price per kilogram – a floating-point number.
    Fruit price per kilogram – a floating-point number.
    Total kilograms of vegetables – an integer.
    Total kilograms of fruits – an integer.
```

Constraints: all numbers will be within the range from 0.00 to 1000.00.

**Expected Output** 

Print on the console one floating-point number: the earnings of all fruits and vegetables in Euro.

Clarification for the first example:

    Vegetables cost: 0.194$ * 10 kg. = 1.94 $
    Fruits cost: 19.4 $  * 10 kg. = 194 $
    Total: 195.94 $ = 101 Euro

👉 Guidelines: 

- Go through the problem requirements. 
- In this case, we have to calculate the total income from the harvest. It equals the sum of the earnings from the fruits and vegetables which can be calculated by **multiplying the price per kilogram by the quantity**. The input is given in Dollars and the output should be in Euros. It is assumed that 1 EUR equals 1.94$, therefore, to get the wanted output value, you have to **divide** the sum by 1.94.
  
👉 Choose the Data Types

After having a clear idea of how to solve the task, you can continue with choosing appropriate data types. 
- Go through the input: there are two integers for total kilograms of vegetables and fruits, therefore, and the variables that have to be declared to store their values can be converted to numbers with **parseInt(…)**. 
- The prices of the fruits and vegetables are said to be **floating-point numbers** and therefore, the variables will be converted by using the method **parseFloat(…)**.


#### Problem Two: OTS Classroom

An **OTS Classroom** has a rectangular size lenght x width meters, without columns on the inside. The room is divided into two parts- **left** and **right**, with a hallway approximately in the middle. 
- In both parts, there are **rows** with **desks**. 
- In the back of the room, there is a big entrance door. In the front, there is a podium for the teacher. 
- A single student's seat takes up 70 x 120 cm (a table with size 70 x 40 cm + space for a chair and passing through with size 70 x 80 cm). 
- The hallway width is at least 100 cm. It is calculated that due to the entrance door (which has 160 cm opening) exactly one working space is lost, and due to the podium (which has a size of 160 x 120 cm) exactly two working spaces are lost.
  
👉  **Write a program** that reads the size of the student's seats as input parameters and calculates the number of working places in it.

Input Data

- The program reads two numbers (arguments), one per line: l (length in meters) and w (width in meters).
```bash
Constraints: 3 ≤ w ≤ l ≤ 100.
```
####Output 

Print an integer in the console: the number of working places in the training lab.

Clarification 

- the room length is 1500 cm. 12 rows can be situated in it (12 120 cm = 1440 + 60 cm difference). The hall width is 890 cm. 100 cm of them are for the hallway in the middle. The rest 790 cm can be situated by 11 desks per row (11 \ 70 cm = 770 cm + 20 cm difference). Number of places = 12 * 11 - 3 = 132 - 3 = 129 (we have 12 rows with 11 working places = 132 minus 3 places for podium and entrance door).

- room length is 840 cm. 7 rows can be situated in it (7 * 120 cm = 840, no difference). The hall width is 520 cm. 100 cm from them is for the hallway in the middle. The rest 420 cm can be situated by 6 desks per row (6 * 70 cm = 420 cm, no difference). Number of places = 7 * 6 - 3 = 42 - 3 = 39 (we have 7 rows with 6 working places = 42 minus 3 places for podium and entrance door).

🛑 First build an idea for its solution, before having started to write code. 
- Check the problem requirements. 
- Write a program that calculates the number of working places in a OTS Classroom, where the number depends on the room length and height. 
- The input data will be in meters and the information about how much space the working places and hallway take, will be in centimeters. - - To do the calculations, use the same measuring units, no matter whether you have to choose to convert length and height into centimeters or the other data in meters.  



#### Problem Three: Place Tiles

On the ground in front of an apartment building tiles need to be placed. The ground has a square shape with a side of N meters. The tiles are "W" meters wide and "L" meters long. There is one bench on the ground with a width of "M" meters and a length of "O" meters. There is no need to place tiles under it. Each tile is replaced for 0.2 minutes.

👉 **Write a program that reads from the console the size of the ground, the tiles and the bench, and calculates how many tiles are needed to cover the ground and what is the total time for placing all of the tiles.**

**Example:**
 A ground with size 20 m has an area of 400 m2m^2m​2​​. A bench that is 1 m wide and 2 m long, has an area of 2 m2m^2m​2​​. One tile is 5 m wide and 4 m long and has an area of 20 m2m^2m​2​​. The space that needs to be covered is 400 - 2 = 398 m2m^2m​2​​. 398 / 20 = 19.90 tiles are necessary. The time needed is 19.90 * 0.2 = 3.98 minutes.
Input Data

👉 5 arguments are passed to the function:

   - N – length of a side of the ground within the range of [1 … 100].
   - W – width per tile within the range of [0.1 … 10.00].
   - L – length per tile within the range of [0.1 … 10.00].
   - M – width of the bench within the range of [0 … 10].
   - O – length of the bench within the range of [0 … 10].


Some details: 

    - Total area = 20 * 20 = 400.
    - Area of the bench = 1 * 2 = 2.
    - Area for covering = 400 – 2 = 398.
    - Area of tiles = 5 * 4 = 20.
    - Needed tiles = 398 \/ 20 = 19.9.
    - Needed time = 19.9 * 0.2 = 3.98.

**Hints** 👇 🤔

It is required to calculate the number of tiles that have to be placed, as well as the time for placing them. To find that number, it has to be calculated the area that needs to be covered and divide it by the area per tile. 
👉 🤔 By the requirements of the problem, the ground is square, therefore, you find the total area by multiplying its side by its value **` N * N`**. 
After that, calculate the area that the bench takes up by multiplying its two sides as well **`M * O`**.

🏮 After subtracting the area of the bench from the area of the whole ground, we obtain the area that needs to be repaired.

👉 Calculate the area of a single tile by multiplying its two sides with one another **`W * L`**. 
👉 Divide the area for covering by the area of a single tile. This way, we find the number of necessary tiles. 
👉 Multiply it by 0.2 (the time needed for changing a tile). 