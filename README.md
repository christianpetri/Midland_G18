# Midland G18 Radio Complete Documentation

[![PMR446 Compliant](https://img.shields.io/badge/PMR446-Compliant-green)](https://en.wikipedia.org/wiki/PMR446)
[![Documentation](https://img.shields.io/badge/docs-available-blue)](#table-of-contents)
[![License](https://img.shields.io/badge/license-Unlicense-blue)](https://unlicense.org/)

> **DISCLAIMER: UNOFFICIAL DOCUMENTATION**
>
> This documentation is unofficial and represents independent research about the
> Midland G18 PRO radio. While information has been verified against official manuals
> where possible, it may contain errors, omissions, or inaccuracies.
>
> **USE AT YOUR OWN RISK**. The author assumes no liability for damages, injuries,
> regulatory violations, or other consequences resulting from use of this information.
> Always consult official Midland documentation and comply with applicable radio
> regulations in your jurisdiction.

A comprehensive resource for the **Midland G18 PRO PMR446 radio**, including user
manuals, frequency tables, programming profiles, and best practices for tactical
and recreational use.

**Key Specifications:**

* **IP67 Certified**: Waterproof up to 1m depth for 30 minutes, dust-proof
* **Power Output**: ≤500mW ERP (both low and high power modes)
* **Frequencies**: 16 PMR446 frequencies (446.00625 - 446.19375 MHz)
* **Channels**: 99 configurations (16 base + 83 with pre-programmed CTCSS tones)
* **Battery**: 7.4V Li-ion 1600mAh rechargeable pack
* **Weight**: 240g (battery included)
* **Dimensions**: 113mm × 56mm × 38mm (antenna excluded)

**Note**: "99 channels" refers to channel configurations, not separate frequencies.
The radio uses 16 physical frequencies with CTCSS tone filtering to create 99
selectable channel options. See `docs/CHANNELS.md` for details.

## Table of Contents

* [Frequency Information](#frequency-information)
  * [Frequency Limitations](#frequency-limitations)
  * [PMR446 Frequency Table](#pmr446-frequency-table)
* [Hybrid Profile Configuration](#hybrid-profile-for-midland-g18-radio)
  * [Profile Overview](#profile-overview)
  * [Configuration Guide](#complete-configuration-guide)
  * [Use Case Optimization](#use-case-optimization)
  * [Performance Specifications](#performance-specifications)
  * [Programming Instructions](#programming-instructions)
* [Tactical Team Operations](#tactical-team-operations-and-settings)
  * [Team Checklists](checklists/) - Dedicated checklist files
  * [Operational Settings](#settings-for-tactical-operations)
  * [Button Settings](#programmable-function-pf-button-settings)
* [PMR446 Compliance and Technical Specifications](#pmr446-compliance-and-technical-specifications)
* [Safety and Best Practices](#safety-and-best-practices)

## Frequency Information

### Frequency Limitations

#### Operating Band Restrictions

The Midland G18 PRO operates exclusively within the PMR446 frequency band (446.00625 - 446.19375 MHz). The radio cannot receive or transmit on frequencies outside this designated range.

#### Important Notes

* The G18 PRO is not a wideband scanner
* FRS frequencies (462-467 MHz, North American standard) are not accessible
* The radio is designed for PMR446 compliance and cannot be modified for other bands
* Attempting to operate outside PMR446 frequencies may violate local regulations

### PMR446 Frequency Table

The G18 PRO supports **99 total PMR446 channels**: 16 base channels plus 83
pre-programmed channels with CTCSS tones. See `docs/CHANNELS.md` for the complete
channel list.

**16 Base PMR446 Channels:**

| Channel | Frequency (MHz) | Notes                  |
|---------|------------------|------------------------|
| 1       | 446.00625        | Default PMR446 channel |
| 2       | 446.01875        |                       |
| 3       | 446.03125        |                       |
| 4       | 446.04375        |                       |
| 5       | 446.05625        |                       |
| 6       | 446.06875        |                       |
| 7       | 446.08125        |                       |
| 8       | 446.09375        |                       |
| 9       | 446.10625        |                       |
| 10      | 446.11875        |                       |
| 11      | 446.13125        |                       |
| 12      | 446.14375        |                       |
| 13      | 446.15625        |                       |
| 14      | 446.16875        |                       |
| 15      | 446.18125        |                       |
| 16      | 446.19375        |                       |

## Hybrid Profile for Midland G18 Radio

This versatile configuration profile balances tactical and recreational
features, making it ideal for users who need reliable communication across
various scenarios including hiking, tactical operations, emergency preparedness,
and general use.

### Profile Overview

The Hybrid Profile is designed for maximum flexibility while maintaining
optimal performance and battery efficiency. It provides:

* **Tactical readiness** with quick-access emergency features
* **Recreational functionality** for hiking and outdoor activities
* **Optional FM Radio** receiver (requires PRG-G15 software configuration)
* **Emergency preparedness** with alarm and monitoring capabilities
* **User-friendly operation** with intuitive button assignments

### Complete Configuration Guide

#### General Settings

##### TX Power Management

**Important**: Both "Low" and "High" power modes output **≤500mW ERP** per PMR446
regulations. The power output is identical; the mode selection exists for
user preference and potential battery optimization.

* **Default Setting**: Low Power Mode
  * **Output**: 500mW ERP (same as High)
  * **Benefit**: May conserve battery in some conditions
  * **Range**: Same as High Power (up to 12+ km in optimal conditions)
  * **Best For**: General use, battery consciousness
* **High Power Mode**: Available via menu (POW setting)
  * **Output**: 500mW ERP (same as Low)
  * **Range**: Same as Low Power (up to 12+ km in optimal conditions)
  * **Note**: Display shows "LOW" when Low Power is selected
  * **Reality**: Both modes comply with PMR446 ≤500mW limit

##### Time-Out Timer (TOT)

* **Setting**: 3 minutes
  * **Purpose**: Prevents accidental extended transmissions
  * **Benefit**: Conserves battery and promotes channel sharing
  * **Safety**: Prevents radio lock-up situations

#### Advanced Button Assignments

**Important**: The following describes a **custom programmed configuration** using
the optional PRG-G15 software. These are **not** factory defaults.

**Factory Defaults**:

* **PF3 (Function Key 1)**: Short press = Monitor
* **PF4 (Function Key 2)**: Long press (3 sec) = Scan

**Hybrid Profile Custom Programming** (requires PRG-G15 software):

##### PF3 Button: Monitor Function

* **Short Press**: Monitor (keep default)
  * **Function**: Opens squelch to hear weak or distant signals
  * **Usage**: Check channel activity before transmitting
  * **Tactical Benefit**: Situational awareness in critical scenarios
  * **Hiking Benefit**: Monitor for group communications in weak signal areas

##### PF3 Long Press: FM Radio Toggle (Custom Option)

* **Custom Programming**: FM Radio receiver (requires PRG-G15 software)
  * **Function**: Toggle FM broadcast radio receiver mode
  * **Source**: Confirmed in official manual ("FM Radio and Compander
        (programmables with PRG-G15)")
  * **Requirement**: Must be enabled via PRG-G15 programming software
  * **Alternative**: Can assign channel up/down, VOX toggle, or leave unassigned

##### PF4 Button: Channel Scan

* **Long Press**: Scan (keep default)
  * **Function**: Monitor multiple channels for activity
  * **Scan List**: All programmed channels
  * **Tactical Benefit**: Enhanced situational awareness
  * **Hiking Benefit**: Find active group communications
  * **Emergency Use**: Locate emergency communications

##### PF4 Short Press: (Available for custom programming)

* **Suggestion**: Leave unassigned or assign to frequently-used function
  * **Note**: Power toggle is not recommended since both Low and High modes
        output identical 500mW ERP - the toggle only changes the display
        indicator, not actual performance

#### Emergency and Safety Features

##### Emergency Button Configuration

* **Activation**: 3-second hold (prevents accidental activation)
  * **Function**: Emergency alarm transmission
  * **Signal**: 30-second distinctive alarm tone
  * **Follow-up**: 30-second open transmission window
  * **Channels**: Transmits on current channel
  * **Configuration**: Must be enabled via PRG-G15 software

##### Emergency Alarm Features

* **Audio Alert**: Loud distinctive tone (30 seconds)
* **Transmission Window**: 30 seconds open transmission after alarm
* **Automatic Cycle**: Returns to receive mode, can be repeated
* **Visual Indication**: Display shows emergency mode active
* **Priority Use**: Should take precedence over normal traffic
* **Location Aid**: Helps others locate emergency source
* **Note**: Must be enabled via PRG-G15 programming software

#### Advanced Feature Configuration

##### Busy Channel Lockout (BCL)

* **Setting**: Enable via PRG-G15 software
  * **Purpose**: Prevents transmission on occupied channels
  * **Benefit**: Avoids interference with existing communications
  * **Etiquette**: Promotes proper radio communication protocols
  * **Note**: Requires PRG-G15 programming software to configure

##### VOX (Voice Operated Exchange)

* **Setting**: Disabled by default
  * **Reason**: Not suitable for noisy tactical environments
  * **Alternative**: Manual PTT for better control
  * **Optional**: Can be enabled for hands-free operation when appropriate
  * **Sensitivity**: Adjustable if enabled

##### Scrambler/Privacy

* **Setting**: Optional (based on use case)
  * **Type**: Digital voice scrambling
  * **Usage**: When privacy is required
  * **Compatibility**: All radios must use same scrambler setting
  * **Note**: Not encryption-grade security

##### CTCSS/DCS Tones

* **Setting**: Channel-dependent
  * **Purpose**: Reduces interference from other users
  * **Recommendation**: Use on busy channels
  * **Compatibility**: Coordinate with team members
  * **Standard Tones**: Use common CTCSS frequencies

##### Additional Programmable Features (Optional)

The following features can be configured via PRG-G15 software for enhanced customization:

* **ROGER BEEP**: End-of-transmission tone confirmation
  * **Use Case**: Group coordination, confirms PTT release
  * **Note**: May not be compatible with non-Midland radios in mixed groups
* **VOICE Prompts**: Spoken channel/setting announcements
  * **Use Case**: Accessibility, hands-free confirmation
  * **Note**: Disable for stealth operations
* **Compander**: Audio compression for clearer communications
  * **Use Case**: Noisy environments, improved voice clarity
  * **Note**: Both radios must have compander enabled for compatibility
* **RRM Channel**: Restricted Radio Mode (Italy-specific regulatory channel)
  * **Use Case**: Compliance with Italian PMR446 regulations

**Important for Mixed Radio Groups**: If your team uses different radio brands (Baofeng, Motorola, etc.), only use standard PMR446 features (frequencies, CTCSS/DCS codes) for compatibility. Advanced features like ROGER BEEP, Compander, and Scrambler may not work across different manufacturers.

##### Additional PRG-G15 Features

Optional features configurable via PRG-G15 programming software:

* **ROGER BEEP**: Enable/disable end-of-transmission confirmation tone
  * **Use Case**: Confirm PTT release in noisy environments
  * **Team Coordination**: All radios should match this setting
* **VOICE Prompts**: Enable/disable spoken audio announcements
  * **Announces**: Channel numbers, menu settings
  * **Preference**: Disable for stealth operations, enable for convenience
* **Compander**: Audio compression/expansion for clearer communications
  * **Benefit**: Reduces background noise, enhances voice clarity
  * **Compatibility**: Both transmit and receive radios should match
* **RRM Channel**: Italy-specific Restricted Radio Mode channel
  * **Availability**: Italy only (regulatory requirement)

**Note**: SQUELCH levels can be adjusted via front panel (Menu > SQL) without programming software.

### Use Case Optimization

#### For Tactical Operations

* Monitor function (PF3) provides channel awareness before transmission
* Channel scanning (PF4 long press) for situational awareness
* Emergency alarm enables rapid distress signaling
* BCL prevents interference with critical communications
* VOX disabled for noise discipline and security
* CTCSS/DCS tones for group isolation on busy channels
* All transmissions limited to 500mW ERP per PMR446 regulations

#### For Hiking and Recreation

* Monitor function helps locate group communications in weak signal areas
* Scanning quickly finds the most active channel
* Emergency features provide safety backup
* CTCSS tones reduce interference from other hikers/groups
* Narrow bandwidth provides clearer audio quality
* 16-20 hour battery life with typical use (90% RX, 10% TX)
* All modes output 500mW ERP for consistent range performance
* Power toggle adapts to changing terrain/distance needs

#### For Emergency Preparedness

* Emergency alarm provides distress signaling
* High power access ensures maximum range when needed
* Monitor capability allows listening for emergency traffic
* Channel scanning helps locate active emergency communications
* Battery optimization extends operational time

### Performance Specifications

#### Battery Life Estimates

**Battery Pack**: 7.4V Li-ion 1600mAh rechargeable

**Charging Time**: 4 hours (full charge)

| Usage Pattern             | Battery Life |
|---------------------------|--------------|
| 90% receive, 10% transmit | 16-20 hours |
| 50% receive, 50% transmit | 8-12 hours |
| Continuous transmit       | 4-6 hours |

**Power Mode Note**: The "Low" and "High" power menu settings both output
≤500mW ERP per PMR446 regulations. Battery life is nearly identical between
modes since the RF output power is the same. Any minor difference is due to
internal circuitry efficiency, not transmission power.

#### Range Performance

**Note**: Range is identical for both power modes (≤500mW ERP per PMR446
regulations)

| Environment | Typical Range | Notes |
|-------------|---------------|-------|
| **Open Terrain** | Up to 12+ km | Line of sight, no obstructions |
| **Urban Areas** | 1-2 km | Buildings and structures |
| **Forest/Hills** | 4-6 km | Trees, leaves, moderate obstructions |
| **Buildings** | Varies | Reduced by metal construction |

**Coverage depends on**: Terrain, obstructions (buildings, trees), antenna
position, weather conditions, and interference.

### Programming Instructions

**Programming Cable Kit Required**: To use PRG-G15 software, you must purchase the **Midland PRG-G15 Programming Kit C1131** (€36.00).

**Kit Contents:**

* USB programming cable
* PRG-G15 software (CD-ROM/USB or download)
* Compatible with G15/G15 PRO/G18/Arctic models

**Purchase From:**

* [Midland Europe Official Store](https://www.midlandeurope.com/en_150/products/prg-g15) (€36.00)
* Midland authorized dealers worldwide
* Part Number: C1131 | EAN: 8011869193460

**Note**: Software and cable are for experienced users. No instruction manual or support hotline included.

#### PRG-G15 Software Capabilities

The PRG-G15 programming software allows you to customize the following radio features:

**Radio Functions:**

* **CTCSS/DCS Codes** - Configure privacy tones (50 CTCSS + 105 DCS codes)
* **TOT (Time-Out Timer)** - Set transmission timeout limits
* **VOX Sensitivity** - Adjust voice-activation threshold
* **ROGER BEEP** - Enable/disable end-of-transmission tone
* **SQUELCH Levels** - Configure noise suppression
* **VOICE Prompts** - Enable/disable audio announcements
* **RRM Channel** - Restricted Radio Mode (Italy-specific)

**Advanced Features:**

* **Emergency Button** - Enable/disable alarm function (3-second hold)
* **FM Radio** - Enable broadcast receiver mode
* **Compander** - Audio compression for clearer communications
* **PF3/PF4 Buttons** - Reprogram function key assignments

**Important Limitations:**

* Cannot modify frequencies (locked to PMR446 band)
* Cannot change output power (fixed at ≤500mW ERP)
* Modifying these would invalidate regulatory approval

**System Requirements:** Not publicly documented (likely Windows 7 or newer with USB support)

#### Step-by-Step Setup

##### Preparation

* [ ] **Purchase Midland PRG-G15 Kit C1131** (€36 official, includes USB cable + software)
* [ ] **Backup existing settings** before programming
* [ ] **Charge battery** to full capacity
* [ ] **Install programming software** and drivers
* [ ] **Connect programming cable** securely

##### Basic Configuration (Front Panel Menu)

* [ ] Set `TX Power` to Low via Menu > POW (both modes = 500mW)
* [ ] Set `TOT` to desired timeout (30-270 sec) via Menu > TOT
* [ ] Disable `VOX` initially via Menu > VOX > OFF
* [ ] Adjust `SQL` (Squelch) to level 5 via Menu > SQL

##### Advanced Configuration (PRG-G15 Software Required)

* [ ] Enable `BCL` (Busy Channel Lockout)
* [ ] Configure Emergency Button (3-second hold activation)
* [ ] Enable FM Radio feature if desired
* [ ] Configure Compander for audio processing

##### Button Programming (Hybrid Profile Custom Setup)

* [ ] Keep `PF3 Short Press` as Monitor (factory default - recommended)
* [ ] Keep `PF4 Long Press` as Scan (factory default - recommended)
* [ ] Optional: Assign `PF3 Long Press` to frequently-used function
* [ ] Optional: Assign `PF4 Short Press` to frequently-used function
* [ ] Enable Emergency Button (3-second hold) via PRG-G15
* [ ] Test all programmed functions thoroughly

**Note**: Power toggle is not recommended since both modes output identical
500mW ERP.

##### Advanced Features

* [ ] Configure Emergency Alarm settings
* [ ] Set up CTCSS tones if needed
* [ ] Program channel assignments from frequency table
* [ ] Test scrambler settings if privacy required

##### Testing and Validation

* [ ] Test all button functions thoroughly
* [ ] Verify emergency alarm operation
* [ ] Check power toggle functionality
* [ ] Test FM radio operation
* [ ] Validate scan performance

### Safety Considerations and Best Practices

#### Operational Safety

##### Battery Management

* Use only manufacturer-approved batteries
* Monitor battery level regularly
* Carry spare batteries for extended operations
* Avoid deep discharge cycles

##### RF Safety

* Never operate without proper antenna attached
* Maintain safe distance during transmission
* Follow manufacturer's SAR guidelines (0.982 W/Kg)
* Use appropriate antenna for environment

##### Emergency Protocols

* Test emergency alarm functionality regularly
* Coordinate emergency procedures with team members
* Know local emergency frequencies and protocols
* Practice emergency communication procedures

#### Programming Safety

##### Configuration Backup

* Always backup settings before changes
* Document all modifications
* Test thoroughly after programming
* Keep backup configurations available

##### Validation Testing

* Test all functions after programming
* Verify compliance with local regulations
* Check for proper operation in target environment
* Confirm emergency features work correctly

#### Usage Guidelines

##### Communication Etiquette

* Listen before transmitting
* Keep transmissions brief and clear
* Use proper radio procedures
* Respect emergency channel protocols

##### Maintenance Schedule

* Clean radio and accessories regularly
* Check programming monthly
* Update software when available
* Inspect antennas and connections

### Quick Setup Summary

For users who want to implement this **hybrid profile**:

**Basic Settings** (accessible via front panel menu):

1. **Power Mode**: Either Low or High (both = 500mW ERP) - Menu > POW
2. **Squelch**: Level 5 (default) - Menu > SQL
3. **VOX**: Disabled - Menu > VOX > OFF
4. **CTCSS/DCS**: As needed for your group - Menu > C-CDC/R-CDC/T-CDC
5. **TOT**: 30-270 seconds configurable - Menu > TOT

**With PRG-G15 Programming Software** (advanced features):
6. **BCL**: Enable (Busy Channel Lockout)
7. **Emergency Button**: Enable (3-second hold)
8. **PF3/PF4 custom actions**: Optional reprogramming
9. **FM Radio**: Enable receiver mode
10. **Compander**: Enable audio compression

**Factory Defaults Work Well**: The default button assignments (Monitor and
Scan) are already optimized for most use cases.

### Performance Tips

#### Maximizing Battery Life

* Use Low Power mode for nearby communication
* Disable FM radio when not needed
* Reduce backlight timeout
* Use scan sparingly
* Turn off unnecessary features

#### Optimizing Range

* Use High Power mode for long-range communication
* Position antenna vertically when possible
* Find elevated positions for better propagation
* Avoid obstacles and interference sources
* Use repeaters when available

#### Emergency Preparedness

* Practice emergency procedures regularly
* Know alternative communication methods
* Keep emergency contact information accessible
* Maintain spare batteries and backup equipment
* Coordinate with local emergency services

### Support and Troubleshooting

#### Common Issues

* **Poor Range**: Check antenna, try high power mode, find elevated position
* **Weak Audio**: Adjust squelch, check volume, verify narrow bandwidth
* **Battery Drain**: Reduce backlight, use low power, disable unused features
* **Programming Errors**: Verify cable connection, restart software, check
    drivers

#### Additional Resources

* **User Manual**: See `docs/` folder for English, German, and French manuals
* **Programming Software**: [PRG-G15 Download](https://support.midlandeurope.com/en_150/products/g18-pro) (Midland Europe Support)
* **Programming Cable Kit**: [Midland PRG-G15 Official](https://www.midlandeurope.com/en_150/products/prg-g15) (€36, includes USB cable + software)
* **Official Support**: [G18 PRO Support Page](https://support.midlandeurope.com/en_150/products/g18-pro)
* **Community Forums**: User experiences and modifications
* **Technical Support**: Manufacturer assistance and warranty service

**Important**: This configuration profile is optimized for general use. Always
verify compliance with local regulations and adjust settings based on specific
operational requirements and environmental conditions.

## Tactical Team Operations and Settings

### Tactical Team Checklists

Detailed checklists have been organized into separate files for easy reference:

* [Pre-Mission Checklist](checklists/Pre_Mission_Checklist.md) - Complete preparation verification
* [Mission Execution Checklist](checklists/Mission_Execution_Checklist.md) - Active operations protocol
* [Post-Mission Checklist](checklists/Post_Mission_Checklist.md) - After-action review and maintenance

### Settings for Tactical Operations

#### Radio Configuration

* **Frequency Range**: PMR446 (446.0 - 446.2 MHz)
* **Default Channel**: 1 (446.00625 MHz)
* **Channel Spacing**: 12.5 kHz
* **CTCSS/DCS Settings**: Enabled (as per mission requirements)

#### Communication Protocols

* **Standard Call Signs**: Assigned per team member
* **Emergency Code**: Team-defined alert phrase
* **Check-In Interval**: Every 15 minutes (adjust as needed)
* **CTCSS/DCS Codes**: Use privacy tones to isolate team communications

#### Equipment Maintenance

* **Radio Batteries**: Fully charged before deployment (1600mAh, ~16-20 hours)
* **Range Testing**: Pre-test in similar terrain conditions
* **Audio Accessories**: External mic/headset for tactical environments
* **Backup Units**: Spare batteries and backup radios

#### Security Measures

* **Scrambler**: Enable for basic voice privacy (not encryption-grade)
* **CTCSS/DCS Codes**: Coordinate team-specific privacy codes
* **Channel Discipline**: Monitor before transmitting (BCL if programmed)

### Programmable Function (PF) Button Settings

**Hardware Note**: The G18 PRO has **Function key 1 (PF3)** and **Function key 2
(PF4)** only. There are no PF1 or PF2 buttons.

#### Default PF Button Assignments (Per Manual)

1. **Function Key 1 (PF3)**:
    * **Short Press**: Monitor function
    * **Description**: Opens squelch to hear weak signals and check channel
        activity before transmitting.

2. **Function Key 2 (PF4)**:
    * **Long Press (3 seconds)**: SCAN function
    * **Description**: Scans through all programmed channels to detect active
        communications.

3. **Emergency Button** (separate physical button):
    * **Long Press (3 seconds)**: Emergency alarm
    * **Description**: Sends 30-second alarm tone, then 30 seconds of open
        transmission for status update. Must be enabled via programming software.

#### Programmable Options (via PRG-G15 software)

The PF3 and PF4 buttons can be reprogrammed with the optional PRG-G15
programming software to customize functionality for specific operational needs.

#### Customizable PF Button Options

The following functions can be assigned to PF3/PF4 buttons via PRG-G15 software:

* **Monitor**: Listen to the current channel without squelch (default PF3 short)
* **Scan**: Cycle through all programmed channels (default PF4 long)
* **Emergency Alarm**: Send distress signal (separate emergency button)
* **FM Radio**: Toggle FM broadcast receiver mode
* **High/Low Power**: Toggle power mode (note: both output 500mW ERP)

**Note**: Specific programmable options depend on PRG-G15 software capabilities.
Consult programming software manual for complete list of assignable functions.

## PMR446 Compliance and Technical Specifications

The Midland G18 is fully compliant with PMR446 regulations in Europe,
operating exclusively within the 446.0 to 446.2 MHz frequency range. This
ensures legal operation across all European countries without requiring a
license.

## Safety and Best Practices

* Always perform pre-operation radio checks
* Monitor battery levels and carry spares
* Use appropriate power levels for your situation
* Follow radio etiquette and communication protocols
* Test emergency features regularly
* Keep firmware updated
* Store radios in dry, temperature-controlled environments
