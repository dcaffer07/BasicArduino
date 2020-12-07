# BasicArduino
I'm going to learn how to use an Arduino, and make awesome things with it!


## TableofContents
* [TableOfContents](#TableOfContents)
* [HelloArduino](#HelloArduino)
* [FiniteLEDBlink](#FiniteLEDBlink)
* [VariableLEDBlink](#VariableLEDBlink)


## HelloArduino

### Description & Code
This project being one of my first with aurduino, it was relativeley easy and writing the code.  First, I wrote code esuring a loop for the following things using void set  up.  I then connected the code to an LED light using the pinmode function, I then made the LED blink using delays, and finally by making the monitor show "BLINK" I put a serial begin to turn on my monitor, and then by using serial print I was able to make"Blink" print on the monitore. 

```C++
int LED = 13;


// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin 13 as an output.
  pinMode(LED, OUTPUT);
  Serial.begin(9600); // This turns on my Serial Monitor
  Serial.print("Hello World!");
  Serial.print("1...");
  Serial.print("2...");
  Serial.print("3...");
}

// the loop function runs over and over again forever
void loop() {
  
  Serial.println("Blink!");
  digitalWrite(LED, HIGH);           // turn the LED on (HIGH is the voltage level)
  delay(250);                       // wait for a second
  digitalWrite(LED, LOW);            // turn the LED off by making the voltage LOW
  delay(250);                       // wait for a second
}

```

### Evidence
[Here is my code on Arduino Create](https://create.arduino.cc/editor/dcaffer07/f99e84db-5dae-4b41-b6be-9c93e095c7b4)

### Image or Wiring
<img src="https://cdn-learn.adafruit.com/assets/assets/000/002/177/original/learn_arduino_fritzing_pin_13.jpg?1396780180" /> 

Image credit belongs to [Ada Fruit](https://learn.adafruit.com/assets/2177)

### Reflection
This assignment was very helpfull in getting me familiarized with aurduino uno.  I though that it was exteremly difficult at times, and it requitred some research and dedication to solve any problems i had, but i quess that is what engineering is about!  I am super excited to continue to work with aurduino and i look forward to more difficult assignments in the future.

## FiniteLEDBlink

### Description & Code
As I have learned from Mr.H and just general engineering, it is okay to use others ideas as long as you give them credit, proper citation, and understand what they did.  In this code, it first connects the LED bulb to the code, it then states how many times per second it needs to blink, and by 500, 500 x 2 =1000, this would mean once a second, it then says that given these facts the following code will operate.  Next it sayd void loop, and in this particular toime it says to repeat this loop of blinking once per second 5 times. That is the basis of the code and how it was built. 

```C++
  int ledPin = 13;
int blinkTime = 500;
bool eyesStinging=true;


void setup()
{
  pinMode(ledPin, OUTPUT);
if(eyesStinging)                         //Only blink if it's absolutely necessary
  blinkyBlinky(5, blinkTime); // 5 is number of blinks, blinkTime is the milliseconds in each state from above: int blinkTime = 500;
}

void loop()
{


  //
}

void blinkyBlinky(int repeats, int time)
{
  for (int i = 0; i < repeats; i++)
  {
    digitalWrite(ledPin, HIGH);
    delay(time);
    digitalWrite(ledPin, LOW);
    delay(time);
  }
}

```
Code Credit to KenF from aurduino.cc- [Here is the code](https://forum.arduino.cc/index.php?topic=273575.0)

### Evidence
[Here is the code on Arduino Create](https://create.arduino.cc/editor/dcaffer07/9f383a3b-047e-40ea-9aec-e91fe8d1928e)

### Image or Wiring
<img src="https://cdn.sparkfun.com/assets/learn_tutorials/3/1/0/Arduino_circuit_01_01.png" /> 


### Reflection
Although I really struggled to get my feet going, with the help of seeing and analyzing someone elses work, I was able to understand what I was doing.  I think that it was a super cool project once I got the hang of it, but like I said I found it pretty diffiucult at first.  Despite some troubles, this was a very fun project amd I look forward to writing new code in the future.

## Variable LED Blink

### Description and Code
The Variable Led Blink is desighned to begin blinking at 1 blink oer second and in order to get it to blink we begin with are standard blinking code.  From here you must use the delayVar code to make the blink slowy get faster.  We do this by making the delayVa5r less and less by subtracting 100milla secpns from each blink until it gets to 5 blinks per second at which point is stops and continues to blink at that rate.

```C++
  /* Karl Helmstetter
variable LED BLink
This should blink an LED faster and faster, until it reaches 5 blinks per second
*/

int ledPin = 8;
int delayVar = 1000;  //this variable is used for my delays.

void setup() {
  pinMode(ledPin,OUTPUT);    
}

void loop() {
    digitalWrite(ledPin, HIGH);           // turn the LED on (HIGH is the voltage level)
    delay(delayVar);                       // wait for a second
    digitalWrite(ledPin, LOW);            // turn the LED off by making the voltage LOW
    delay(delayVar);                       // wait for a second
    Serial.println(delayVar);
    delayVar = delayVar - 100;
    
    //as long as the delay is longer than 100 ms, we should continue to blink,
    // and we should also 
}
```
Code credit goes to Karl Helmstetter

### Evidence
[Here is the code on Arduino Create](https://create.arduino.cc/editor/dcaffer07/34819985-39c3-4c1b-9f74-63c1d841dd2d)

### Image or Wiring
<img src="https://raw.githubusercontent.com/rgabramedhin93/BasicArduino/main/Screenshot%202020-11-18%20at%204.16.05%20PM.png" /> 

### Reflection
It is super exciting to know that we are getting closer and closer to the end goal, that being the project.  This was a cool assignment that I addmittingly struggled with at first but eventually got the hang of with some example code.  I really enjoyed working through this and I look forward to more assignments in the future.
