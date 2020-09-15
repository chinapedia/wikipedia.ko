> This article is converted from Wikipedia: [초안:OFFer Project](https://ko.wikipedia.org/wiki/초안:OFFer_Project).


**OFFer**\[1\]*' : Cooking [IoT](../Page/사물인터넷.md "wikilink") System using Burner Remote Control and [NFC](../Page/근거리_무선_통신.md "wikilink")*'

OFFer is an [IoT](../Page/사물인터넷.md "wikilink") that remotely controls the [burner](https://ko.wikipedia.org/wiki/휴대용버너 "wikilink") handle by connecting Android application and [Arduino](../Page/아두이노.md "wikilink") via [Bluetooth](../Page/블루투스.md "wikilink") communication. OFFer has three functions: an off function that turns off the fire, a timer function that turns off the fire at the set time, and an automatic food timer function. The Off and Timer functions automatically turn off the burner, providing convenience and safety for all burners, indoors and outdoors, including camping sites. An automatic food timer lets you cook food remotely. This function is an extension of the existing timer function, suggesting various possibilities of OFFer. In addition, the OFFer is equipped with a gas sensor, which protects against the possibility of a fire caused by a gas leak.

# Introduction

As many modern people who are tired of repetitive life choose camping as a breakthrough in their daily lives, camping families are increasing. As a result, the camping market is growing and consumption of camping equipment is also increasing. In this regard, there is increasing interest in applying the Internet of Things ([IoT](https://ko.wikipedia.org/wiki/IOT "wikilink")) technology to the existing camping supplies. In this document, we researched portable burner among camping equipment and developed mobile application to remotely control portable [burner](../Page/휴대용_버너.md "wikilink"). Through the convergence of the camping industry and the IoT industry, which emerged as the main axis of the new market economy, it is possible to move away from the current IoT technology, which is mostly smart home, and apply it to existing devices, so that it can jump to the IoT technology as a broader meaning.\[2\] In this document, by incorporating IoT technology into the gas burner for camping, we have developed a service that can help to make the camping life safer and more convenient than before.



# Related Research

Devices that combine camping equipment and [IoT](../Page/사물인터넷.md "wikilink")\[3\] include [Bluetooth](../Page/블루투스.md "wikilink") speakers, safety devices to detect intrusions, and light gas leak detection sensors, but there are no devices related to the [burner](https://ko.wikipedia.org/wiki/휴대용버너 "wikilink") itself.

In fact, devices with functions like this study can be found in smart home systems. It can be attached to the gas valve to control the gas valve via [Bluetooth](../Page/블루투스.md "wikilink"). There is also a timer function but no cooking function and the price reaches 150,000 won. The most commercially available device\[4\] is a manual timer type, which is lower than the previously mentioned device, and sells for about 50,000 won on average, although users cannot control it or customize the timer. OFFer described in this document controls the knob of the gas burner, not the gas valve, and is different from the existing researches and devices in that it can be attached to the burner.\[5\]

# OFFer System Structure

The OFFer system proposed in this document consists of Android app and Arduino program for user service.

#### <big><u>Android App System Structure</u></big>

[대체글=](https://ko.wikipedia.org/wiki/파일:안드로이드_앱_시스템_구조.png "wikilink") The class of Android-based app for users consists of 2 activities and 4 fragments as shown in Figure 1.

##### \- Menu Activity

The Menu Activity is the first screen that appears when you run the app, as shown in Figure 2 and Figure 3. It is composed of connection UI so that Bluetooth connection with Arduino can be done through Bluetooth connection button. [대체글=](https://ko.wikipedia.org/wiki/파일:Figure2._Main,_Figure3._Connection.png "wikilink")
\===== - Bluetooth Activity ===== The Bluetooth Activity is an activity that contains the bluetooth connection and all the execution screens of the app, as shown in Figure 4. The bluetooth connection flow includes Bluetooth on / off status, device selection, socket creation, device connection, and socket deletion. When bluetooth is off, it automatically connects upon user approval and selects a device to connect. Create a socket through the [UUID](../Page/범용_고유_식별자.md "wikilink") and connect it with the device. When all is done, delete the socket.

There is a FrameLayout to hold four fragments. Each fragment can be displayed on the layout by clicking the button. There is also a communication function that allows Bluetooth communication with the device in each fragment. [대체글=](https://ko.wikipedia.org/wiki/파일:Figure4._Bluetooth_Activity.png "wikilink")

##### \- TurnOff Fragment

Fragment to turn off the burner. The UI consists of a single button, as shown in Figure 5. Pressing the button sends the data corresponding to the Off function to the Arduino. Press the button once to deactivate it. It can only be used once.

##### \- Control Fragment

Control Fragment is a Fragment functioning according to user's SeekBar control as shown in Figure 6. The UI is composed of SeekBar that can adjust the intensity of the intensity as shown in Figure 6 and text indicating the current intensity. While dragging SeekBar, the text indicating the current intensity is changed, and when dragging, the data corresponding to the intensity is transmitted to Arduino. [대체글=](https://ko.wikipedia.org/wiki/파일:Figure5._TurnOff,_Figure6._Control.png "wikilink")
\===== - Timer Fragment ===== The Timer Fragment is a Fragment with timer setting, operation and cooking functions as shown in Figure 7. As shown in Figure 8, the UI consists of a listview that selects minutes and seconds, a textview that shows the current time remaining, a button to create a dish, a list of cooking choices, and a cooking UI. [대체글=](https://ko.wikipedia.org/wiki/파일:Figure7._Cook_Timer,_Figure8._Progress.jpg "wikilink") If minutes and seconds are selected, the textview for the remaining time is modified accordingly and the timer starts. When 0 seconds have elapsed, data corresponding to Off is transmitted to Arduino.

Pressing the Create Cooking button sends the intensity control data to the Arduino according to the saved recipe. When the cooking time is over, the data corresponding to the Off function is sent to the Arduino, and the cooking UI changes to minutes, seconds, and remaining time UI.

##### \- HowTo Fragment

This fragment contains an image that shows how to use the OFFer app. [대체글=](https://ko.wikipedia.org/wiki/파일:OFFer_Demonstration_Video.png "wikilink")\]



#### <big><u>Arduino System Structure</u></big>

This chapter describes the connections between the Arduino and the sensors required for device design. The first Arduino model used was [UNO](https://ko.wikipedia.org/wiki/:en:Arduino_Uno "wikilink"). It is divided into Bluetooth module for Bluetooth communication ([HC-06](https://blog.naver.com/PostView.nhn?blogId=3demp&logNo=220195739907&parentCategoryNo=&categoryNo=41&viewDate=&isShowPopularPosts=true&from=search)), servo motor for intensity control ([MG995](https://kd3302.tistory.com/931)), gas detection module for gas detection ([MQ-2](http://blog.naver.com/PostView.nhn?blogId=damtaja&logNo=220155308097)), amplifier for sounding alarm ([LM386](https://ko.wikipedia.org/wiki/:en:LM386 "wikilink")) and speakers according to required functions. [대체글=](https://ko.wikipedia.org/wiki/파일:Figure9._Arduino_System_Structure.png "wikilink")

Pins 0 and 1 of Arduino Uno are used for serial communication with PC, so connect HC-06 and [RDX](https://ko.wikipedia.org/wiki/RDX "wikilink") (Data Receive) to No.3 and [TDX](https://ko.wikipedia.org/wiki/TDX "wikilink") (Data Transmit) to No.2 [GPIO](../Page/GPIO.md "wikilink") pin for Bluetooth communication. In Arduino Uno, servo pin can be controlled by digital pin through Servo library, but pin 9 and 10 are not available for PWM output, so use 8 as GPIO pin to send control signal of servo motor. The gas-detected result will receive analog data, so accept the analog input to A0 of Arduino's analog pins A0 to A5. The amplifier outputs a square wave by varying the frequency at a certain duty cycle. The GPIO pin used is digital number 9 pin. Finally, 5V and GDN are connected to all modules. To facilitate this, PCB boards are used and all modules are connected in parallel. It is also connected to the battery (9V), so it is possible to use only the battery without using an adapter.

Arduino's Bluetooth serial communication was performed at a baud rate of 9600. Likewise, mobiles have the same communication speed. The communication is ready and the data is sent from the mobile to the Arduino. If there is data received through serial, Arduino reads the received data and determines the angle of movement according to the value of this data. We rotate the servo motor with reference to the direction of the previous movement of the servomotor, the direction of the current movement, and the position of the current servomotor. At this time, the angle of the servomotor was changed by 1 degree and delayed to avoid the excessive movement of the servomotor. Read the gas value entered at A0 from MQ-2. This value is between 0 and 1024. If this value is higher than a certain value, it is assumed that gas is detected and an alarm is called. The alarm outputs the alarm sound to the speaker connected to the amplifier by using the tone function having the specified frequency for the specified time. After the alarm, the device is configured to send data via Bluetooth serial communication and disconnect the Bluetooth connection.

# Implementation Result

The user opens the app, connects the app and the Arduino device using the Bluetooth connection button, and executes each function through the menu at the bottom. There are four menus, off tab, control tab, timer tab and howto tab. The user can see how to use the app in the howto tab. The off tab has a button to turn off the burner. The user can always turn the fire off via the button but cannot turn it back on. The control tab has a seek bar that adjusts the intensity. The user adjusts the burner intensity by moving the seek bar. The timer tab has a regular timer and an automatic food timer. You can turn off the fire after a set time through the normal timer. An automatic food timer can run food stored in the app, and each food is automatically set to fire at a set time.

# Conclusion and Future Research

With the recent development of IoT technology, many smart home-related IoT products are being released. In this paper, we proposed an OFFer service that combines IoT technology with a gas burner to reduce the number of fire accidents that occur at campsites.

The OFFer can be scheduled to turn off the fire and has a function to detect gas leaks so that the gas burner can be used more safely. In addition, by setting the automatic cooking time, it is configured to automatically perform the uncontrolled in case of cooking a lot of use, it was configured to be used in a restaurant or restaurant where a recipe and cooking time is set.

However, the project is currently limited in that the burner design available is limited. Therefore, in the future, the hardware device will be manufactured in a flexible design to increase scalability, thereby increasing the portability of users.



# Introduction for Korean(Just for upload)

**근거리 통신과 버너 원격 제어를 이용한 쿠킹 IOT 시스템, 오퍼**

OFFer는 안드로이드 어플리케이션과 아두이노를 블루투스 통신을 통해 연결하여 버너 손잡이를 원격으로 조절하는 IOT이다. OFFer의 기능은 크게 3가지 이다. 불을 끄는 Off기능, 설정시간에 불이 꺼지는 타이머기능 그리고 자동 음식 타이머기능이다. Off와 타이머 기능은 버너의 불을 자동으로 꺼주므로 캠핑장을 포함한 실내외의 모든 버너 사용에 편리성과 안전성을 제공한다. 자동 음식 타이머는 음식을 원격으로 요리해주는 기능이다. 이 기능은 기존 타이머 기능의 확장기능으로 OFFer의 다양한 활용 가능성을 암시한다. 또한 OFFer는 가스 감지센서를 탑재해, 가스 누출로 인한 화재의 가능성으로부터 안전성을 갖추고 있다.

## 각주

1.
2.
3.
4.
5.