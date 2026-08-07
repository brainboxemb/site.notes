# Seeed Studio XIAO ESP32S3

This page contains the selected ESP32 board, LoRa hardware, expansion board, antenna options, suppliers and preliminary costs for the embedded development setup.

> Prices were checked in July 2026 and may change over time.

## Board Selection

The current choice is the Seeed Studio XIAO ESP32S3.

For use with the XIAO Expansion Board, the version with pre-soldered pin headers is preferred.

- [Seeed Studio — XIAO ESP32S3, pre-soldered](https://www.seeedstudio.com/Seeed-Studio-XIAO-ESP32S3-Pre-Soldered-p-6334.html)
- [Seeed Studio Wiki — XIAO ESP32S3](https://wiki.seeedstudio.com/xiao_esp32s3_getting_started/)

## LoRa Module

LoRa support is added with the Wio-SX1262 module.

- [Seeed Studio — XIAO ESP32S3 with Wio-SX1262](https://www.seeedstudio.com/Wio-SX1262-with-XIAO-ESP32S3-p-5982.html)
- [Seeed Studio Wiki — XIAO ESP32S3 and Wio-SX1262 Kit](https://wiki.seeedstudio.com/wio_sx1262_with_xiao_esp32s3_kit/)

The kit combines:

- XIAO ESP32S3
- Wio-SX1262 LoRa module
- Wi-Fi and Bluetooth through the ESP32S3
- LoRa and LoRaWAN support through the SX1262

The Wio-SX1262 version for the XIAO ESP32S3 uses a board-to-board connection and must be matched with the correct XIAO version.

## Expansion Board

The XIAO ESP32S3 and Wio-SX1262 combination can be installed on the Expansion Board Base for XIAO.

- [Seeed Studio — Expansion Board Base for XIAO](https://www.seeedstudio.com/Seeeduino-XIAO-Expansion-board-p-4746.html)
- [Seeed Studio Wiki — Expansion Board Base for XIAO](https://wiki.seeedstudio.com/Seeeduino-XIAO-Expansion-Board/)

The expansion board provides several useful development features, including:

- OLED display
- RTC
- Buzzer
- Push button
- MicroSD card slot
- Grove connections
- Battery connector and charging support

## Antennas

The XIAO ESP32S3 and Wio-SX1262 kit includes antennas for both radio systems:

- A 2.4 GHz antenna for Wi-Fi and Bluetooth
- An 868–915 MHz antenna for LoRa

The included antennas are small flexible antennas, commonly referred to as FPC antennas.

The included FPC antennas are suitable for initial development and testing. However, the preference for the final development setup is to use official Seeed Studio rod antennas.

### Included Antennas

| Antenna | Frequency | Use |
|---|---|---|
| Included FPC antenna | 2.4 GHz | Wi-Fi and Bluetooth |
| Included FPC antenna | 868–915 MHz | LoRa |

### Preferred Antenna Upgrade

- [Seeed Studio — 2.4 GHz rod antenna for XIAO](https://www.seeedstudio.com/2-4GHz-2-81dBi-Antenna-for-XIAO-ESP32C3-p-5475.html)
- [Seeed Studio — XIAO ESP32S3 with Wio-SX1262](https://www.seeedstudio.com/Wio-SX1262-with-XIAO-ESP32S3-p-5982.html)

| Antenna | Quantity | Status |
|---|---:|---|
| Official Seeed Studio 2.4 GHz rod antenna | 2 | Preferred upgrade |
| Official Seeed Studio 868–915 MHz rod antenna | 2 | Preferred upgrade |

Separate rod antennas do not have to be ordered immediately. The included FPC antennas can first be used to build and test the setup.

## Suppliers

### XIAO ESP32S3

| Supplier | Version | Headers | Price including VAT |
|---|---|---|---:|
| [Seeed Studio — XIAO ESP32S3, pre-soldered](https://www.seeedstudio.com/Seeed-Studio-XIAO-ESP32S3-Pre-Soldered-p-6334.html) | XIAO ESP32S3 | Pre-soldered | Approximately €9.00 |
| [Kiwi Electronics — XIAO ESP32S3, pre-soldered](https://www.kiwi-electronics.com/en/seeed-studio-xiao-esp32s3-pre-soldered-20408) | XIAO ESP32S3 | Pre-soldered | €9.43 |
| [TinyTronics — XIAO ESP32S3](https://www.tinytronics.nl/nl/development-boards/microcontroller-boards/met-wi-fi/seeed-studio-xiao-esp32-s3) | XIAO ESP32S3 | Without pre-soldered headers | €9.00 |

The TinyTronics version is not preferred because it does not have pre-soldered headers.

### Wio-SX1262

| Supplier | Product | Price including VAT |
|---|---|---:|
| [Seeed Studio — XIAO ESP32S3 with Wio-SX1262](https://www.seeedstudio.com/Wio-SX1262-with-XIAO-ESP32S3-p-5982.html) | Combined XIAO ESP32S3 and Wio-SX1262 kit | Approximately €11.50 |
| [Kiwi Electronics — Wio-SX1262 for XIAO](https://www.kiwi-electronics.com/en/wio-sx1262-voor-xiao-20459) | Separate Wio-SX1262 module | €5.43 |

### Expansion Board

| Supplier | Product | Price including VAT |
|---|---|---:|
| [Seeed Studio — Expansion Board Base for XIAO](https://www.seeedstudio.com/Seeeduino-XIAO-Expansion-board-p-4746.html) | Expansion Board Base for XIAO | Approximately €15.80 |
| [Kiwi Electronics — XIAO Expansion Board](https://www.kiwi-electronics.com/en/search?search=xiao%20expansion%20board) | Expansion Board Base for XIAO | €17.53 |
| [TinyTronics — Expansion Board for XIAO](https://www.tinytronics.nl/nl/development-boards/accessoires/adapter-boards/seeed-studio-expansion-board-voor-seeeduino-xiao) | Expansion Board Base for XIAO | €17.25 |

## Preliminary Seeed Studio BOM

The estimate assumes two identical development targets.

Each target consists of:

- One XIAO ESP32S3
- One Wio-SX1262
- One Expansion Board Base for XIAO
- The included 2.4 GHz FPC antenna
- The included LoRa FPC antenna

The combined XIAO ESP32S3 and Wio-SX1262 kit is used in the Seeed Studio estimate.

### Initial Setup

The initial setup uses the antennas included with the kits.

| Component | Quantity | Unit price | Subtotal |
|---|---:|---:|---:|
| XIAO ESP32S3 with Wio-SX1262 kit | 2 | $10.90 | $21.80 |
| Expansion Board Base for XIAO | 2 | $14.90 | $29.80 |
| Included 2.4 GHz FPC antenna | 2 | Included | — |
| Included LoRa FPC antenna | 2 | Included | — |
| **Product total** |  |  | **$51.60** |

At the exchange rate used in July 2026, the product total is approximately **€45.16 excluding VAT**.

### Preferred Setup

The preferred setup adds official rod antennas.

| Component | Quantity | Unit price | Subtotal |
|---|---:|---:|---:|
| XIAO ESP32S3 with Wio-SX1262 kit | 2 | $10.90 | $21.80 |
| Expansion Board Base for XIAO | 2 | $14.90 | $29.80 |
| Official 2.4 GHz rod antenna | 2 | $2.20 | $4.40 |
| Official LoRa rod antenna | 2 | $2.49 | $4.98 |
| **Product total** |  |  | **$60.98** |

At the exchange rate used in July 2026, the product total is approximately **€53.37 excluding VAT**.

## Seeed Studio Germany Warehouse Estimate

Shipping from the Germany warehouse avoids import charges because the products are already shipped from within the European Union.

| Setup | Products including VAT | Estimated shipping | Estimated total |
|---|---:|---:|---:|
| Initial setup with included FPC antennas | €54.64 | €10.00 | **€64.64** |
| Preferred setup with rod antennas | €64.58 | €10.00 | **€74.58** |

The final shipping price and warehouse availability must be checked during checkout.

## Seeed Studio China Warehouse Estimate

Since July 2026, e-commerce shipments entering the European Union with a value of no more than €150 are subject to a fixed import duty of €3 per product category.

VAT may be collected by Seeed Studio during checkout. Otherwise, VAT and import charges may be collected by the carrier when the parcel enters the Netherlands.

A carrier may also charge an additional administration or customs-clearance fee. That possible fee is not included below.

### Initial Setup from China

The initial BOM contains two product types:

| Product type | Import duty |
|---|---:|
| XIAO ESP32S3 with Wio-SX1262 kit | €3.00 |
| Expansion Board Base for XIAO | €3.00 |
| **Estimated import duty** | **€6.00** |

| Cost | Low estimate | Expected estimate | High estimate |
|---|---:|---:|---:|
| Products | €45.16 | €45.16 | €45.16 |
| Shipping from China | €10.00 | €15.00 | €20.00 |
| Import duty | €6.00 | €6.00 | €6.00 |
| Subtotal before VAT | €61.16 | €66.16 | €71.16 |
| VAT, 21% | €12.84 | €13.89 | €14.94 |
| **Estimated order total** | **€74.00** | **€80.05** | **€86.10** |

A provisional budget of approximately **€80.00** can be used for the initial setup from the China warehouse.

### Preferred Setup from China

The preferred BOM contains four product types:

| Product type | Import duty |
|---|---:|
| XIAO ESP32S3 with Wio-SX1262 kit | €3.00 |
| Expansion Board Base for XIAO | €3.00 |
| 2.4 GHz rod antenna | €3.00 |
| LoRa rod antenna | €3.00 |
| **Estimated import duty** | **€12.00** |

| Cost | Low estimate | Expected estimate | High estimate |
|---|---:|---:|---:|
| Products | €53.37 | €53.37 | €53.37 |
| Shipping from China | €10.00 | €15.00 | €20.00 |
| Import duty | €12.00 | €12.00 | €12.00 |
| Subtotal before VAT | €75.37 | €80.37 | €85.37 |
| VAT, 21% | €15.83 | €16.88 | €17.93 |
| **Estimated order total** | **€91.20** | **€97.25** | **€103.30** |

A provisional budget of approximately **€100.00** can be used for the preferred setup from the China warehouse.

The exact number of product categories depends on how the products are declared by Seeed Studio and the carrier.

## Preliminary Kiwi Electronics BOM

Kiwi Electronics sells the XIAO ESP32S3, Wio-SX1262 and Expansion Board as separate products.

The listed package contents indicate that antennas are included with the XIAO ESP32S3 and Wio-SX1262. Separate rod antennas are therefore not included in this initial BOM.

| Component | Quantity | Unit price excluding VAT | Subtotal excluding VAT |
|---|---:|---:|---:|
| [XIAO ESP32S3, pre-soldered](https://www.kiwi-electronics.com/en/seeed-studio-xiao-esp32s3-pre-soldered-20408) | 2 | €7.79 | €15.58 |
| [Wio-SX1262 for XIAO](https://www.kiwi-electronics.com/en/wio-sx1262-voor-xiao-20459) | 2 | €4.49 | €8.98 |
| [Expansion Board Base for XIAO](https://www.kiwi-electronics.com/en/search?search=xiao%20expansion%20board) | 2 | €14.49 | €28.98 |
| **Product total excluding VAT** |  |  | **€53.54** |
| **VAT, 21%** |  |  | **€11.24** |
| **Product total including VAT** |  |  | **€64.78** |

### Estimated Kiwi Electronics Total

| Shipping method | Shipping including VAT | Estimated order total |
|---|---:|---:|
| PostNL letterbox package | €4.22 | €69.00 |
| PostNL parcel | €7.20 | €71.98 |
| DHL parcel | €8.46 | €73.24 |

The complete order may be too large for letterbox shipping. Parcel shipping is therefore the safer estimate.

A provisional delivered price of approximately **€72.00** can be used for planning.

The Kiwi BOM uses the included FPC antennas. Official rod antennas can be added later as an upgrade.

## Cost Comparison

| Supplier or warehouse | Antenna configuration | Estimated total |
|---|---|---:|
| Seeed Studio, Germany warehouse | Included FPC antennas | Approximately €64.64 |
| Kiwi Electronics | Included FPC antennas | Approximately €72.00 |
| Seeed Studio, Germany warehouse | Preferred rod antennas | Approximately €74.58 |
| Seeed Studio, China warehouse | Included FPC antennas | Approximately €80.05 |
| Seeed Studio, China warehouse | Preferred rod antennas | Approximately €97.25 |

The Germany warehouse appears to be the cheapest option when all components are available there.

Kiwi Electronics may still be the simpler option because:

- It ships from the Netherlands
- The XIAO boards have pre-soldered headers
- The required test antennas are included
- Prices are shown directly in euros
- No import processing is required

## Proposed Setup

### Initial Setup

| Component | Quantity |
|---|---:|
| XIAO ESP32S3, pre-soldered | 2 |
| Wio-SX1262 for XIAO ESP32S3 | 2 |
| Expansion Board Base for XIAO | 2 |
| Included 2.4 GHz FPC antenna | 2 |
| Included 868–915 MHz LoRa FPC antenna | 2 |

### Preferred Setup

| Component | Quantity |
|---|---:|
| XIAO ESP32S3, pre-soldered | 2 |
| Wio-SX1262 for XIAO ESP32S3 | 2 |
| Expansion Board Base for XIAO | 2 |
| Official Seeed Studio 2.4 GHz rod antenna | 2 |
| Official Seeed Studio 868–915 MHz rod antenna | 2 |

## Notes

-