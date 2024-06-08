---
layout: post
title: RFID types of tags
date: 2024-06-08 10:00:00 +0000
description: oday we'll talk about RFID tags, its internal components and how they're classified.
img: rfid_part2/cover.jpg
fig-caption: # Add figcaption (optional)
tags: [RFID]
---

Hey,\
Hi friend, nice to see you again!

This is the second post in a series about RFID and you can find the previous one [here]({{site.baseurl}}/lets-talk-about-rfid-part1/).

Today we'll talk about RFID tags, its internal components and how they're classified. Hope you enjoy.
<br />


# Types of tags

RFID tags can be categorized in many ways:
* internal power support: active, passive or semi-passive.
* memory type: read-write, read-only or write-once read-many (WORM)
* communication frequency: Low Frequency, High Frequency or Ultra High Frequency


## Energy support

### Active tags

Active tags have an internal energy source, like a battery, that powers on the microchip and an active transmitter, due to this, this kind of tag can have more memory capacity and the ability to generate it's own signal to transfer data, being able to be detected and transmit to really long distances, of up to 100m. They can also be divided in two subgroups:

* Transponder: remains inactive and "awakes" when detects the radio signal of a reader, transmitting the response as soon as are awake.
* Beacon: always awake, emitting signals at predefined intervals.

<figure style="display: inline-block;">
  <img style="vertical-align: top;" src="{{site.baseurl}}/assets/img/rfid_part2/active_tag.png" alt="RFID active tag">
  <figcaption style="text-align: center;">RFID active tag - Source: [1]</figcaption>
</figure>


### Passive tags

Passive tags don't have an internal energy souce nor an active transmitter, so they have to use the electromagnetic field created by the reader to generate electricity to power on the microchip and to transmit the response back to the reader, a physical process that will be discussed later. Due to this they have a smaller memory capacity and a really small working distance.

Due to the very low production cost; usually just a simple microchip, copper wire and pvc/plastic; passive tags are the most found on the market and the most implemented in projects, therefore, more emphasis will be placed on them.

<figure style="display: inline-block;">
  <img style="vertical-align: top;" src="{{site.baseurl}}/assets/img/rfid_part2/passive_tag.png" width="75%" height="75%" alt="RFID passive tag">
  <figcaption style="text-align: center;">RFID passive tag - Source: [2]</figcaption>
</figure>


### Semi-passive tags

Semi-passive tags, or Battery-Assisted Passive (BAP) tags, are a hybrid between active and passive tags. They have their own energy source that powers up the microchip and assists in the communication, but don't have an active transmitter, and due to this, they need the electromagnetic field created by the reader to transmit the response back. As the battery powers the microchip, they can have bigger memories and don't need to extract energy from reader's field, which allows them to respond to weaker signals and to work with longer distances than the passive tags.

<figure style="display: inline-block;">
  <img style="vertical-align: top;" src="{{site.baseurl}}/assets/img/rfid_part2/semi_passive_tag.png" alt="RFID semi-passive tag">
  <figcaption style="text-align: center;">RFID semi-passive tag - Source: [3]</figcaption>
</figure>


## Memory type

**Read-only (RO):** The memory can only be read and the data in it is created during its manufacturing

**Read-write (RW):** The memory can be written and rewritten as many times as necessary. RW memories also have a RO space where some information about the tag is stored.

**Write-once read-many (WORM):** THe memory can only be written once. WORM memories also have a RO space where some information about the tag is stored.


## Communication frequency

As said before, RFID communicates through radio waves, and one of its properties is frequency. Broadly speaking, frequency refers to the number of occurrences of an event in a given period of time, in our case, frequency is the number of oscillations per second of the wave. Thus, passive tags operate mainly in three frequency bands: Low Frequency (LF), High Frequency (HF) or Ultra High Frequency (UHF).

**Low Frequency:** Operates mainly in bands between 125 kHz to 134 kHz. Provides a short reading range, up to 10 cm, and a slow reading speed, but is very resistant to interference, from metals and liquids for example.

**High Frequency:** Operates mainly in the band of 13.56 MHz. Provides a medium reading range, up to 1 m, and an intermediate reading speed, but suffers more interference then the low frequency. The so famous NFC tecnology (Near-Field Communication), present in public transportation, contactless payments and smartphones, operates in this frequency, and this is not just a coincidence, NFC standards and protocols are based in the RFID standards, such as ISO/IEC 14443.

**Ultra High Frequency:** Operates mainly in the bands between 856 MHz to 960 MHz. Provides a long reading range, up to 10 m, and a fast reading speed, but suffers a lot with interference.

<figure style="display: inline-block;">
  <img style="vertical-align: top;" src="{{site.baseurl}}/assets/img/rfid_part2/frequency.jpg" alt="Communication frequencies example">
  <figcaption style="text-align: center;">Communication frequencies example - Source: [4]</figcaption>
</figure>


# References

[1] [https://learn.sparkfun.com/tutorials/rfid-basics/all](https://learn.sparkfun.com/tutorials/rfid-basics/all)\
[2] [https://ae01.alicdn.com/kf/HTB1_vIVKpXXXXcBXXXXq6xXFXXXW/RFID-Thick-Card-Mango-125KHz-Thick-Card-Access-Control-System-Card.jpg](https://ae01.alicdn.com/kf/HTB1_vIVKpXXXXcBXXXXq6xXFXXXW/RFID-Thick-Card-Mango-125KHz-Thick-Card-Access-Control-System-Card.jpg)\
[3] [https://www.researchgate.net/figure/A-typical-semi-passive-tag-with-an-internal-battery-116_fig3_339643122](https://www.researchgate.net/figure/A-typical-semi-passive-tag-with-an-internal-battery-116_fig3_339643122)\
[4] [https://www.impinj.com/products/technology/how-can-rfid-systems-be-categorized](https://www.impinj.com/products/technology/how-can-rfid-systems-be-categorized)\

