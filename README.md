# usb_mapping.json # The Logical USB Project 🔌

Let’s be brutally honest: trying to figure out USB versions and specs shouldn't feel like reading a military cockpit manual. 

The USB Implementers Forum (USB-IF) has turned what should be a simple cable standard into an absolute, certified dumpster fire of corporate branding. Because of marketing politics and retroactive gaslighting, **USB 3.0**, **USB 3.1 Gen 1**, and **USB 3.2 Gen 1** are all the *exact same* 5 Gbps technology from 2008. They literally just kept renaming old tech so companies could print "New!" on the box without upgrading the hardware.

We are completely bypassing the corporate marketing gibberish. This project is a simple, open-source JSON dictionary that maps their messy corporate nonsense into a logical, predictable, human-readable standard.

---

## The Sane Naming Standard

Our system follows a basic rule that a human brain can actually process: **The major version defines the architecture era, and the generation defines the speed iteration.** No retroactive renaming allowed.

| What it should be called | Real-World Speed | What the USB-IF calls it (The Mess) |
| :--- | :--- | :--- |
| **USB 2.0 Gen 1** | 480 Mbps | USB 2.0 (High-Speed) |
| **USB 3.0 Gen 1** | 5 Gbps | USB 3.0 / USB 3.1 Gen 1 / USB 3.2 Gen 1 |
| **USB 3.0 Gen 2** | 10 Gbps | USB 3.1 Gen 2 / USB 3.2 Gen 2 |
| **USB 3.0 Gen 3** | 20 Gbps | USB 3.2 Gen 2x2 |
| **USB 4.0 Gen 1** | 20 Gbps | USB4 Gen 2x2 |
| **USB 4.0 Gen 2** | 40 Gbps | USB4 Gen 3x2 / USB4 40Gbps |

---

## How to Use the Data

If you are a developer building a hardware database, a retail scraper, a system utility, or you just want to build a browser extension that fixes product listings on Amazon, use our master mapping file. 

Grab the raw data layer here:
 `usb_mapping.json`

### Quick JSON Example
```json
{
  "logical_name": "USB 3.0 Gen 2",
  "usb_if_marketing_name": "SuperSpeed USB 10Gbps",
  "usb_if_technical_names": ["USB 3.1 Gen 2", "USB 3.2 Gen 2"],
  "max_speed_gbps": 10.0,
  "common_connectors": ["USB-A", "USB-C"]
}
