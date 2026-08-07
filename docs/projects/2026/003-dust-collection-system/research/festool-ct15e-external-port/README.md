# Festool CT 15 E External Port

This page investigates existing designs for adding an external dust collection port to a Festool CTL 15 E.

The goal is to develop a solution that allows a cyclone separator to be connected while preserving the original functionality of the dust extractor. Where practical, the final design should use the OsVAC standard instead of proprietary hose connections.

## Design Objectives

- Compatible with the Festool CTL 15 E.
- Preserve the original airflow.
- Maintain the original hose connection.
- Add an external connection for a cyclone separator.
- Prefer OsVAC compatible connections.
- Modular and easy to print.
- Avoid permanent modifications where possible.

---

## Existing Designs

### Cults3D - Front Hose Port Extension for Festool CTM MIDI

**Source**

https://cults3d.com/en/3d-model/tool/front-hose-port-extension-for-festool-ctm-midi

**Image**

![Front Hose Port Extension](./_image/cults3d_front-hose-port-extension_festool-ctm-midi-1_w320.webp)
![Front Hose Port Extension](./_image/cults3d_front-hose-port-extension_festool-ctm-midi-2_w320.webp)

**Notes**

- Designed for the Festool CTM MIDI.
- Uses the original Festool hose interface.
- No OsVAC compatibility.
- Good inspiration for the overall concept.

---

### MakerWorld - Festool CT MIDI External Dust Port

**Source**

https://makerworld.com/nl/models/1377712-festool-ct-midi-external-dust-port

A split remix is also available, making the design easier to print.

**Image**

![Festool CT MIDI External Dust Port](./_image/makerworld_festool-ct-midi_external-dust-port_w320.webp)

**Notes**

- Designed for the Festool CT MIDI.
- Modular printable construction.
- Interesting approach for adapting to the CTL 15 E.

---

### Printables - Flexible Segmented Vacuum Hose Adapter for Festool

**Source**

https://www.printables.com/model/559792-flexible-segmented-vacuum-hose-adapter-for-festool

**Image**

![Flexible Segmented Vacuum Hose Adapter](./_image/printables_flexible-segmented-vacuum-hose-adapter_festool_w320.webp )

**Notes**

This design may provide an alternative approach for the internal connection between the Festool CTL 15 E and an external port.

The Festool side of the published adapter appears to use a female Festool hose connection. For use inside the CTL 15 E, this would likely need to be replaced by a male Festool connector that fits directly into the vacuum's internal hose connection.

At the opposite end, the existing hose or DN40 connection could be replaced by an OsVAC 40 interface.

The interesting part of this design is therefore primarily the flexible segmented section and not necessarily the original connectors at either end.

**Possible adaptation**

Festool CTL 15 E internal connection  
- male Festool connector  
- flexible segmented section  
- OsVAC 40 connector  
- external cyclone connection


### Printables - Hose Adapter Festool CT 15 to Oneida Ultimate Dust Deputy

**Source**

https://www.printables.com/model/437760-hose-adapter-festool-ct-15-to-oneida-ultimate-dust/related

**Image**

![Festool CT 15 to Oneida Ultimate Dust Deputy Adapter](./_image/printables_festool-ct15_oneida-ultimate-dust-deputy-adapter_w320.webp)

**Notes**

This design connects a Festool CT 15 directly to an Oneida Ultimate Dust Deputy.

The adapter is particularly interesting because it is specifically designed for the Festool CT 15, making it a useful reference for the Festool-side interface.

For this project, the Oneida connection could potentially be replaced by an OsVAC 40 interface while retaining the Festool connection geometry.

### Mullet Tools - Festool Connection Kits

**Source (CT MIDI / MINI)**

https://mullettools.com/products/festool-ct-midi-pipe-and-fittings-mullet-connection-kit

**Image**

![Festool CT MIDI and MINI Connection Kit](./_image/mullettools_festool-ct-midi-mini_connection-kit_w320.jpg ':size=320')

**Source (CT 15 / CT 25)**

https://mullettools.com/products/mullet-high-speed-cyclone-dust-collector-festool-ct15-e-adapter-assembly-kit

**Image**

![Festool CT 15 and CT 25 Connection Kit](./_image/mullettools_festool-ct15-ct25_connection-kit-1_w320.webp)
![Festool CT 15 and CT 25 Connection Kit](./_image/mullettools_festool-ct15-ct25_connection-kit-2_w320.webp)
**Notes**

Mullet Tools uses a custom component to connect the Festool dust extractor to a standard PVC pipe system.

The product descriptions differ between the two pages:

- The CT MIDI / MINI page describes the component as an **ABS** part.
- The CT 15 / CT 25 page describes the component as a **3D-printed custom adapter**.

At this stage it is unclear whether these are manufactured differently or whether the descriptions simply differ between the two product pages.

For this project, the custom Festool interface could potentially be redesigned to transition directly to an OsVAC 40 connection instead of the PVC system used by Mullet Tools.