# BasicArduino
I'm going to learn how to use an Arduino, and make awesome things with it!


## TableofContents
* [TableOfContents](#TableOfContents)
* [HelloArduino](#HelloArduino)
* [FiniteLEDBlink](#FiniteLEDBlink)
* [VariableLEDBlink](#VariableLEDBlink)
* [OneButtonOneLED](#OneButtonOneLED)
* [TwoButtonsTwoLEDs](#TwoButtonTwoLED)
* [ServoControl](#ServoControl)


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

## VariableLEDBlink

### Description & Code
In this assignment, we were tasked with constructing code and the appropriate wiring so that an LED would blink faster and faster until it eventually remained constant.   It began at 1oooms on, and 100ms of, and than the breaks and blink times wiuld decrease by 100ms steadilly, so 900ms on and off, than 800ms on and off, and so on a so forth.  Once the code gets down to 100ms on and off, it will stay there and the times will no longer vary.  To do this you just use the simple on LED of LED loop code, however you use a delay var which allows for that 100ms decrease each time.  

```C++
  /* variable LED BLink
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
    
    //as long as the delay is longer than 100 ms, blinks continue, 
}
```

### Evidence
[Here is the code on Arduino Create](https://create.arduino.cc/editor/dcaffer07/34819985-39c3-4c1b-9f74-63c1d841dd2d)

### Image of Wiring
<img src="https://cdn.sparkfun.com/assets/learn_tutorials/3/1/0/Arduino_circuit_01_01.png" /> 


### Reflection
Cool Project.  I think that this one has helped us ease into the harder projects that are yet to come.  To be honest it is pretty mezmorizing to watch it Blink faster. So as I said I really enjoyed this project and I look forward to more projects in the future! 

## One Button One LED

### Description and Code
In this assignemnt, we were asked to make an LED blink everytime we hit a botton on our aurduiono.  You first do this by assigning the wring to the different areas to ensure an connection and a blink, i did this using pinmodes and inputs and outputs.  You then create the void setup so that the code knows what it is trying to do, ad then you craete a loop in which the LED turns on when the button is pushed.  It was a pretty straight forward assignment that was relatively easy to understand.

```C++
 int buttonPin = 2; // Pin connected to PushButton                                                                       
int ledPin = 13; // Pin connected to LED
int buttonState = 0; // Gives pushbutton a value

void setup() {
  
  pinMode(ledPin, OUTPUT); // Led-> Output
  pinMode(buttonPin, INPUT); // Led-> Input
}

void loop() {
  buttonState = digitalRead(buttonPin); // Read the given input from pin 2
  if(buttonState == HIGH) { // If i push button, set to be  high
    digitalWrite(ledPin, HIGH); // LED on
  }
  else{
    digitalWrite(ledPin, LOW); // If not on-> Off
  }
  }
```

### Evidence
[Here is the code on Arduino Create](https://create.arduino.cc/editor/dcaffer07/2d230442-b3cc-4759-961c-ced619a7f59b)

### Image of Wiring
<img src="https://www.arduino.cc/wiki/static/875a01f9d20a576acd5b7974e6339339/b2982/button.png" /> 

### Reflection
To be honest I found this assignment to be one of the easiest assignments that we have done so far.  I though that it was very straight forward, however it is super exciting to know that we are starting to get into the more advanced stuff.  I am super happy with how this assignment went, and I look forward to more like it in the future!

## Two Buttons Two LEDs

### Description and Code
Pretty straight forward, just make double of what I did last time.  The goal was to make the two LEDs light up when a button is pushed, and so all i did was make the connections to the breadboard different so that the 2nd LED had its own power supply and ID in the code, but otherwise the wiring was almost the same just simplified and doubled, as was the code, just simplified and doubled.

```C++
 // These are pin mubers/ enrgy suppliers and where they come from
// pin numbers:
const int buttonPin1 = 2;     // button1 pin
const int buttonPin2 = 4;     // button2 pin
const int ledPin2 =  8;       // LED2 Pin#
const int ledPin1 =  11;      // LED1 pin#


int buttonState = 0;         // Button status

void setup() {
  // LED pin as an output:
  pinMode(ledPin1, OUTPUT);
  // button pin as an input:
  pinMode(buttonPin1, INPUT_PULLUP);
  pinMode(ledPin2, OUTPUT);
  pinMode(buttonPin2, INPUT_PULLUP);
}

void loop() {
  // pushbutton value:
  buttonState = digitalRead(buttonPin1);

  // check if the pushbutton is pressed.
  // if it is, the buttonState is HIGH:
  if (buttonState == HIGH) {
    digitalWrite(ledPin1, LOW);
    delay(0);
    digitalWrite(ledPin1, HIGH);
    delay(0);
    digitalWrite(ledPin1, LOW);
  }

  // pushbutton value:
  buttonState = digitalRead(buttonPin2);

  // check if the pushbutton is pressed.
  // if it is, the buttonState is HIGH:
  if (buttonState == HIGH) {
    digitalWrite(ledPin2, LOW);
    delay(0);
    digitalWrite(ledPin2, HIGH);
    delay(0);
    digitalWrite(ledPin2, LOW);
  }
}
```

### Evidence
[Here is the code on Arduino Create](https://create.arduino.cc/editor/dcaffer07/7cffb45e-a83c-4e4f-b0f3-65d2ddc0a245)

### Image of Wiring
<img src="https://hacksterio.s3.amazonaws.com/uploads/attachments/869889/2leds_2pushbuttons_qrzfpJkZfK.jpg" /> 

### Reflection
I really enjoyed this project.  It wasn't too challenging, but it was still engaging.  I think that this project really helped me utilize my breadboard space, whcih sounds weird, but as the wiring has begun to become more and more complicating, it is important that I don't waste space (which will also be important when it comes to the portable button controlled servo project whcih requires good space management).  This was a super cool project, and I look forward to more tasks similar to this one.
