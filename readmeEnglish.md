# Belial01
This project aims to continue the legacy of the multiplatform Diskmag Exilium (Belial 01), under an ATMEGA328 (arduinocade).<br>
First we need a hardware platform, which in this case, will be the arduinocade (Peter Barrett).<br>
In order to bring the platform closer to the maximum number of people, a first design will be made under an ARDUINO ONE board without the need to change the 16 Mhz glass (sacrificing color), as well as the greater compatibility of pins and hardware of the arduinocade.<br>
<ul>
 <li><a href='#arduinoide'>IDE Arduino<a/></li>
 <li><a href='#hardware'>Hardware<a/></li>
 <li><a href='#video'>Video<a/></li>
 <li><a href='#mixer'>Audio mixer<a/></li>
 <li><a href='#joystick'>Test joystick ATARI<a/></li>
 <li><a href='#jukebox'>Jukebox<a/></li> 
 <li><a href='#html5'>HTML5<a/></li>
 <li><a href='#box'>Console<a/></li>
</ul>

<br><br>
<a name="arduinoid"><h2>IDE Arduino</h2>>/a>
Tests have been carried out with the IDE 1.8.11.
<br><br>
  
<a name="hardware"><h2>Hardware</h2><a>
An ARDUINO ONE plate is used, equipped with ATMEGA328, so it would also be worth DUEMILANOVE or NANO, respecting the location of the pins.<br>
The same pins as the arduinocade will be used:
<ul>
  <li>Video - D1 and 9</li>
  <li>Audio - D6</li>
</ul>
The specific pins of the arduino will be left free for the future:
<ul>
 <li>A4,A5 - I2C to connect EEPROM LC256</li>
 <li>13,12,11- ISP programmer</li>
 <li>D2 and D3 - PS/2 keyboard</li>
</ul>
For the joystick we'll use:
<ul>
 <li>ATARI - A0,A1,A2,A3,D4 and D5</li>
</ul>
The pins and the infrared module have been removed from the arduinocade, but we will use ATARI and AMSTRAD CPC standard controls instead.

<br><br>
<a name="video"><h2>Video</h2><a>
The SPI mode (Dave Schmenk) is used to generate video, similar to the arduinocade, but with the difference, of following with the same 16 Mhz crystal of the arduino, so that a signal is generated:
<ul>
 <li>CVBS RCA</li>
 <li>Black and white NTSC</li>
 <li>Hsync 63.55 microseconds</li>
 <li>320x200 pixels</li>
 <li>Tiles 40x25</li>
 <li>Single resistance 1 K and 470 ohms</li>
</ul>
The circuit to be carried out is as follows:
<center><img src="preview/previewVideoCircuit.jpg"></center>
<br><br>

<a name="mixer"><h2>Audio mixer</h2><a>
The audio of arduinocade is characterized by
<ul>
 <li>PWM - pin D6</li>
 <li>Mono output</li>
 <li>4 channels</li>
 <li>Resistance 100 K</li>
</ul>
I have decided to continue using pin 6 for compatibility, but I have replaced the 100 K fixed resistor with a 100 K logarithmic pontentiometer, which allows the volume to be adjusted.<br>
<center><img src="preview/previewSoundPotenciometer.jpg"></center>

  
  
