# Bench Power Supply Barrel Connectors Adapter
## Disclaimer
I do not take any responsibilities for personal harm or property damage caused by building or using this project. Make sure to read my safety recommendations down below.

## Introduction
This project started to solve the problem of seamlessly powering up devices through their DC jack using my bench power supply.

It receives power through banana plugs. Personally, I've decided it was the perfect way to power it because of the setup I'm running.
I highly doubt you found this page without going through [my video](https://youtu.be/uaTE9wOTJUA) first, so you probably already know what I'm talking about!

## Safety
### Precautions
* Always be ready to cut power to the adapter board immediately
* Follow the handling recommendations listed below
* Do not exceed the power rating listed below

### Handling
The board itself features lots of exposed solder and easy to short parts, it would be best to have an enclosure for it. However, you must keep in mind that
I have not designed such an enclosure yet, and it is currently not available. My recommendations for it would be to use simple brass standoffs, with two simple laser-cut acrylic plates above and below.

If you have a 3D printer you can probably design yourself a plastic enclosure with some slots to insert clear plastic sheets of any kind.

If you can't make yourself an enclosure, you will have to pay very close attention to where you place the board, or even wrap it in kapton tape if you're particularly forgetful about this kind of stuff.

### Power Rating
#### Important Notes
All ratings discussed here only refer to this adapter board. This doesn't apply to any kind of cable, adapter, or connector that you use with this board. Using wires, adapters, or connectors with an inferior rating can cause them to melt or catch on fire.

#### Absolute Maximum Rating
24V @ 3A

#### Further Details
I naturally don't have specific ratings for this board as several factors can affect it, nor have I performed any testing.

**Part #** | **Description** | **References** | **Power Rating**
--- | --- | --- | ---
SK22D15L5 | DPDT Polarity Switch | SW1 | 50V @ 3A (150W)
DC-044K-D020 | DC Socket | J3 | 24V @ 7A (168W)
HT7525-1 | LDO Voltage Regulator | U1, U2 | 30V
KS106M050C07RR0VH2FP0 | Electrolytic Capacitor | C1, C2, C3, C4 | 50V

##### According to these ratings this means that
* Exceeding 24V WILL EVENTUALLY damage the DC Socket or heating it up more than it should
* Exceeding 30V WILL damage the LDO Voltage Regulators, which might end up causing further damage to the adapter or whatever you're powering with it.
* Exceeding 50V WILL EVENTUALLY damage the Polarity Switch or heating it up more than it should
* Exceeding 50V WILL blow up the electrolytic capacitors, which could end up causing personal injury
* Exceeding 3A WILL EVENTUALLY damage the Polarity Switch or heating it up more than it should
* Exceeding 7A WILL EVENTUALLY damage the DC Socket or heating it up more than it should
* Exceeding 150W WILL EVENTUALLY damage the Polarity Switch or heating it up more than it should
* Exceeding 168W WILL EVENTUALLY damage the DC Socket or heating it up more than it should
* Exceeding ANY OF THESE, MAY cause personal injury, property damage, or fires.

##### Should these limits somehow be exceeded
* The board MIGHT tolerate exceeding Wattage or Amperage ratings, it MIGHT tolerate exceeding 24V, but it will NEVER tolerate exceeding 30V.
* Monitor the temperature of the adapter board at all times while exceeding any limit, and make sure to be ready to cut power immediately.
