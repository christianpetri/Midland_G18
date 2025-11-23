# Tactical Team Operations Guide

This guide provides comprehensive settings, protocols, and procedures for
tactical team operations using the Midland G18 PRO PMR446 radio.

## Tactical Team Checklists

Detailed operational checklists have been organized into separate files for
easy reference during mission phases:

* [Pre-Mission Checklist](../checklists/Pre_Mission_Checklist.md) - Complete
  preparation verification
* [Mission Execution Checklist](../checklists/Mission_Execution_Checklist.md) -
  Active operations protocol
* [Post-Mission Checklist](../checklists/Post_Mission_Checklist.md) -
  After-action review and maintenance

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

* **Scrambler**: Enable for basic voice privacy (not encryption-grade)
  * **Note**: Not military-grade encryption
  * **Compatibility**: All team radios must use same scrambler setting
  * **Limitation**: Can be defeated by determined listeners
* **CTCSS/DCS Codes**: Coordinate team-specific privacy codes
  * **Purpose**: Reduce interference, filter out other users
  * **Security**: Does not encrypt communications
* **Channel Discipline**: Monitor before transmitting (use BCL if programmed)

### Operational Security

* **Code Words**: Use pre-arranged code words for sensitive information
* **Location Security**: Avoid transmitting exact coordinates in the clear
* **Time Limits**: Keep transmissions short to minimize detection
* **Frequency Rotation**: Consider rotating channels during long operations

## Programmable Function (PF) Button Configuration

**Hardware Note**: The G18 PRO has **Function key 1 (PF3)** and **Function key 2
(PF4)** only. There are no PF1 or PF2 buttons.

### Default PF Button Assignments (Per Manual)

1. **Function Key 1 (PF3)**:
    * **Short Press**: Monitor function
    * **Description**: Opens squelch to hear weak signals and check channel
        activity before transmitting
    * **Tactical Use**: Situational awareness, check channel before transmission

2. **Function Key 2 (PF4)**:
    * **Long Press (3 seconds)**: SCAN function
    * **Description**: Scans through all programmed channels to detect active
        communications
    * **Tactical Use**: Detect other team communications, find active channels

3. **Emergency Button** (separate physical button):
    * **Long Press (3 seconds)**: Emergency alarm
    * **Description**: Sends 30-second alarm tone, then 30 seconds of open
        transmission for status update
    * **Requirement**: Must be enabled via PRG-G15 programming software
    * **Tactical Use**: Distress signaling, emergency notification

### Programmable Options (via PRG-G15 software)

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

### Recommended Tactical Configuration

**For Most Tactical Operations**, the factory defaults work well:

* **PF3 Short Press**: Monitor (check channel activity)
* **PF4 Long Press**: Scan (find active communications)
* **Emergency Button**: Enable via PRG-G15 for distress signaling

**Custom Options** (requires PRG-G15 programming):

* **PF3 Long Press**: Assign to frequently-used function (FM Radio, VOX toggle, etc.)
* **PF4 Short Press**: Leave unassigned or assign to quick channel switch

## Advanced Tactical Features

### Busy Channel Lockout (BCL)

* **Purpose**: Prevents transmission on occupied channels
* **Benefit**: Avoids interference with existing communications
* **Configuration**: Enable via PRG-G15 software
* **Tactical Advantage**: Prevents accidentally stepping on critical transmissions

### Voice Operated Exchange (VOX)

* **Default**: Disabled for tactical operations
* **Reason**: Not suitable for noisy tactical environments
* **Alternative**: Manual PTT for better control
* **Optional**: Can be enabled for hands-free operation in quiet environments

### Time-Out Timer (TOT)

* **Recommended Setting**: 3 minutes (180 seconds)
* **Purpose**: Prevents accidental extended transmissions
* **Benefit**: Conserves battery, promotes channel sharing
* **Configuration**: Adjustable via Menu > TOT (30-270 seconds)

### Emergency Alarm

* **Activation**: 3-second hold on emergency button
* **Signal**: 30-second distinctive alarm tone
* **Follow-up**: 30-second open transmission window
* **Configuration**: Must be enabled via PRG-G15 software
* **Test Regularly**: Verify functionality before each mission

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
* **Power Conservation**: Plan Low Power usage where appropriate

## Troubleshooting Common Issues

### Poor Range

* **Check antenna**: Ensure proper connection and orientation
* **Try High Power mode**: Switch via Menu > POW (both = 500mW ERP)
* **Find elevated position**: Improve line-of-sight propagation
* **Verify CTCSS/DCS**: Ensure matching codes across team radios

### Weak Audio

* **Adjust squelch**: Lower squelch via Menu > SQL
* **Check volume**: Verify volume setting
* **Test with different radio**: Isolate transmitter vs. receiver issue

### Battery Drain

* **Reduce backlight**: Shorten timeout or disable
* **Use Low Power mode**: Minor battery savings possible
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
