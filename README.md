# Bench Power Supply Barrel Connectors Adapter
## Disclaimer
I do not take any responsibilities for personal or property damage caused by 

## Introduction
This project started to solve the problem of seamlessly powering up devices through their DC jack using my bench power supply.

It receives power through banana plugs. Personally, I've decided it was the perfect way to power it because of the setup I'm running.
I highly doubt you found this page without going through [my video](https://youtu.be/uaTE9wOTJUA) first, so you probably already know what I'm talking about!

## Safety
### Handling
The board itself features lots of exposed solder and easy to short parts, it would be best to have an enclosure for it. However, you must keep in mind that
I have not designed such an enclosure yet, and it is currently not available.My recommendations for it would be to use simple brass standoffs, with two simple laser-cut acrylic plates above and below.

If you have a 3D printer you can probably design yourself a plastic enclosure with some slots to insert clear plastic sheets of any kind.

If you can't make yourself an enclosure, you will have to pay very close attention to where you place the board, or even wrap it in kapton tape if you're particularly forgetful about this kind of stuff.

### Power Rating
#### Absolute Maximum Rating
24V @ 3A
#### Further Details
I naturally don't have specific ratings for this board as several factors can affect it, nor have I performed any testing.

The polarity switch (SK22D15L5) is rated for a maximum of 50V @ 3A, or 150W.
The DC socket (DC-044K-D020) is rated 24V @ 7A, or 168W.
The voltage regulator (HT7525-1) is rated for a maximum input voltage of 30V. This means that this should be the hard voltage limit that cannot be exceeded without running the risk of frying the voltage regulators.

I know for a fact that 24V @ 3A is a very safe rating for this board. If your power supply can output 30V like mine does, it might be possible to power this with 30V @ 5A and still keep within the 150W limit of the polarity switch.
Exceeding 150W will begin heating up and potentially damaging the power switch, 
