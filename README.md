**The Humble Hygrometer: DHT22’s Tale of Temp and Moisture**

Greetings, esteemed tinkerer! Welcome to a repository where the air spills its secrets, courtesy of the mighty DHT22 sensor. 
This Arduino sketch is your ticket to becoming the meteorologist you never knew you could be—tracking temperature and humidity with the precision of a hawk and the charm of a quirky inventor. 
It’s less about weather forecasts and more about proving you can eavesdrop on the atmosphere. Let’s dive into this delightful dance of data!

**What’s This Gadget Up To?**

This project harnesses the DHT22 sensor (plugged into pin 2) to measure humidity and temperature, then beams the results to your Serial Monitor like a proud parent showing off report cards.
Every two seconds, it whispers, “Here’s the humidity, here’s the temp,” in a loop so reliable you could set your watch to it—if watches cared about dew points.

**
The Star of the Show**

DHT22 Sensor (Pin 2): The diva of environmental sensing, delivering humidity and temperature stats with a dramatic flair.
Arduino: The trusty stagehand, keeping the sensor’s performance on cue.

**The Code: A Breath of Fresh C++**

#include "DHT.h"

#define DHTPIN 2     // Pin where DHT22 is connected
#define DHTTYPE DHT22  // Specify the sensor type

DHT dht(DHTPIN, DHTTYPE);

void setup() {
  Serial.begin(9600);
  Serial.println(F("DHT22 !!")); // A triumphant hello

  dht.begin(); // Curtain up, sensor on!
}

void loop() {
  float temperature = dht.readTemperature();
  float humidity = dht.readHumidity();

  Serial.print(F("Humidity: "));
  Serial.print(humidity);
  Serial.print(F("%  Temperature: "));
  Serial.print(temperature);
  Serial.println(F("°C "));

  delay(2000); // A brief interlude before the next act
}

**Getting Started: Sniff the Air Like a Pro

Prerequisites**

An Arduino (Uno, Nano, or whatever’s not buried in your junk drawer)
A DHT22 sensor (because DHT11 is just too basic)
The DHT library by Adafruit (install it, or this won’t work—trust me)
Jumper wires and a breadboard (soldering optional, chaos guaranteed)
The Arduino IDE (no, you can’t upload this with sheer willpower)
A curiosity for what’s floating in your room’s air

**Hardware Setup**

Connect the DHT22 to pin 2 (data pin), VCC to 5V, GND to ground. Add a 10kΩ pull-up resistor between VCC and the data pin—because sensors are needy.
Plug your Arduino into your computer like it’s a lifeline to the outside world.
Pray the humidity isn’t 100% from your nervous sweating.
**Installation**

git clone https://github.com/trish004/DHT22.git

Install the DHT library via the Arduino IDE: Sketch > Include Library > Manage Libraries > Search "DHT22 example".
Open the .ino file and upload it to your board faster than you can say “relative humidity.”
Usage: Become the Weather Whisperer
Fire it up, open the Serial Monitor (9600 baud), and watch the numbers roll in like a weather ticker.
Wave a damp cloth or blow hot air (carefully!) to see the sensor react—science in action!
Adjust the delay(2000) if you’re impatient or just want to feel the pulse of the air more often.

**Why This Exists**

Because who doesn’t want to know if their room is secretly a sauna? Perfect for IoT enthusiasts, data nerds, or anyone who’s ever wondered, 
“Is it me, or is it hot in here?” Plus, it’s a stepping stone to smarter projects—like a plant-watering bot or a “should I open the window?” alarm.

**Contributing: Make It Rain (Ideas)**

Got a tweak to add wind speed, graph the data, or make the sensor sing its readings? Fork this repo, sprinkle your genius, and send a pull request. Just don’t flood me with bugs—literal or otherwise.

**License**
MIT License—because sharing is caring, and I’m not about to dampen your creative spirit. Use it, tweak it, show it off at your next tech gathering.

**Final Gust**
This project is proof that even the air has stories to tell, and you’ve got the tools to listen. 
So grab your Arduino, channel your inner climatologist, and let’s measure the world—one humid breath at a time. 

**Happy tinkering, you atmospheric alchemist!**

