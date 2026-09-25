## Contributing Guidelines

**Good practice recommendations:**
- Always pull before starting work
- Always work in a new branch
- Commit often, merge branch asap
- Check GitHub issues frequently
- Update docs after work

### Branch Naming
```
[category]/[initials]-[short description]
```

**Category:**
- feature: new functionality
- fix: bugs
- docs: documentation

ie: feature/bl-imu-driver

### Commit Naming - Conventional Commits

```
type: short description
```

**Type: (examples)**
- feat: add controller for primary RPM
- fix: correct timeout in UART control
- docs: update wiring diagram in WIRING.md
- refactor: split harness.cpp into read/calibrate
- test: add unit test for GPS function

### File Header

**See also: .github/file_header_template.h**

Include the following snippet as a header in all project files.

Guidelines:
- Keep the Doxygen "@tag"s so we can use it later if needed.
- @hardware is one of the most important (The teensys SHOULD be labeled) -- this tells everyone how to use the file
- Delete any tags, including the @ symbol, if they aren't used.
- Add your name after the previous name in @author.

```
/**
 * @file        <filename.cpp/h>
 * @brief       <One-line summary of what this file does>
 *
 * @details     <Optional: a couple sentences of extra context — what problem
 *              this solves, how it fits into the overall system, etc.
 *              Delete this block if @brief already says enough.>
 *
 * @hardware    <Which Teensy (1 of 3), which pins/peripherals this touches.
 *              e.g. "Teensy 4.1 #2 - reads IMU on I2C1, drives motor PWM
 *              on pin 4">
 *
 * @depends     <Other files/headers this relies on, if not obvious from
 *              #includes. e.g. "Requires encoder.h ISR to be attached in
 *              main setup()">
 *
 * @rtos_note   <FreeRTOS-specific context, if applicable. e.g. "Functions
 *              here are called only from motorTask - NOT ISR-safe" or
 *              "Uses xQueue defined in shared_queues.h">
 *
 * @author      <Your name>
 * @date        <Date created, e.g. 2026-09-24>
 */

#ifndef <FILENAME>_H   // e.g. MOTOR_CONTROL_H — delete this ifndef guard block if this is a .cpp
#define <FILENAME>_H

// #includes here

#endif // <FILENAME>_H
```