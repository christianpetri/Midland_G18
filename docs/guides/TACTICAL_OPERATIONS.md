# Tactical Team Operations Guide

This guide provides comprehensive settings, protocols, and procedures for
tactical team operations using the Midland G18 PRO PMR446 radio.

## Radio Configuration for Tactical Operations

### Basic Settings

* **Frequency Range**: PMR446 (446.0 - 446.2 MHz)
* **Default Channel**: 1 (446.00625 MHz)
* **Channel Spacing**: 12.5 kHz
* **Power Output**: ≤500mW ERP (both Low and High modes)
* **CTCSS/DCS Settings**: Enabled (as per mission requirements)

### Communication Protocols

#### Standard Operating Procedures

* **Standard Call Signs**: Assigned per team member
* **Emergency Code**: Team-defined alert phrase
* **Check-In Interval**: Every 15 minutes (adjust as needed)
* **CTCSS/DCS Codes**: Use privacy tones to isolate team communications
* **BCL (Busy Channel Lockout)**: Enable to prevent transmitting over active communications

#### Radio Discipline

* **Listen Before Transmitting**: Use Monitor (PF3) to check channel activity
* **Keep Transmissions Brief**: Minimize transmission time for security and battery life
* **Use Proper Procedures**: Employ standard radio communication protocols
* **Maintain Operational Security**: Avoid transmitting sensitive information in the clear

## Equipment Maintenance

### Battery Management

* **Radio Batteries**: Fully charged before deployment (1600mAh, ~16-20 hours typical use)
* **Pre-Mission Check**: Verify 80%+ charge on all units
* **Spare Batteries**: Carry at least one spare per radio
* **Charging Schedule**: Recharge after each mission, even if partially used

### Range Testing

* **Pre-Deployment Testing**: Test range in similar terrain conditions
* **Environmental Factors**: Account for buildings, terrain, vegetation
* **Expected Range**: 1-2 km urban, 4-6 km forest/hills, 12+ km open
  terrain

### Audio Accessories

* **Tactical Headsets**: External mic/headset for noisy or tactical environments
* **PTT Accessories**: Remote push-to-talk for hands-free operation
* **Compatibility**: Verify accessories are compatible with G18 PRO

### Backup Equipment

* **Backup Units**: Spare batteries and backup radios
* **Emergency Power**: Solar chargers or power banks with appropriate
  adapters
* **Replacement Parts**: Spare antennas, belt clips, programming cables

## Security Measures

### Privacy Features

