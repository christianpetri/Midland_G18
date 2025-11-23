# G18-PRO NC (New Channel) Variants

**Last updated: 2025-11-23**

Documentation for the G18-PRO NC variants with enhanced features including Noise
Cancelling TX and Dual Watch functionality.

## Overview

The **NC** designation indicates the "New Channel" enhanced variant of the Midland
G18-PRO radio, introducing advanced features for professional and tactical
communications.

| Aspect | Standard G18-PRO | G18-PRO NC |
|--------|------------------|-----------|
| **Model Code** | 3 | 4 |
| **Software** | G18-PRO Programming Software | G18-PRO NC Programming Software |
| **Key Features** | Standard PMR446 | + Noise Cancelling TX + Dual Watch + Only-CH Mode |
| **Test Mode Columns** | 10 | 14 |
| **Configuration Profiles** | Standard | Enhanced with NC profiles |

## Key Features

### Noise Cancelling TX (New) – Hardware Feature

**Purpose**: Reduce background noise during transmission for clearer audio to
recipients.

**Hardware Requirement**: Enhanced signal processing chip (NC variant only)

- **Feature ID**: `id_1078` (Noise Cancelling TX)
- **Available On**: G18-PRO NC only (not compatible with standard G18-PRO)
- **Benefit**: Improves voice clarity in noisy environments (vehicles, industrial
  sites, tactical operations)

**Configuration**: Set per-channel in PRG-G15 software

```
Channel → Optional Features → Noise Cancelling TX → [On/Off]
```

### Dual Watch (DW) – Hardware Feature

**Purpose**: Monitor two channels simultaneously without manual switching.

**Hardware Requirement**: Dual receiver chipset (NC variant only)

- **Feature ID**: `id_F` (DW in key functions)
- **Configuration**: `D.W.main CH` (Dual Watch main channel)
- **Available On**: G18-PRO NC only (not compatible with standard G18-PRO)
- **Use Cases**:
  - Monitor primary tactical channel + secondary command channel
  - Maintain awareness of team frequency while monitoring dispatch
  - Emergency services: Primary unit frequency + repeater monitoring

**How It Works**:

1. Radio uses dedicated second receiver to monitor secondary channel
2. Set primary channel as main watch channel
3. Designate secondary channel in DW configuration
4. Radio automatically monitors both, prioritizing incoming transmissions on
   selected channel

### Only-CH Mode (New)

**Purpose**: Restrict radio to operate on a single selected channel only,
preventing accidental frequency changes during tactical operations.

- **Feature ID**: `id_1135` (Only-CH Mode)
- **Status**: Programmable via PRG-G15 software
- **Benefit**: Security and focus — prevents unauthorized channel switching

**Configuration**: Enable in PRG-G15 Optional Menus

```
Radio → Optional Menus → Only-CH Mode → [On/Off]
```

**Use Cases**:

- Tactical operations requiring strict frequency discipline
- Training scenarios where trainees should not change frequencies
- High-security communications requiring locked channels

## Programming Software Changes

### Test Mode Expansion

The NC variant includes 14 test mode columns and 14 test mode rows (vs. 10 columns and 21 rows in standard):

| Aspect | Standard G18-PRO | G18-PRO NC |
|---|---|---|
| **Test Columns** | 10 | 14 |
| **Test Rows** | 21 | 14 |
| **Channel Info Columns** | 15 | 15 |

**New test parameters** in NC variant (expanded test diagnostics):

- Noise Cancelling algorithm calibration
- Dual Watch switching timing
- Filter response validation
- Channel interleaving performance

### Configuration Folder Structure

**Standard Model (m3/m4)**:

- `default.dat` - Factory default
- `PRO.dat` - Standard 400-520 MHz
- `PRO PMR.dat` - PMR446 restricted
- `PRO PMR LPD.dat` - PMR446 + LPD band
- `PRO PMR NEW.dat` - Updated PMR446 profile
- `PRO PMR LPD NEW.dat` - Updated PMR446+LPD

**NC Model (m4 variant)**:

- All standard profiles available
- Enhanced with NC algorithm parameters
- Noise cancellation thresholds pre-calibrated
- Dual Watch timing optimized

## Hardware Compatibility

### Supported Models

- **G18-PRO NC** (Model 4) - Full support, all features enabled
- **G15-PRO NC** - Compact variant with same feature set
- **Standard G18-PRO/G15-PRO** - Compatible with PRG-G15 software, but NC
  features unavailable

### Firmware Requirements

- **Programming Software**: V1.1.25 or later required for NC support
- **Radio Firmware**: Check radio firmware version via:
  1. Power on radio
  2. Press `Menu`
  3. Navigate to `Radio Info` → `Version`
  4. Verify model shows "G18-PRO NC" or "G15-PRO NC"

