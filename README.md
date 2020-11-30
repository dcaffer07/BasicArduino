# BasicArduino
I'm going to learn how to use an Arduino, and make awesome things with it!


## TableofContents
* [TableOfContents](#TableOfContents)
* [HelloArduino](#HelloArduino)
* [FiniteLEDBlink](#FiniteLEDBlink)

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

### Evidence

### Image or Wiring

### Reflection
