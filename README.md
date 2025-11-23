# Midland G18 PRO Documentation

[![PMR446 Compliant](https://img.shields.io/badge/PMR446-Compliant-green)](https://en.wikipedia.org/wiki/PMR446)
[![Documentation](https://img.shields.io/badge/docs-comprehensive-blue)](docs/)
[![License](https://img.shields.io/badge/license-Unlicense-blue)](https://unlicense.org/)

> **DISCLAIMER: UNOFFICIAL DOCUMENTATION**
>
> This documentation is unofficial and represents independent research about the
> Midland G18 PRO radio. While information has been verified against official
> manuals where possible, it may contain errors, omissions, or inaccuracies.
>
> **USE AT YOUR OWN RISK**. The author assumes no liability for damages,
> injuries, regulatory violations, or other consequences resulting from use of
> this information. Always consult official Midland documentation and comply
> with applicable radio regulations in your jurisdiction.

Comprehensive documentation for the **Midland G18 PRO PMR446 radio**, including
user manuals, frequency tables, programming profiles, and best practices for
tactical and recreational use.

## Quick Start

**New to the G18 PRO?** Start here:

1. **Read the basics**: [Key Specifications](#key-specifications) below
2. **Check frequencies**: [PMR446 Frequency Table](#pmr446-frequencies)
3. **Configure your radio**: [Hybrid Profile Guide](docs/guides/HYBRID_PROFILE.md)
4. **Program advanced features**: [PRG-G15 Programming Guide](docs/guides/PROGRAMMING.md)

## Key Specifications

| Feature | Specification |
|---------|---------------|
| **Certification** | IP67 (waterproof 1m/30min, dust-proof) |
| **Power Output** | ≤500mW ERP (both Low/High modes) |
| **Frequencies** | 16 PMR446 channels (446.00625-446.19375 MHz) |
| **Channels** | 99 configurations (16 base + 83 with CTCSS) |
| **Battery** | 7.4V Li-ion 1600mAh rechargeable |
| **Battery Life** | 16-20 hours (90% RX, 10% TX) |
| **Weight** | 240g (with battery) |
| **Dimensions** | 113mm × 56mm × 38mm (antenna excluded) |
| **SAR Rating** | 0.982 W/Kg |

**Note**: "99 channels" refers to channel configurations, not separate
frequencies. The radio uses 16 physical frequencies with CTCSS tone filtering
to create 99 selectable channel options.

## Documentation Structure

### Core Guides

* **[Hybrid Profile Configuration](docs/guides/HYBRID_PROFILE.md)** - Versatile setup
  balancing tactical and recreational features
* **[Tactical Operations Guide](docs/guides/TACTICAL_OPERATIONS.md)** - Settings,
  protocols, and procedures for tactical team use
* **[PRG-G15 Programming Guide](docs/guides/PROGRAMMING.md)** - Complete programming
  software reference

### Reference Materials

* **[Channel List](docs/reference/CHANNELS.md)** - Complete 99-channel configuration table
* **[Documentation Index](docs/README.md)** - Folder map for guides, manuals, references
* **Official Manuals**
  * **English**: [PDF (official)](docs/manuals/MANUAL_G18_PRO_EN.pdf) |
    [Markdown](docs/manuals/MANUAL_G18_PRO_EN.md) ⭐ *Enhanced with diagrams, tables, clickable TOC*
  * **German**: [PDF](docs/manuals/MANUAL_G18_PRO_GER.pdf) |
    [Markdown](docs/manuals/MANUAL_G18_PRO_GER.md) ⭐ *Enhanced with tables, clickable TOC*
  * **French**: [PDF](docs/manuals/MANUAL_G18_PRO_FRA.pdf)
  
  > 📄 **Note**: Markdown versions are professionally formatted transcripts of the official PDFs
  > with enhanced readability, embedded radio diagrams, searchable text, and clickable navigation.
  > Transcribed with best effort for accuracy — always refer to the official PDF for authoritative information.
* **[Operational Checklists](checklists/)** - Pre-Mission, Mission Execution,
  Post-Mission

## PMR446 Frequencies

The G18 PRO operates on **16 PMR446 channels** (446.00625-446.19375 MHz).

| Channel | Frequency (MHz) | Channel | Frequency (MHz) |
|---------|-----------------|---------|-----------------|
| 1 | 446.00625 | 9 | 446.10625 |
| 2 | 446.01875 | 10 | 446.11875 |
| 3 | 446.03125 | 11 | 446.13125 |
| 4 | 446.04375 | 12 | 446.14375 |
| 5 | 446.05625 | 13 | 446.15625 |
| 6 | 446.06875 | 14 | 446.16875 |
| 7 | 446.08125 | 15 | 446.18125 |
| 8 | 446.09375 | 16 | 446.19375 |

**Important Limitations:**

* **PMR446 band only** - Cannot receive/transmit outside 446.0-446.2 MHz
* **Not a wideband scanner** - Cannot access FRS (462-467 MHz) or other bands
* **Fixed power output** - Both Low and High modes output ≤500mW ERP per
  regulations
* **License-free** - Legal to operate in Europe without license

See [CHANNELS.md](docs/reference/CHANNELS.md) for complete 99-channel list with CTCSS tones.

## Quick Reference

### Default Button Assignments

* **PF3 (Short Press)**: Monitor - Opens squelch to hear weak signals
* **PF4 (Long Press)**: Scan - Cycles through all programmed channels
* **Emergency Button (3-sec hold)**: Emergency alarm (must enable via PRG-G15)

### Basic Menu Settings

Access via MENU button on front panel:

* **POW**: Toggle Low/High power (both = 500mW ERP)
* **SQL**: Adjust squelch level (0-9)
* **VOX**: Enable/disable voice activation
* **TOT**: Set transmission timeout (30-270 seconds)
* **C-CDC/R-CDC/T-CDC**: Configure CTCSS/DCS privacy tones

### Advanced Programming (PRG-G15 Software)

Requires **Midland PRG-G15 Programming Kit C1131** (€36):

* [Official Midland Store](https://www.midlandeurope.com/en_150/products/prg-g15)
* [Software Download](https://support.midlandeurope.com/en_150/products/g18-pro)

**Programmable Features:**

* CTCSS/DCS codes (50 CTCSS + 105 DCS)
* PF3/PF4 button assignments
* Emergency button enable/disable
* FM Radio receiver mode
* ROGER BEEP, VOICE prompts, Compander
* Busy Channel Lockout (BCL)
* VOX sensitivity, TOT, Squelch levels

See [PROGRAMMING.md](docs/guides/PROGRAMMING.md) for complete guide.

## Use Cases

### Tactical Teams

* Emergency alarm for distress signaling
* Channel scanning for situational awareness
* CTCSS/DCS tones for group isolation
* BCL prevents interfering with critical communications
* See [Tactical Operations Guide](docs/guides/TACTICAL_OPERATIONS.md)

### Hiking & Recreation

* Monitor function to locate group in weak signal areas
* Scanning to find most active channel
* Emergency features for safety backup
* 16-20 hour battery life for extended trips
* See [Hybrid Profile](docs/guides/HYBRID_PROFILE.md)

### Emergency Preparedness

* Emergency alarm provides distress signaling
* Channel scanning locates active emergency communications
* Battery optimization extends operational time
* IP67 waterproofing for harsh conditions

## Range Performance

**Note**: Range identical for both Low and High power modes (≤500mW ERP).

| Environment | Typical Range | Notes |
|-------------|---------------|-------|
| **Open Terrain** | Up to 12+ km | Line of sight, no obstructions |
| **Forest/Hills** | 4-6 km | Trees, moderate obstructions |
| **Urban Areas** | 1-2 km | Buildings and structures |
| **Buildings** | Varies | Reduced by metal construction |

Coverage depends on terrain, obstructions, antenna position, weather, and
interference.

## Safety and Best Practices

* Always perform pre-operation radio checks
* Monitor battery levels and carry spares
* Use appropriate power levels for your situation
* Follow radio etiquette and communication protocols
* Test emergency features regularly
* Never operate without proper antenna attached
* Maintain safe distance during transmission (SAR: 0.982 W/Kg)
* Store radios in dry, temperature-controlled environments

## Additional Resources

### Official Sources

* **Product Page**:
  [Midland G18 PRO](https://www.midlandeurope.com/en_150/products/g18-pro)
* **Support Page**:
  [G18 PRO Support](https://support.midlandeurope.com/en_150/products/g18-pro)
* **Programming Kit**:
  [PRG-G15 C1131](https://www.midlandeurope.com/en_150/products/prg-g15) (€36)

### This Repository

* **Detailed Guides**: See [docs/guides/](docs/guides/) folder
* **Checklists**: See [checklists/](checklists/) folder
* **Reference Tables**: See [docs/reference/](docs/reference/) folder
* **Official Manuals**: PDFs and transcripts in [docs/manuals/](docs/manuals/) folder

## Contributing

Found an error or have additional information? This is a community resource.
Contributions welcome via pull requests or issues.

## License

This documentation is released into the public domain under the [Unlicense](UNLICENSE).
Use freely for any purpose.