* **Scrambler**: Enable for basic voice privacy (not encryption-grade) - see [PROGRAMMING.md](PROGRAMMING.md#scrambler-voice-privacy) for details
* **CTCSS/DCS Codes**: Coordinate team-specific privacy codes - see [PROGRAMMING.md](PROGRAMMING.md#ctcssdcs-tones-selective-calling)
* **Channel Discipline**: Monitor before transmitting (use BCL if programmed)

### Operational Security

* **Code Words**: Use pre-arranged code words for sensitive information
* **Location Security**: Avoid transmitting exact coordinates in the clear
* **Time Limits**: Keep transmissions short to minimize detection
* **Frequency Rotation**: Consider rotating channels during long operations

### NC Variant Features (G18-PRO NC)

If your radio is the **G18-PRO NC** model, three advanced features enhance
tactical operations (requires PRG-G15 V1.1.25+):

#### Noise Cancelling TX

**Purpose**: Reduce background noise during transmission for clearer tactical
communications.

* **Configuration**: Enable per-channel in PRG-G15 software
* **Tactical Benefit**: Improves voice clarity in high-noise environments
  (vehicles, helicopters, tactical situations)
* **Use Case**: Ideal when communicating in noisy deployment areas
* **Recommended**: Enable on primary tactical channels

#### Dual Watch (DW)

**Purpose**: Simultaneously monitor primary team channel and secondary command
channel without manual switching.

* **Configuration**: Requires PRG-G15 software (set `D.W.main CH` to primary channel)
* **Tactical Benefit**: Maintain awareness of both team and command frequencies
* **Example Setup**:
  * Primary: Team tactical frequency (446.0625 MHz)
  * Secondary: Command/dispatch frequency (446.1875 MHz)
* **Operation**: Radio automatically alerts on incoming traffic from either channel
* **Recommended**: Enable for team leaders coordinating with command

#### Only-CH Mode

**Purpose**: Lock radio to single channel operation, preventing frequency
changes during critical operations.

* **Configuration**: Enable in PRG-G15 `Optional Menus` → `Only-CH Mode`
* **Tactical Benefit**: Prevents accidental frequency changes, enforces discipline
* **Security**: Restricts unauthorized channel access (useful for trainee teams)
* **Hardware Requirement**: Available on all G18-PRO models (standard and NC)
* **Recommended**: Enable during high-risk operations or team training

### Advanced NC Features for Tactical Teams

**⚠️ NC Variant Only** - The following features require G18-PRO NC hardware:

* **Noise Cancelling TX** - Improves voice clarity in noisy environments (vehicles,
  industrial sites)
* **Dual Watch (DW)** - Monitor primary tactical channel + secondary command/dispatch
  channel simultaneously

Both require the NC variant's dual receiver chipset and cannot be retrofitted to
standard G18-PRO radios.

**For complete NC feature documentation**, see
[NC Variants Guide](../reference/NC_VARIANTS.md).

## Programmable Function (PF) Button Configuration

### Button Functions for Tactical Use

**Factory Default Assignments** (work well for most tactical operations):

* **PF3 Short Press**: Monitor - Check channel before transmitting
* **PF4 Long Press (3 sec)**: Scan - Find active communications
* **Emergency Button (3 sec hold)**: Distress alarm (must enable via PRG-G15)

**For complete button programming options and detailed configuration**, see
[Hybrid Profile Configuration](HYBRID_PROFILE.md).

### Recommended Tactical Button Setup

For standard tactical operations, factory defaults are optimal:

* Use **Monitor (PF3)** to check channel before transmitting
* Use **Scan (PF4)** to locate active team communications  
* Enable **Emergency Button** via PRG-G15 for distress signaling

## Advanced Tactical Features

### Busy Channel Lockout (BCL)

* **Tactical Use**: Prevents accidentally stepping on critical transmissions
* **Configuration**: Enable via PRG-G15 - see [PROGRAMMING.md](PROGRAMMING.md#bcl-busy-channel-lockout)

### Voice Operated Exchange (VOX)

* **Tactical Recommendation**: Disable for noisy tactical environments
* **Manual PTT Preferred**: Better control for tactical communications
* **Details**: See [PROGRAMMING.md](PROGRAMMING.md#vox-voice-operated-exchange)

### Channel Scanning Modes

**Tactical Scan Recommendations**:

* **TO (Time-Operated)**: Best for monitoring channels while tracking activity
* **CO (Carrier-Operated)**: Best for staying on active communications, monitoring team traffic
* **SE (Search)**: Best for finding active channels, emergency response mode

**Detailed scan configuration**: See [PROGRAMMING.md](PROGRAMMING.md#scan-modes)

**Quick Tip**: Press ENT for 4 seconds on any channel to exclude/include from scan list.

## Mission Planning Considerations

### Communication Plan

* **Primary Channel**: Designate main operating channel
* **Alternate Channels**: Plan backup channels for contingencies
* **Emergency Channel**: Designate emergency/distress channel
* **CTCSS/DCS Codes**: Coordinate privacy tones across team

### Range Planning

* **Terrain Analysis**: Assess expected range based on environment
* **Relay Positions**: Plan relay stations for extended range
* **Check-In Schedule**: Establish regular status updates
* **Lost Comms Procedures**: Define actions if communication is lost

### Battery Planning

* **Mission Duration**: Calculate expected battery life
* **Spare Battery Allocation**: Distribute spares across team
* **Charging Opportunities**: Identify recharge points during mission
* **Power Conservation**: Minimize transmit time and disable unused features

## Troubleshooting Common Issues

### Poor Range

* **Check antenna**: Ensure proper connection and orientation
* **Verify power setting**: Confirm Menu > POW shows expected mode (both = 500mW ERP)
* **Find elevated position**: Improve line-of-sight propagation
* **Verify CTCSS/DCS**: Ensure matching codes across team radios

### Weak Audio

* **Adjust squelch**: Lower squelch via Menu > SQL
* **Check volume**: Verify volume setting
* **Test with different radio**: Isolate transmitter vs. receiver issue

### Battery Drain

* **Reduce backlight**: Shorten timeout or disable
* **Minimize transmit time**: Primary power conservation method
* **Disable unused features**: Turn off FM radio, scan, etc.
* **Check battery health**: Replace aging batteries

### Programming Errors

* **Verify cable connection**: Ensure secure connection to radio
* **Restart software**: Close and reopen PRG-G15
* **Check drivers**: Verify USB drivers installed correctly
* **Consult manual**: Review programming software documentation

## Safety and Best Practices

### Pre-Operation Checks

* Always perform radio checks before deployment
* Verify all team members on same channel and CTCSS/DCS codes
* Test emergency features and procedures
* Confirm spare batteries available and charged

### During Operations

* Monitor battery levels regularly
* Use appropriate power levels for situation
* Follow radio etiquette and communication protocols
* Maintain operational security

### Post-Operation

* Debrief team on communication effectiveness
* Document any issues or improvements needed
* Inspect and maintain equipment
* Recharge batteries immediately

### General Safety

* Never operate without proper antenna attached
* Maintain safe distance during transmission
* Follow manufacturer's SAR guidelines (0.982 W/Kg)
* Store radios in dry, temperature-controlled environments

---

*For programming instructions, see [PROGRAMMING.md](PROGRAMMING.md)*

*For hybrid profile configuration, see [HYBRID_PROFILE.md](HYBRID_PROFILE.md)*