## Feature Comparison

### Noise Cancelling TX Technical Details

**Algorithm**: Adaptive noise suppression

- Analyzes microphone input in real-time
- Identifies and filters background noise patterns
- Preserves voice frequency content (300-3400 Hz)
- Reduces noise floor while maintaining speech intelligibility

**Settings Available**:

- **Off**: Standard transmission (no processing)
- **On**: Enables adaptive noise cancellation
- **Sensitivity**: Per-channel tuning (via PRG-G15 advanced settings)

**Recommended Use**:

- ✅ Noisy environments (vehicles, construction, machinery)
- ✅ Tactical operations (wind noise, rotor blades)
- ✅ Professional communications (quality improvement)
- ⚠️ May reduce intelligibility at extremely low signal levels

### Dual Watch Configuration

**Setup Example** (Tactical Team):

1. **Primary Channel**: Team frequency (446.0625 MHz)
2. **Secondary Channel**: Command frequency (446.1875 MHz)
3. **DW Mode**: Enabled
4. **Priority**: Primary channel (auto-switch on activity)

**Audio Indication**:

- Beep/tone indicates secondary channel activity
- User can switch manual focus if needed
- Transmission defaults to primary unless switched

## Programming Instructions

### Enable Noise Cancelling TX

1. **Open PRG-G15 Software** (V1.1.25+)
2. **Load Radio Codeplug** (Read from radio)
3. **Navigate**: `Channel Info` → Select channel
4. **Check feature**: `Optional Features` → `Noise Cancelling TX`
5. **Save & Write** to radio

### Configure Dual Watch

1. **Open PRG-G15 Software**
2. **Navigate**: `Radio` → `Optional Menus`
3. **Set**: `D.W.main CH` → Select primary monitoring channel
4. **Configure**: `Dual Watch` → On
5. **Secondary Channel**: Assign in channel list
6. **Save & Write** to radio

### Enable Only-CH Mode

1. **Open PRG-G15 Software** (V1.1.25+)
2. **Load Radio Codeplug** (Read from radio)
3. **Navigate**: `Radio` → `Optional Menus`
4. **Find**: `Only-CH Mode` → Set to `On`
5. **Select**: Single channel to lock radio to
6. **Save & Write** to radio

**After enabling**:

- Radio will only transmit/receive on selected channel
- All other channels become unavailable until mode is disabled
- Useful for training or secure operations

## Troubleshooting

### NC Features Not Appearing in Software

**Problem**: Noise Cancelling TX and Dual Watch options hidden

**Solutions**:

1. Update PRG-G15 to V1.1.25 or later
2. Verify radio model is G18-PRO NC (not standard G18-PRO)
3. Delete `setting.xml` in PRG-G15 directory, restart software
4. Re-import codeplug file

### Noise Cancellation Too Aggressive

**Symptom**: Voice sounds robotic or speech clipped

**Adjustment**:

1. Open PRG-G15 advanced settings
2. Reduce `Noise Cancelling TX` sensitivity per-channel
3. Test transmit in similar environment
4. Iterate until clarity achieved

### Dual Watch Not Switching

**Symptom**: Only receives on primary channel, secondary ignored

**Check**:

1. Verify Dual Watch enabled in `Optional Menus`
2. Confirm secondary channel configured and valid frequency
3. Test receiver sensitivity on secondary channel (use Test Mode)
4. Check if secondary channel SQL (squelch) level too high

## Version History

| Software Version | Model | NC Support | Notes |
|---|---|---|---|
| V1.1.25 | G18-PRO/G15-PRO | Model 4 (NC) | NC features introduced |
| V1.1.24 and earlier | G18-PRO/G15-PRO | Model 3 only | Standard features only |

## Related Documentation

- [Programming Guide](../guides/PROGRAMMING.md) - General PRG-G15 usage
- [Tactical Operations](../guides/TACTICAL_OPERATIONS.md) - Dual Watch deployment
- [Channels Reference](CHANNELS.md) - Frequency and configuration guide
- [Official Manuals](../manuals/) - Complete technical specifications

## References

**Programming Software**: G15G18PRO V1.1.25

- Language files: `lang_G18PRONC_en.xml`, `lang_G18PRONC_en.xml`
- Supported models: G15PRO, G15PRONC, G18PRO, G18PRONC
- Factory default configurations: m0-m4 model variants

**Regulatory Note**: All NC features operate within PMR446 compliance (446.00625-446.19375
MHz) and comply with European radio regulations. Feature availability varies by
jurisdiction.

---

*This document is based on analysis of PRG-G15 software V1.1.25 and official
Midland documentation. Features and specifications subject to change without
notice.*
