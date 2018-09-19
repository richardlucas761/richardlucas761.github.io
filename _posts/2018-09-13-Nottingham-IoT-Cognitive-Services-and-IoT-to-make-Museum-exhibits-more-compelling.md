# [Nottingham IoT : Cognitive Services and IoT to make Museum exhibits more compelling.](https://www.meetup.com/Nottingham-IoT-Meetup/events/253751297/)

## When was the last time to visited your local museum?

> Martin Kearn will talk about how museums are under increasing pressure to become commercially viable whilst modernising themselves and appealing the insta-generation. This is the story of how Microsoft worked with Black Radley to create the ‘intelligent exhibit’ IoT device. This is a Raspberry Pi device which adds artificial intelligence to museum exhibits by tailoring the audio description to the age of the exhibit visitor. It does this whilst logging insightful analytics data on the back end which tracks visitors as they traverse the museum. This is a tale of IoT, cloud, cardboard and museum artefacts from the 1800’s.

> Martin Beeby of Oracle (who formally worked on the project while at Microsoft) will talk about the difficulties of developing IoT applications and connecting them to the cloud when you are in a museum with an internet connection that would be better suited to the Jurassic era.

Martin and Martin (!) talked about the work they had done creating an interactive museum system which used a camera to detect when a person (face) was looking at an exhibit and play audio which was appropriate to the age of the person. A child would have a different audio file played to them than an adult, for example.

Their system was installed at the Shrewsbury Museum and Art Gallery, built from a Raspberry Pi3 running Microsoft's IoT Core operating system and costing around £100. The system used the Azure Cognitive Services to determine the age of the person viewing the exhibit and the built in face recognition software in Windows to notice when a face was looking at the exhibit (the Azure service was needed to provide more information on the age of the person viewing).

The system could track a unique face (accurate to a certain degree) and provide visitor information about which exhibits people had visited and their estimated age.

The challenges of having a device with a camera as it's only input device were presented, they were using QR codes scanned by the camera to update the system with a new URL for audio files. The device also read out it's current IP address using text-to-speech, it's only output device being the speakers.

## "Edge Case" testing device

Martin Beeby described the creation of a steampunk arcade machine which was used at Microsoft events to test whether websites were compatible with the Microsoft Edge browser.

The device was based around a Raspberry Pi2, an Ada Fruit display, a DMX controller for the lighting on the arcade machine and even a thermal printer to provide users with a printout of their testing results. The software was written in Node.JS and Python.

Martin described the problems of getting good quality WiFi at customer sites or at conference venues, particularly for a device with limited input and output devices, similar to the museum system described above.

To work round these limitations there are some interesting alternatives in having a local machine learning server running Tensor Flow although the system requires training before use. An alternative is to use a Movidius USB device which can be trained in the cloud and then downloaded to a USB device. Both these approaches getting round the limitation of having to have a good internet connection.

## Links

[@martinkearn on Twitter](https://twitter.com/martinkearn)

[@thebeebs on Twitter](https://twitter.com/thebeebs)

[Using Cognitive Services to make museum exhibits more compelling and track user behavior, Microsoft Technical Case Study](https://microsoft.github.io/techcasestudies/cognitive%20services/2017/08/04/BlackRadley.html)

[Microsoft Admiral Edge Case](http://wemakeawesomesh.it/edgecase.html)

[Tensor Flow](https://www.tensorflow.org/)

[Movidius USB](https://developer.movidius.com/)