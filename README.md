# Bench Power Supply Barrel Connectors Adapter
![1](https://github.com/ItalianRetroGuy/Bench-Power-Supply-Barrel-Connectors-Adapter/assets/88715197/fa855f4c-2573-4bd2-a9c9-c6c8294b6c86)
![2](https://github.com/ItalianRetroGuy/Bench-Power-Supply-Barrel-Connectors-Adapter/assets/88715197/2c4f788f-9e33-4fdb-84c3-d03dc2147eed)

## Disclaimer
I do not take any responsibilities for personal harm or property damage caused by building or using this project. Make sure to read my safety recommendations down below.

## Introduction
This project started to solve the problem of seamlessly powering up devices through their DC jack using my bench power supply.

It receives power through banana plugs. Personally, I've decided it was the perfect way to power it because of the setup I'm running.
I highly doubt you found this page without going through [my video](https://youtu.be/uaTE9wOTJUA) first, so you probably already know what I'm talking about!

## Use Cases
I mainly use this for powering retro consoles through their DC jacks, because of their reduced current draw and voltage requirement. It might be possible to power laptops too but only while idling, as they tend to have a much higher current draw which could exceed the capabilities of the board. Also, some laptops can detect it's not the original charger (don't ask me how, I assume the charger sends some info when plugged in) and refuse to let power in.

The polarity switch is useful for devices like the Sega Game Gear which require a different connector polarity based on their region, but generally speaking retro consoles come from a time where it was very likely to find negative-sleeve connectors. When working on a lot of them you might find yourself needing to switch it quite a few times.

## Compatibility
This adapter can be powered via banana plugs (male). It can work with any universal connector set that can be powered via 5.5mmx2.1mm DC plugs (male), as long as you own a male-to-male 5.5mmx2.1mm barrel plug adapter.

## Recommended Connectors and Adapters (Affiliate Links)
* [Male-to-male 5.5mmx2.1mm barrel plug adapter](https://s.click.aliexpress.com/e/_DD6vQwD) <ins>***WARNING: THIS CABLE IS ONLY RATED FOR 12V @ 3A***</ins>
* [Universal connectors set](https://s.click.aliexpress.com/e/_DEg6efL) <ins>***WARNING: THESE CONNECTORS ARE ONLY RATED FOR 90W***</ins>

## Assembly
### Instructions
Assembling this should be very straightforward, there are markings on the board that will help you place every component down properly.
* LED orientation is marked on the board like a regular diode.
* The resistors have no required orientation
* The electrolytic capacitors have the negative side marked on the board.
* The voltage regulators are TO-92 packages and they have the flat side marked down on the board.
* The DC socket cannot be placed in the wrong way.
* The polarity switch has the actuator drawn on the board but you can also rotate it to make it harder to be accidentally flicked. If you somehow prefer you can even mount it on the other side of the board.
* The banana sockets are slightly more complicated, you can see a bit of how I did in [my video](https://youtu.be/uaTE9wOTJUA) for this project. I recommend making sure the solder starts slightly poking out of the holes on the other side of the board, acting like tiny rivets. This is to ensure a very strong mount that is taking advantage of the entire board strength.
### Bill of Materials
[You can download the bill of materials from here](/bom/benchpsu_barreljack_adapter.csv)
### PCB
[You can order the PCB directly from PCBWay](https://www.pcbway.com/project/shareproject/Barrel_Connector_Adapter_for_Bench_Power_Supplies_b430900c.html), or [you can download](/grb/grb.zip) the gerber files required for manufacturing.

I recommend choosing a white or red solder mask color, as it boosts the red light coming from the LEDs.

## Instructions
### Powering a Device
* Read and become familiar with the safety information and power ratings down below
* Insert the positive banana plug coming from the bench power supply in the adapter's positive (red, or marked V+) banana socket
* Insert the negative banana plug coming from the bench power supply in the adapter's negative (black, or marked V+) banana socket
* Insert one end of a male-to-male 5.5mmx2.1mm barrel plug adapter inside the adapter's DC socket marked J3
* Attach the connector you need at the other end of the male-to-male barrel plug adapter
* Ensure the adapter board is not touching and cannot touch any conductive object or surface
* Enable power output from the bench power supply to the adapter
* Select appropriate connector wiring using the selection switch
* Plug the connector in the device which must be powered

## Safety
### Precautions
* Do not reverse the positive and negative banana plugs, the board might not survive that
* Set a current limit or overcurrent protection of 3A on your bench power supply when using this adapter, or always be ready to cut power to the adapter board immediately
* Follow the handling recommendations listed below
* Do not exceed the power rating listed below
* Keep the board unpowered when not in use to avoid accidental shorts

### Handling
The bare adapter board must be kept away from any conductive object or surface. It has many easy to short points, and it would be best to have an enclosure for it. However, you must keep in mind that
I have not designed such an enclosure yet, and as such it is currently not available.

My recommendations for it would be to use simple brass standoffs, with two simple laser-cut acrylic plates above and below.
If you have a 3D printer you can probably design yourself a plastic enclosure with some slots to insert clear plastic sheets of any kind.

If you can't make yourself an enclosure, you will have to pay very close attention to where you place the board, or even wrap it in kapton tape if you're particularly forgetful about this kind of stuff.

### Power Rating
#### Important Notes
All ratings discussed here only refer to this adapter board. This doesn't apply to any kind of cable, adapter, or connector that you use with this board. Using wires, adapters, or connectors with an inferior rating can cause them to melt or catch on fire if their own rating is exceeded.

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
* Exceeding ANY OF THESE, MAY cause personal injury, property damage, or start fires.

##### Should these limits somehow be exceeded
* The board MIGHT tolerate exceeding Wattage or Amperage ratings, it MIGHT tolerate exceeding 24V, but it will NEVER tolerate exceeding 30V.
* Monitor the temperature of the adapter board at all times while exceeding any limit, and make sure to be ready to cut power immediately.


## Dimensions
**Dimension** | **Value** | **Notes**
--- | --- | ---
Board Size | 66mm x 66mm
Hole Pattern Spacing | 54mm
Hole Distance From Center to Board Corner Edges | 6mm | Measured before adding fillets
Board Fillet Radius | 9mm
Mounting Hole Diameter | 3.2mm
Mounting Hole Conductive Ring Thickness | 1.2mm
