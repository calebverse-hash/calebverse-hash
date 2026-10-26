# Project Archangel — Search-and-Rescue Drone / Rover Concept

**Role:** Independent concept development and early systems planning  
**Stage:** Exploratory concept; paused after project-priority change

## Vision
Explore coordinated indoor search-and-rescue using an unmanned drone and rover. The engineering emphasis moved from mapping toward **reliable inter-vehicle communications**.

## Work explored
- Defined indoor mission conditions, sensing objectives and initial architectural tradeoffs.
- Studied roles of command, telemetry, sensing and coordination messages.
- Explored PX4, ArduPilot and Gazebo tooling on macOS; investigated initial SITL setup issues.
- Considered communications loss handling, onboard autonomy boundaries and verification tests.
- Scoped hardware, funding, milestones and possible faculty collaboration.

## Engineering questions
How are messages prioritized? What happens during link dropouts? Which safety actions must remain onboard? What packet loss/latency tests would prove a link is usable?

**Status:** This is not a demonstrated integrated autonomous system. The original Archangel repository remains private. This case study documents conceptual systems work, not a completed build.
