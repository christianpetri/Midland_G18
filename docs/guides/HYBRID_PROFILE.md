# Hybrid Profile Configuration for Midland G18 Radio

This versatile configuration profile balances tactical and recreational
features, making it ideal for users who need reliable communication across
various scenarios including hiking, tactical operations, emergency preparedness,
and general use.

## Profile Overview

The Hybrid Profile is designed for maximum flexibility while maintaining
optimal performance and battery efficiency. It provides:

* **Tactical readiness** with quick-access emergency features
* **Recreational functionality** for hiking and outdoor activities
* **Optional FM Radio** receiver (requires PRG-G15 software configuration)
* **Emergency preparedness** with alarm and monitoring capabilities
* **User-friendly operation** with intuitive button assignments

## Complete Configuration Guide

### General Settings

#### TX Power Management

**Important**: Per PMR446 regulations, the G18-PRO outputs **≤500mW ERP** in both
"Low" and "High" power modes. The official manual confirms: "By default, both low
and high power are set at 500mW."

* **Power Setting**: Menu > POW
  * **Low Mode**: 500mW output (displays "LOW" indicator)
  * **High Mode**: 500mW output (no indicator)
  * **Range**: Identical in both modes (~12+ km optimal conditions)
  * **Recommendation**: Keep on Low mode; toggling serves no practical purpose

#### Time-Out Timer (TOT)

* **Setting**: 3 minutes
  * **Purpose**: Prevents accidental extended transmissions
  * **Benefit**: Conserves battery and promotes channel sharing
  * **Safety**: Prevents radio lock-up situations

### Advanced Button Assignments

**Important**: The following describes a **custom programmed configuration** using
the optional PRG-G15 software. These are **not** factory defaults.

**Factory Defaults**:

* **PF3 (Function Key 1)**: Short press = Monitor
* **PF4 (Function Key 2)**: Long press (3 sec) = Scan

**Hybrid Profile Custom Programming** (requires PRG-G15 software):

#### PF3 Button: Monitor Function

* **Short Press**: Monitor (keep default)
  * **Function**: Opens squelch to hear weak or distant signals
  * **Usage**: Check channel activity before transmitting
  * **Tactical Benefit**: Situational awareness in critical scenarios
  * **Hiking Benefit**: Monitor for group communications in weak signal areas

#### PF3 Long Press: FM Radio Toggle (Custom Option)

