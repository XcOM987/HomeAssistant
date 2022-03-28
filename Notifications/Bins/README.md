# Bins Notifications

## Intro
This is the info on how I managed to get actionable notifications for my bins in Home Assistant using a mix of Node Red and Automations.

## Licences
Some images were used under licence and [designed by Frimufilms - Freepik.com](https://www.freepik.com) and will be atributed under each inital usage, note the GPL licence on here does not overrule any part of licences attached to the images, please see them for further info should you wish to use them.

This project is covered under the GPL3 licence found [here](https://github.com/XcOM987/HomeAssistant/blob/main/LICENSE)

## Thanks
Historically I've only ever used plain text notifications which wern't actionable, recently though I came across a twitter thread from a wizard known as James Callaghan which can be found [here](https://twitter.com/jamescallaghan/status/1502055840051863552), he wrote up a lovely thread about how he made HTML5 actionable noticiations (After much persistance from people like me asking how he did it).

You can find James':
- [Twitter](https://twitter.com/jamescallaghan)
- [Github](https://github.com/jcallaghan).

In my prep work I started looking up guides and details from other people who had done similar things, I checked out Everything Smart Home who has released a couple of videos historicaly about doing actionable notifications which can be [viewed here](https://www.youtube.com/watch?v=v8fcwhko1k4).

You can find Everything Smart home at:
- [Youtube](https://www.youtube.com/channel/UCrVLgIniVg6jW38uVqDRIiQ)
- [Twitter](https://twitter.com/EverySmartHome)
- [Website](https://everythingsmarthome.co.uk/)

I'd highly recommend giving them both a follow and a read/watch.

## Objectives
I wanted to set a list of objectives to work towards, these are:
- Notifications should be simple and easy to understand
- Quick to understand the notification from a quick glance
- Notification is to use the Moduler method within Node Red on my Home Assistant setup
- To be 100% within node red without any clutch methods to try and function
- To be actionable.

## Setup
My setup is all contained within Node Red which runs atop Home Assistant (HA), to get notifications on my Android device I use the HA companion App found within the Android App Store, for this to function correctly my HA instance has to be accessible to the outside world, there are many ways to achieve this, personally I have my system accessible via Nabucasa in addition to it being accessible via a load balancer which proxies requests and protects the server from unauthorised external access.

## Preperation

##### Researching
I begun by reading thorugh all of James' tweets abut the subject in question, and watched all of Everything Smart home's videos about notifications within Home Assistant.

##### Sourcing images
following this I gathered the images I wanted to use, I sourced them from [freepik](www.freepik.com)
For recycling I opted for [this image](https://www.freepik.com/free-vector/trash-waste-concept-with-food-glass-paper-realistic_7497465.htm#&position=5&from_view=undefined#position=2)[^1], and for waste bin I went for [this image](https://www.freepik.com/free-vector/trash-can-filled-with-garbage-bags-glasses-wine-plastic-bottles-banana-peels_9641595.htm#&position=8&from_view=undefined#position=4)[^2]

##### Modifying images

I decided on a maximum size of 250x500 as this would be a good size to provide enough detail and not be too large, it would also fill cards on Home Assistant nicely.

Once I have acquired my images I needed to make some modifications, I started by adding alpha layers to create transparancies, I also decided I had to change the colour of the bin to match mine to make it easier to see which bin it was at a glance, also so just so it matched, this was achieved in GIMP using the Hue and saturation tool, I added both images to a single file as seperate layers, and changed the opasicty to about 25% for the one I wanted grayed out, the result is below.
![Recycling](https://raw.githubusercontent.com/XcOM987/HomeAssistant/main/Notifications/Bins/Recycling.png)
![Waste](https://raw.githubusercontent.com/XcOM987/HomeAssistant/main/Notifications/Bins/waste.png)

## Node Red Notifications


[^1]: [Food vector created by macrovector - www.freepik.com](https://www.freepik.com/vectors/food)
[^2]: [Box vector created by frimufilms - www.freepik.com](https://www.freepik.com/vectors/box)
 
  Footnotes
[^note]:
    Named footnotes will still render with numbers instead of the text but allow easier identification and linking.  
    This footnote also has been made with a different syntax using 4 spaces for new lines.