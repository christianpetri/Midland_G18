# PRG-G15 Programming Guide

Complete guide for programming the Midland G18 PRO radio using the PRG-G15
software and programming cable kit.

## Required Equipment

### Programming Cable Kit

**Programming Cable Kit Required**: To use PRG-G15 software, you must purchase
the **Midland PRG-G15 Programming Kit C1131**.

**Kit Contents:**

* USB programming cable
* PRG-G15 software (CD-ROM/USB or download)
* Compatible with G15/G15 PRO/G18/Arctic models

**Purchase Information:**

* **Official Source**:
  [Midland Europe Store](https://www.midlandeurope.com/en_150/products/prg-g15)
* **Price**: €36.00
* **Part Number**: C1131
* **EAN**: 8011869193460
* **Availability**: Midland Europe and authorized dealers worldwide

**Important Note**: Software and cable are for experienced users. No instruction
manual or support hotline included with kit.

### Software Download

* **Official Download**:
  [PRG-G15 at Midland Support](https://support.midlandeurope.com/en_150/products/g18-pro)
* **Included With**: Programming cable kit (CD-ROM/USB)
* **System Requirements**: Not publicly documented (likely Windows 7 or newer
  with USB support)

## PRG-G15 Software Capabilities

The PRG-G15 programming software allows you to customize the following radio
features:

### Radio Functions

* **CTCSS/DCS Codes** - Configure privacy tones (50 CTCSS + 105 DCS
  codes)
* **TOT (Time-Out Timer)** - Set transmission timeout limits (30-270
  seconds)
* **VOX Sensitivity** - Adjust voice-activation threshold (1-9 levels)
* **ROGER BEEP** - Enable/disable end-of-transmission tone
* **SQUELCH Levels** - Configure noise suppression (0-9 levels)
* **VOICE Prompts** - Enable/disable audio announcements
* **RRM Channel** - Restricted Radio Mode (Italy-specific regulatory
  channel)

### Advanced Features

* **Emergency Button** - Enable/disable alarm function (3-second hold
  activation)
* **FM Radio** - Enable broadcast receiver mode
* **Compander** - Audio compression for clearer communications
* **PF3/PF4 Buttons** - Reprogram function key assignments

### Important Limitations

* **Cannot modify frequencies** - Locked to PMR446 band
  (446.00625-446.19375 MHz)
* **Cannot change output power** - Fixed at ≤500mW ERP per regulations
* **Regulatory Compliance** - Modifying these would invalidate PMR446
  approval

### NC Variant Features (G18-PRO NC Only)

The **G18-PRO NC** variant adds three advanced features:

* **Noise Cancelling TX** (hardware feature) - Adaptive noise suppression during
  transmission for clearer audio. Requires dual receiver hardware in NC variant.
* **Dual Watch (DW)** (hardware feature) - Simultaneously monitor two channels
  with automatic switching on incoming transmissions. Requires dual receiver
  hardware in NC variant.
* **Only-CH Mode** - Restrict radio to single channel operation for tactical
  discipline and security

**Important Hardware Note**: Noise Cancelling TX and Dual Watch are **hardware
features** that require the NC variant's dual receiver chipset. These cannot be
enabled on standard G18-PRO radios even with PRG-G15 software, as the physical
hardware is not present.

**Availability**: All three features are only available on G18-PRO NC model
(requires PRG-G15 V1.1.25+). Standard G18-PRO does not support these features.
See
[NC Variants Documentation](../reference/NC_VARIANTS.md) for detailed
configuration instructions.

## Step-by-Step Programming Guide

### Preparation

* [ ] **Purchase Midland PRG-G15 Kit C1131** (€36 official, includes USB cable + software)
* [ ] **Backup existing settings** before programming (if possible)
* [ ] **Charge battery** to full capacity (prevents power loss during programming)
* [ ] **Install programming software** and USB drivers
* [ ] **Connect programming cable** securely to radio and computer

### Installing Software

1. **Download or Install PRG-G15**:
   * From CD/USB included with cable kit, or
   * Download from [Midland Support Page](https://support.midlandeurope.com/en_150/products/g18-pro)
2. **Install USB Drivers**: Follow software installer prompts
3. **Connect Cable**: Attach programming cable to radio and USB port
4. **Power On Radio**: Turn on radio before launching software
5. **Launch PRG-G15**: Open software and detect radio

### Basic Configuration (Front Panel Menu)

These settings can be configured without PRG-G15 software using the radio's
front panel menu:

* [ ] Set **TX Power** to Low via Menu > POW (both modes = 500mW)
* [ ] Set **TOT** to desired timeout (30-270 sec) via Menu > TOT
* [ ] Disable **VOX** initially via Menu > VOX > OFF
* [ ] Adjust **SQL** (Squelch) to level 5 via Menu > SQL
* [ ] Configure **CTCSS/DCS** via Menu > C-CDC/R-CDC/T-CDC

### Advanced Configuration (PRG-G15 Software Required)

These features require PRG-G15 programming software:

* [ ] **BCL (Busy Channel Lockout)**: Enable to prevent transmitting over active communications
* [ ] **Emergency Button**: Enable 3-second hold activation
* [ ] **FM Radio**: Enable broadcast receiver feature
* [ ] **Compander**: Enable audio compression
* [ ] **ROGER BEEP**: Enable end-of-transmission tone (optional)
* [ ] **VOICE Prompts**: Configure spoken announcements (on/off)
* [ ] **RRM Channel**: Configure Italy-specific channel (if applicable)

### Button Programming (Custom Setup)

#### Factory Default Assignments

* **PF3 Short Press**: Monitor (recommended to keep)
* **PF4 Long Press**: Scan (recommended to keep)

#### Optional Custom Programming

* [ ] **PF3 Long Press**: Assign to frequently-used function
  * Options: FM Radio toggle, VOX toggle, Channel Up/Down, or leave unassigned
* [ ] **PF4 Short Press**: Assign to quick-access function
  * Options: Power toggle (not recommended), Channel switch, or leave unassigned
* [ ] **Emergency Button**: Enable via PRG-G15 (3-second hold activation)

**Note**: Power toggle is not recommended since the G18-PRO defaults both Low and
High modes to 500mW ERP output (see manual: POW section). The toggle only changes
the display indicator without affecting actual transmission power.

### Testing and Validation

After programming, thoroughly test all configurations:

* [ ] **Test all button functions**: Verify PF3, PF4, Emergency button
* [ ] **Verify emergency alarm**: Test 3-second hold activation
* [ ] **Check power toggle**: Confirm menu access (if assigned)
* [ ] **Test FM radio**: Verify receiver operation (if enabled)
* [ ] **Validate scan**: Check channel scanning performance
* [ ] **Test CTCSS/DCS**: Verify privacy tones with another radio
* [ ] **Check TOT**: Verify timeout timer operation
* [ ] **Test VOX**: Verify voice activation (if enabled)

## Programming Safety and Best Practices

### Configuration Backup

* **Always backup settings** before making changes (if software supports)
* **Document all modifications** in a spreadsheet or text file
* **Test thoroughly** after programming
* **Keep backup configurations** available for restoration

### Validation Testing

* **Test all functions** after programming
* **Verify compliance** with local PMR446 regulations
* **Check operation** in target environment (tactical, hiking, etc.)
* **Confirm emergency features** work correctly

### Common Programming Issues

#### Radio Not Detected

* **Verify cable connection**: Ensure secure connection to radio and USB port
* **Check USB drivers**: Reinstall drivers if necessary
* **Try different USB port**: Some ports may have compatibility issues
* **Restart software**: Close and reopen PRG-G15
* **Power cycle radio**: Turn radio off and on

#### Programming Errors

* **Verify radio model**: Confirm PRG-G15 supports G18 PRO
* **Check battery level**: Ensure sufficient charge (>50%)
* **Restart programming**: Cancel and retry operation
* **Consult software manual**: Review troubleshooting section

#### Settings Not Saving

* **Complete programming cycle**: Follow all software prompts
* **Write to radio**: Ensure "Write" or "Program" command executed
* **Verify with radio**: Check settings via radio menu after programming
* **Test in field**: Confirm programmed features work as expected

## Programmable Features Reference

This section provides detailed explanations of all features configurable via PRG-G15 software or radio menu. For configuration recommendations, see the [Hybrid Profile Configuration Guide](HYBRID_PROFILE.md) and [Tactical Operations Guide](TACTICAL_OPERATIONS.md).

### BCL (Busy Channel Lockout)

* **Purpose**: Prevents transmission on channels already in use by other operators
* **How it Works**: Radio monitors channel before transmitting; blocks PTT if channel is busy
* **Benefits**:
  * Prevents interference with existing communications
  * Promotes radio etiquette and professional operation
  * Reduces risk of talking over emergency traffic
* **Use Cases**: Busy PMR446 channels in populated areas, tactical operations requiring coordination discipline, mixed-group operations with multiple teams
* **Configuration**: PRG-G15 > Channel Settings > BCL > Enable
* **Note**: Does not prevent others from transmitting over you

### VOX (Voice Operated Exchange)

* **Purpose**: Enables hands-free operation by automatically transmitting when it detects your voice
* **How it Works**: Microphone monitors audio input; PTT activates when sound exceeds sensitivity threshold
* **Settings**:
  * Sensitivity Levels: 1 (low) to 9 (high), or disabled
  * Delay: Configurable hold time after speech stops
* **Advantages**: Hands-free operation for climbing, cycling, skiing; useful when gloves make PTT difficult; allows operation while hands are occupied
* **Limitations**: Not suitable for noisy environments (wind, vehicles, crowds); may trigger on background noise; battery drain higher than manual PTT; less precise than manual PTT control
* **Recommendations**:
  * Disable for tactical/security operations (prevents accidental transmission)
  * Use sensitivity level 3-5 for quiet environments
  * Test thoroughly before relying on VOX in critical situations
* **Configuration**: PRG-G15 > VOX Settings > Enable + Sensitivity Level OR Front Panel Menu > VOX

### Scrambler (Voice Privacy)

* **Purpose**: Basic voice privacy through digital scrambling
* **How it Works**: Encodes audio signal; requires matching scrambler code to decode
* **Security Level**: **Not encryption-grade** - provides privacy against casual listeners only
* **Compatibility**: All radios in group must use identical scrambler settings; may not work across different radio brands; Midland proprietary implementation
* **Use Cases**: Privacy from casual eavesdroppers, deterring interference from neighboring groups - **NOT for sensitive/classified communications**
* **Limitations**: Can be defeated by scanner enthusiasts; may reduce audio quality; battery impact moderate
* **Configuration**: PRG-G15 > Channel Settings > Scrambler > Enable + Code Selection

### CTCSS/DCS Tones (Selective Calling)

* **Purpose**: Filters out unwanted transmissions from other users on the same frequency
* **How it Works**:
  * CTCSS: Continuous Tone-Coded Squelch System (50 analog tones, 67.0 Hz - 254.1 Hz)
  * DCS: Digital-Coded Squelch (105 digital codes)
  * Radio only unmutes when receiving matching code
* **Benefits**: Reduces interference on busy channels; creates "virtual private channels" on shared frequencies; standard feature compatible across all PMR446 radios
* **Limitations**:
  * Does **not** provide privacy (anyone can listen without tone)
  * Does **not** prevent others from transmitting on your channel
  * Purely a receive filter
* **Common CTCSS Frequencies**: 67.0 Hz, 71.9 Hz, 74.4 Hz, 77.0 Hz, 79.7 Hz, 82.5 Hz, 85.4 Hz, 88.5 Hz, 91.5 Hz, 94.8 Hz
* **Recommendations**: Use on channels 1-8 (PMR446 standard) in populated areas; coordinate codes with team members; use common tones for cross-brand compatibility
* **Configuration**: PRG-G15 > Channel Settings > CTCSS/DCS OR Front Panel Menu > C-CDC/R-CDC/T-CDC

### ROGER BEEP (End-of-Transmission Tone)

* **Purpose**: Audible confirmation tone when PTT is released
* **How it Works**: Brief tone transmitted at end of each transmission
* **Benefits**: Confirms PTT release (useful for beginners); indicates to listeners that transmission has ended; helps with group coordination ("over" signal)
* **Limitations**: May not be recognized or appreciated by non-Midland radios; can be annoying in mixed-brand groups; adds slight time to each transmission
* **Use Cases**: Training new radio operators, group coordination without voice "over" confirmations, accessibility for hearing-impaired operators
* **Recommendations**: **Disable for mixed-brand groups** (may cause confusion); enable for Midland-only teams if desired; test with team before deployment
* **Configuration**: PRG-G15 > Roger Beep > Enable/Disable

### VOICE Prompts (Spoken Announcements)

* **Purpose**: Spoken channel numbers and settings confirmations
* **How it Works**: Radio announces channel changes, mode switches, and settings via speaker
* **Languages**: Multiple language options available (varies by region)
* **Benefits**: Accessibility for visually impaired users; hands-free confirmation without looking at display; training aid for new operators
* **Limitations**: Breaks stealth operations (audible announcements); battery drain increases; may annoy team members in quiet environments
* **Recommendations**: **Disable for tactical/stealth operations**; enable for training or recreational use; useful for nighttime operations when display is hard to read
* **Configuration**: PRG-G15 > Voice Prompt > Enable/Disable + Language Selection

### Compander (Audio Compression)

* **Purpose**: Compresses audio on transmit, expands on receive for clearer communications
* **How it Works**: Reduces dynamic range to improve signal-to-noise ratio
* **Benefits**: Clearer voice in noisy environments; better audio intelligibility; helps overcome weak signal conditions
* **Limitations**: **Both transmit and receive radios must have compander enabled**; may not work with non-Midland radios; can introduce audio artifacts if only one radio uses it
* **Use Cases**: Noisy environments (wind, traffic, crowds), long-range communications, Midland-only radio groups
* **Recommendations**: **Disable for mixed-brand groups** (compatibility issues); enable for Midland-only teams in challenging audio conditions; test before relying on in critical situations
* **Configuration**: PRG-G15 > Compander > Enable/Disable

### Emergency Button

* **Purpose**: Distress signal transmission for emergency situations
* **How it Works**:
  * 3-second hold activates (prevents accidental triggering)
  * 30-second alarm tone transmission
  * 30-second open microphone transmission
  * Repeats until cancelled
* **Configuration Requirements**: Must be enabled via PRG-G15 (disabled by default)
* **Use Cases**: Injury or medical emergency, lost/separated from group, equipment failure in hazardous location, security threat
* **Best Practices**:
  * **Test regularly** to verify functionality
  * Coordinate emergency procedures with team
  * Ensure all team members know activation method
  * Have backup communication plan (whistle, mirror, flares)
* **Limitations**: Requires other radios to be monitoring your channel; battery drain high during extended activation; may not reach distant team members depending on terrain
* **Configuration**: PRG-G15 > Emergency Alarm > Enable + Test

### FM Radio (Broadcast Receiver)

* **Purpose**: FM broadcast reception for entertainment and emergency news monitoring
* **How it Works**: Radio switches from PMR446 transceiver to FM broadcast receiver mode
* **Frequency Range**: Typically 87.5-108 MHz (standard FM broadcast band)
* **Configuration Requirements**: Must be enabled via PRG-G15 (may be disabled by default)
* **Use Cases**: Entertainment during downtime, emergency news/weather updates, situational awareness during long deployments
* **Limitations**:
  * **Cannot receive PMR446 transmissions while in FM mode**
  * Battery drain significantly higher than PMR446 receive
  * Reception quality depends on antenna and location
  * Headphone recommended for extended listening
* **Recommendations**: Enable for recreational/camping use; use sparingly to conserve battery; always return to PMR446 mode when expecting communications
* **Button Assignment**: Typically PF3 long press toggles FM Radio mode
* **Configuration**: PRG-G15 > FM Radio > Enable/Disable

### RRM Channel (Italy-Specific)

* **Purpose**: Restricted Radio Mode channel for Italian PMR446 regulatory compliance
* **Regulatory Context**: Italy has specific PMR446 channel restrictions
* **Configuration**: Channel designation for RRM compliance
* **Use Cases**: **Italy only** - required for legal PMR446 operation
* **Note**: Users outside Italy do not need to configure this feature
* **Configuration**: PRG-G15 > RRM Channel > Select Channel (if applicable)

### TOT (Time-Out Timer)

* **Purpose**: Limits maximum continuous transmission time to prevent channel hogging
* **Settings**: 30-270 seconds (or disabled)
* **How it Works**: Automatically cuts transmission after timeout period; requires PTT release to reset
* **Benefits**: Enforces radio discipline; prevents accidental stuck PTT (button jammed open); conserves battery; ensures fair channel access for all users
* **Recommendations**: Set to 60-120 seconds for tactical operations; set to 180 seconds for recreational use; shorter timeout for busy channels
* **Configuration**: Front Panel Menu > TOT (30-270 sec) OR PRG-G15 > TOT Settings
* **Note**: Can be configured via radio menu without PRG-G15 software

### TX Power (Transmission Power)

* **Settings**: Low / High (front panel toggle)
* **Actual Output**: **Both modes = 500mW ERP** (regulatory compliance)
* **Regulatory Note**: PMR446 regulations lock maximum output to 500mW
* **Official Manual Quote**: "By default, both low and high power are set at 500mW"
* **Why Toggle Exists**: Display indicator only; no actual power difference
* **Recommendation**: Leave on either setting (no performance impact)
* **Configuration**: Front Panel Menu > POW (toggle Low/High)
* **Battery Impact**: None (identical power output)
* **Range Impact**: None (identical transmission power)

### Scan Modes

* **Purpose**: Automatically monitor multiple channels for activity
* **Scan Types**:
  * **TO (Time-Operated)**: 5-second pause on signal, then resume scanning
  * **CO (Carrier-Operated)**: Stop on signal, resume when signal ends
  * **SE (Search)**: Exit scan mode immediately on first signal
  * **Dual Watch (NC variant only)**: Simultaneously monitors two channels (requires dual receiver hardware)
* **How it Works**: Radio pauses on active channel, resumes scanning after transmission ends
* **Configuration**:
  * Scan Type: Front Panel Menu > SCANS > Select TO/CO/SE
  * Scan List: PRG-G15 > Scan Settings > Select Channels
  * Priority Channel: PRG-G15 > Scan Settings > Priority Channel
  * Channel Exclusion: Press ENT 4 seconds on any channel to toggle exclude/include status
* **Button Assignment**: Typically PF4 long press activates scan
* **Use Cases**: Monitoring multiple team channels, searching for active communications, emergency monitoring
* **Limitations**: Battery drain higher than single-channel monitoring; may miss brief transmissions during channel switching; Dual Watch requires NC variant hardware
* **Recommendations**: Limit scan list to relevant channels (reduces battery drain); use Priority Scan for primary team channel + monitoring others
* **Configuration**: Front Panel Menu > SCANS OR PRG-G15 > Scan Settings

## Mixed Radio Group Considerations

### Cross-Brand Compatibility

**Standard PMR446 Features** (work across all brands):

* **Frequencies**: 446.00625-446.19375 MHz
* **CTCSS/DCS Codes**: Standard tones and codes
* **PTT Operation**: Push-to-talk functionality
* **Channel Spacing**: 12.5 kHz

**Midland-Specific Features** (may not work with other brands):

* **ROGER BEEP**: May not be recognized by non-Midland radios
* **Compander**: Requires both radios to support and enable
* **Scrambler**: Proprietary implementation varies by manufacturer
* **FM Radio**: Midland-specific feature

### Recommendations for Mixed Groups

* **Use standard frequencies and CTCSS/DCS codes only**
* **Disable ROGER BEEP** if communicating with other brands
* **Disable Compander** unless all radios support it
* **Avoid proprietary features** for cross-brand compatibility
* **Test thoroughly** before deploying in critical situations

## PRG-G15 V1.1.25 Software Deep Dive

### Supported Radio Models

**Standard Models (Model Code 3)**:

* G18-PRO
* G15-PRO
* G18
* G15
* Arctic

**NC Variants (Model Code 4)**:

* G18-PRO NC
* G15-PRO NC

### Model Codes Explained

| Code | Model | Features | NC Support |
|------|-------|----------|------------|
| m3 | G18/G15/Arctic | Standard PMR446 | No |
| m4 | G18-PRO NC | Dual receiver, enhanced | Yes |

**Note**: Older model codes (m0-m2) were used in earlier G18/G15 variants but are
not supported by current PRG-G15 software.

### Software Configuration Files (.dat)

The software uses `.dat` files to store frequency and feature configurations:

**Standard Configuration Profiles**:

* `default.dat` - Factory defaults
* `PRO.dat` - Full 400-520 MHz band
* `PRO PMR.dat` - PMR446 only (446.00625-446.19375 MHz)
* `PRO PMR LPD.dat` - PMR446 + LPD band (69.0-87.0 MHz)
* `PRO PMR NEW.dat` - Updated PMR446 profile
* `PRO PMR LPD NEW.dat` - Updated PMR446+LPD profile

**NC Variant**: Uses same profile structure with NC feature parameters
pre-calibrated for Noise Cancelling TX and Dual Watch timing.

**Best Practice**: For most G18-PRO users, use `PRO PMR.dat` (PMR446-only,
ensures regulatory compliance).

### PRG-G15 Workflow

**3-Step Programming Cycle**:

1. **Read**: Load current radio settings into software
   * Software detects radio model automatically
   * Reads channel list, CTCSS/DCS settings, feature state
2. **Edit**: Modify settings in software interface
   * Adjust per-channel CTCSS, DCS, RX/TX attributes
   * Configure optional features (Emergency, VOX, etc.)
3. **Write**: Send modified settings back to radio
   * Software verifies changes before transmission
   * Radio updates internal memory and confirms

**Important**: Radio must remain powered and connected during entire cycle. Loss
of USB connection aborts operation.

### Advanced Settings and Optional Menus

**Accessible via PRG-G15 Software**:

* **Optional Menus**: NC features, Only-CH Mode, BCL, Compander
* **Advanced Settings**: Per-channel Noise Cancelling sensitivity, Dual Watch
  primary/secondary channel designation
* **Test Mode**: 14 test parameters for NC variant (10 for standard)

**Note**: Some settings only appear when appropriate radio model detected. NC
features absent if standard G18-PRO connected.

### Language Files

The software includes language support files:

* `lang_G18PRONC_en.xml` - English UI for NC variant
* `lang_G18PRO_en.xml` - English UI for standard variant
* Additional language variants available

**Configuration**: Set via software preferences (typically defaults to system
language).

### Troubleshooting: Resetting Software

If software fails to detect radio or settings appear corrupted:

1. Close PRG-G15
2. Navigate to PRG-G15 installation directory
3. Delete `setting.xml` (software configuration file)
4. Delete `config.xml` (radio detection cache)
5. Restart PRG-G15
6. Reconnect radio via USB

**Warning**: Deleting configuration files resets software to defaults, including
custom window positions and preferences.

### Version Compatibility

| Software Version | Model 3 Support | Model 4 Support | NC Features |
|---|---|---|---|
| V1.1.24 and earlier | ✓ Yes | ✗ No | Unavailable |
| V1.1.25+ | ✓ Yes | ✓ Yes | Available |

**Update Required**: If using G18-PRO NC, you **must** have PRG-G15 V1.1.25 or
later to access NC features (Dual Watch, Noise Cancelling TX, Only-CH Mode).

## Additional Resources

* **User Manual**: See `../manuals/` for English, German, and French manuals
* **Programming Software**: [PRG-G15 Download](https://support.midlandeurope.com/en_150/products/g18-pro)
* **Programming Cable Kit**: [Official Midland Store](https://www.midlandeurope.com/en_150/products/prg-g15)
* **Official Support**: [G18 PRO Support Page](https://support.midlandeurope.com/en_150/products/g18-pro)
* **Community Forums**: User experiences and programming tips

---

*For configuration profiles, see [HYBRID_PROFILE.md](HYBRID_PROFILE.md)*

*For tactical operations guide, see
[TACTICAL_OPERATIONS.md](TACTICAL_OPERATIONS.md)*