* **Custom Programming**: FM Radio receiver (requires PRG-G15 software)
  * **Function**: Toggle FM broadcast radio receiver mode
  * **Source**: Confirmed in official manual ("FM Radio and Compander
        (programmables with PRG-G15)")
  * **Requirement**: Must be enabled via PRG-G15 programming software
  * **Alternative**: Can assign channel up/down, VOX toggle, or leave unassigned

#### PF4 Button: Channel Scan

* **Long Press**: Scan (keep default)
  * **Function**: Monitor multiple channels for activity
  * **Scan List**: All programmed channels
  * **Tactical Benefit**: Enhanced situational awareness
  * **Hiking Benefit**: Find active group communications
  * **Emergency Use**: Locate emergency communications

#### PF4 Short Press: (Available for custom programming)

* **Suggestion**: Leave unassigned or assign to frequently-used function
  * **Note**: Power toggle not recommended (see TX Power Management section)

### Emergency and Safety Features

#### Emergency Button Configuration

* **Activation**: 3-second hold (prevents accidental activation)
  * **Function**: Emergency alarm transmission
  * **Signal**: 30-second distinctive alarm tone
  * **Follow-up**: 30-second open transmission window
  * **Channels**: Transmits on current channel
  * **Configuration**: Must be enabled via PRG-G15 software

#### Emergency Alarm Features

* **Audio Alert**: Loud distinctive tone (30 seconds)
* **Transmission Window**: 30 seconds open transmission after alarm
* **Automatic Cycle**: Returns to receive mode, can be repeated
* **Visual Indication**: Display shows emergency mode active
* **Priority Use**: Should take precedence over normal traffic
* **Location Aid**: Helps others locate emergency source
* **Note**: Must be enabled via PRG-G15 programming software

### Advanced Feature Configuration

Configure these features via PRG-G15 software based on your operational needs.
**For detailed feature explanations**, see [PRG-G15 Programming Guide](PROGRAMMING.md#programmable-features-reference).

* **BCL (Busy Channel Lockout)**: Enable to prevent transmitting over active communications
* **VOX (Voice Operated Exchange)**: Disabled by default; enable for hands-free operation in quiet environments
* **Scrambler**: Enable for basic voice privacy (coordinate settings with team)
* **CTCSS/DCS Tones**: Configure per channel to reduce interference
* **ROGER BEEP**: Enable for end-of-transmission confirmation (may not work with non-Midland radios)
* **VOICE Prompts**: Enable for accessibility; disable for stealth operations
* **Compander**: Enable for clearer audio in noisy environments (requires both radios to have it enabled)
* **RRM Channel**: Italy-specific regulatory channel (configure if required)

### NC Variant Optional Features (G18-PRO NC Only)

If your radio is the **G18-PRO NC** model, you have access to three advanced
features (requires PRG-G15 V1.1.25+ software):

* **Noise Cancelling TX** - Adaptive noise suppression during transmission
  * **Benefit**: Clearer voice transmission in noisy environments
  * **Use Case**: Vehicles, outdoor windy conditions, tactical operations
  * **Configuration**: Enable per-channel in PRG-G15 software
* **Dual Watch (DW)** - Monitor two channels simultaneously
  * **Benefit**: Stay aware of both primary and secondary frequencies
  * **Use Case**: Monitor team and dispatch channels at once
  * **Hardware Requirement**: Requires G18-PRO NC (dual receiver hardware)
  * **Configuration**: Set primary and secondary channels in PRG-G15 software
* **Only-CH Mode** - Lock radio to single channel
  * **Benefit**: Prevents accidental frequency changes
  * **Use Case**: Training, high-security operations, user discipline
  * **Hardware Requirement**: Available on both standard and NC variants
  * **Configuration**: Enable in PRG-G15 `Optional Menus` → `Only-CH Mode`

**⚠️ Hardware Limitation**: Noise Cancelling TX and Dual Watch require the
G18-PRO NC variant's dual receiver chipset. Standard G18-PRO radios cannot use
these features. Only-CH Mode is available on all models.

**For complete NC feature documentation and detailed setup**, see
[NC Variants Guide](../reference/NC_VARIANTS.md).

## Use Case Optimization

### For Tactical Operations

* Monitor function (PF3) provides channel awareness before transmission
* Channel scanning (PF4 long press) for situational awareness
* Emergency alarm enables rapid distress signaling
* BCL prevents interference with critical communications
* VOX disabled for noise discipline and security
* CTCSS/DCS tones for group isolation on busy channels
* All transmissions limited to 500mW ERP per PMR446 regulations

### For Hiking and Recreation

* Monitor function helps locate group communications in weak signal areas
* Scanning quickly finds the most active channel
* Emergency features provide safety backup
* CTCSS tones reduce interference from other hikers/groups
* Narrow bandwidth provides clearer audio quality
* 16-20 hour battery life with typical use (90% RX, 10% TX)
* Consistent 500mW ERP output ensures reliable range

### For Emergency Preparedness

* Emergency alarm provides distress signaling
* 500mW ERP output ensures maximum legal range
* Monitor capability allows listening for emergency traffic
* Channel scanning helps locate active emergency communications
* Battery optimization extends operational time

## Performance Specifications

### Battery Life Estimates

**Battery Pack**: 7.4V Li-ion 1600mAh rechargeable

**Charging Time**: 4 hours (full charge)

| Usage Pattern             | Battery Life |
|---------------------------|--------------|
| 90% receive, 10% transmit | 16-20 hours |
| 50% receive, 50% transmit | 8-12 hours |
| Continuous transmit       | 4-6 hours |

**Note**: Battery life independent of Low/High power setting (both output 500mW).

### Range Performance

| Environment | Typical Range | Notes |
|-------------|---------------|-------|
| **Open Terrain** | Up to 12+ km | Line of sight, no obstructions |
| **Urban Areas** | 1-2 km | Buildings and structures |
| **Forest/Hills** | 4-6 km | Trees, leaves, moderate obstructions |
| **Buildings** | Varies | Reduced by metal construction |

**Coverage depends on**: Terrain, obstructions (buildings, trees), antenna
position, weather conditions, and interference.

## Quick Setup Summary

For users who want to implement this **hybrid profile**:

**Basic Settings** (accessible via front panel menu):

1. **Power Mode**: Either Low or High (both = 500mW ERP) - Menu > POW
2. **Squelch**: Level 5 (default) - Menu > SQL
3. **VOX**: Disabled - Menu > VOX > OFF
4. **CTCSS/DCS**: As needed for your group - Menu > C-CDC/R-CDC/T-CDC
5. **TOT**: 30-270 seconds configurable - Menu > TOT

**With PRG-G15 Programming Software** (advanced features):

1. **BCL**: Enable (Busy Channel Lockout)
2. **Emergency Button**: Enable (3-second hold)
3. **PF3/PF4 custom actions**: Optional reprogramming
4. **FM Radio**: Enable receiver mode
5. **Compander**: Enable audio compression

**Factory Defaults Work Well**: The default button assignments (Monitor and
Scan) are already optimized for most use cases.

## Performance Tips

### Maximizing Battery Life

* Minimize transmit time (primary power savings)
* Disable FM radio when not needed
* Reduce backlight timeout
* Use scan sparingly
* Turn off unnecessary features

### Optimizing Range

* Ensure antenna connection secure (both modes = 500mW)
* Position antenna vertically when possible
* Find elevated positions for better propagation
* Avoid obstacles and interference sources
* Use repeaters when available

### Emergency Preparedness

* Practice emergency procedures regularly
* Know alternative communication methods
* Keep emergency contact information accessible
* Maintain spare batteries and backup equipment
* Coordinate with local emergency services

## Safety Considerations

### Operational Safety

#### Battery Management

* Use only manufacturer-approved batteries
* Monitor battery level regularly
* Carry spare batteries for extended operations
* Avoid deep discharge cycles

#### RF Safety

* Never operate without proper antenna attached
* Maintain safe distance during transmission
* Follow manufacturer's SAR guidelines (0.982 W/Kg)
* Use appropriate antenna for environment

#### Emergency Protocols

* Test emergency alarm functionality regularly
* Coordinate emergency procedures with team members
* Know local emergency frequencies and protocols
* Practice emergency communication procedures

### Usage Guidelines

#### Communication Etiquette

* Listen before transmitting
* Keep transmissions brief and clear
* Use proper radio procedures
* Respect emergency channel protocols

#### Maintenance Schedule

* Clean radio and accessories regularly
* Check programming monthly
* Update software when available
* Inspect antennas and connections

---

**Important**: This configuration profile is optimized for general use. Always
verify compliance with local regulations and adjust settings based on specific
operational requirements and environmental conditions.

*For programming instructions, see [PROGRAMMING.md](PROGRAMMING.md)*
