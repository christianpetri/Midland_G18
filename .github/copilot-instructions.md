# GitHub Copilot Instructions for Midland G18 Documentation

## Repository Purpose

This is a **documentation-only repository** for the Midland G18 PMR446 radio. It
contains no code - only markdown documentation, PDF manuals, and configuration
guides.

## Project Structure

*   `README.md` - Top-level index, quick start, and key specifications
*   `docs/guides/` - Configuration and programming guides (Leisure Profile,
    Professional Considerations, PRG-G15 Programming)
*   `docs/reference/` - Channel tables and NC variant features
*   `docs/manuals/` - Official PDF manuals (EN, GER, FRA) plus searchable
    markdown transcripts
*   `checklists/` - Operational checklists (Pre-Mission, Mission Execution,
    Post-Mission)
*   `.gitignore` - Excludes personal configs, radio programming backups
    (*.g18bak, *.codeplug), and editor files

## Documentation Philosophy

1.  **Structured Documentation**: Content is organized across `README.md`,
    `docs/guides/`, `docs/reference/`, `docs/manuals/`, and `checklists/`
2.  **License**: Unlicense (public domain equivalent) - use badge:
    `[![License](https://img.shields.io/badge/license-Unlicense-blue)](https://unlicense.org/)`
3.  **Target Audience**: Radio enthusiasts, professional teams, hikers, emergency
    preparedness users

## Content Organization Pattern

The documentation follows this structure hierarchy:

1.  **Frequency Information** - PMR446 compliance, frequency tables, technical
    limitations
2.  **Leisure Profile** - Configuration balancing professional and leisure use
3.  **Professional Considerations** - Checklists, protocols, security measures
4.  **Reference Material** - Performance specs, troubleshooting, compliance info

## Markdown Style Guidelines

Follow [Google's Markdown Style Guide](https://google.github.io/styleguide/docguide/style.html)
with these project-specific conventions:

### Headings

*   Use ATX-style headings (`#` syntax, not underlines)
*   Single H1 at document start matching filename
*   Add blank lines before and after headings
*   Capitalize following [Google Developer Style](https://developers.google.com/style/capitalization#capitalization-in-titles-and-headings)
*   Use descriptive, unique heading names to improve anchor link clarity

### Lists

*   Use 4-space indent for wrapped text and nested items
*   Prefer lazy numbering (`1.` for all items) in long lists
*   Use `- [ ]` checkbox format for checklists
*   Separate lists from surrounding content with blank lines

### Tables

*   Keep tables compact and scannable
*   Use reference links to avoid long URLs in cells
*   Align columns for source readability
*   Tables for: frequency lists, battery specs, range performance

### Code and Technical Terms

*   Use `backticks` for settings, modes, button names, frequencies
*   Examples: `PF3`, `Low Power`, `446.00625 MHz`
*   Use **bold** for emphasis on settings/modes in prose
*   Never use *italics* for technical terms

### Line Length

*   Wrap prose at 80 characters where practical
*   Exceptions: tables, long URLs, headings, code blocks
*   Improves diff readability and version control

## PMR446 Technical Context

*   **EU compliance**: PMR446 radios operate 446.00625-446.09375 MHz (8 channels)
*   **NOT compatible with**: FRS (462 MHz band, North America only)
*   **No license required** in Europe for PMR446 operation
*   **Switzerland specific**: Cannot receive 462.6875 MHz (out of band, no
    broadcasts exist there)

## Button Configuration Pattern

*   PF3: Monitor function (press) / FM Radio toggle (hold)
*   PF4: Scan channels (press) / Power level toggle (hold)
*   Emergency: 3-second hold activation (prevents accidental triggering)

## Editing Guidelines

*   Update date stamp at bottom: `*Last updated: YYYY-MM-DD*`
*   Maintain consistent badge styling with shields.io
*   Keep technical specifications accurate (ranges, battery life, frequencies)
*   Preserve checklist formatting for operational procedures
*   No trailing whitespace (use backslash for intentional line breaks)

## File Management

*   Personal configs and radio programming files (*.g18bak, *.codeplug, *.dat)
    should remain gitignored
*   PDF manuals in `docs/` are reference materials, not edited
*   No code files, build systems, or dependencies to manage
