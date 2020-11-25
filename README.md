# BasicArduino
I'm going to learn how to use an Arduino, and make awesome things with it!


## TableofContents
* [TableOfContents](#TableOfContents)
* [HelloArduino](#HelloArduino)
* [FiniteLEDBlink](#FiniteLEDBlink)

## HelloArduino

### Description & Code

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
write a reflection here, remember that it should be usefull, not a diary entry.

## FiniteLEDBlink

### Description & Code

```C++
Code Goes Here
```

### Evidence

### Image or Wiring

### Reflection
