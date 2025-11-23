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
  * **Note**: Power toggle is not recommended since both Low and High modes
        output identical 500mW ERP - the toggle only changes the display
        indicator, not actual performance

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

#### Busy Channel Lockout (BCL)

* **Setting**: Enable via PRG-G15 software
  * **Purpose**: Prevents transmission on occupied channels
  * **Benefit**: Avoids interference with existing communications
  * **Etiquette**: Promotes proper radio communication protocols
  * **Note**: Requires PRG-G15 programming software to configure

#### VOX (Voice Operated Exchange)

* **Setting**: Disabled by default
  * **Reason**: Not suitable for noisy tactical environments
  * **Alternative**: Manual PTT for better control
  * **Optional**: Can be enabled for hands-free operation when appropriate
  * **Sensitivity**: Adjustable if enabled

#### Scrambler/Privacy

* **Setting**: Optional (based on use case)
  * **Type**: Digital voice scrambling
  * **Usage**: When privacy is required
  * **Compatibility**: All radios must use same scrambler setting
  * **Note**: Not encryption-grade security

#### CTCSS/DCS Tones

* **Setting**: Channel-dependent
  * **Purpose**: Reduces interference from other users
  * **Recommendation**: Use on busy channels
  * **Compatibility**: Coordinate with team members
  * **Standard Tones**: Use common CTCSS frequencies

#### Additional Programmable Features (Optional)

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

**Important for Mixed Radio Groups**: If your team uses different radio brands
(Baofeng, Motorola, etc.), only use standard PMR446 features (frequencies,
CTCSS/DCS codes) for compatibility. Advanced features like ROGER BEEP,
Compander, and Scrambler may not work across different manufacturers.

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
* All modes output 500mW ERP for consistent range performance
* Power toggle adapts to changing terrain/distance needs

### For Emergency Preparedness

* Emergency alarm provides distress signaling
* High power access ensures maximum range when needed
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

**Power Mode Note**: The "Low" and "High" power menu settings both output
≤500mW ERP per PMR446 regulations. Battery life is nearly identical between
modes since the RF output power is the same. Any minor difference is due to
internal circuitry efficiency, not transmission power.

### Range Performance

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

* Use Low Power mode for nearby communication
* Disable FM radio when not needed
* Reduce backlight timeout
* Use scan sparingly
* Turn off unnecessary features

### Optimizing Range

* Use High Power mode for long-range communication
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
