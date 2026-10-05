# FYP-Project

## Abstract

AURA is a low-cost, wirelessly connected embodied-AI platform that turns natural-language goals into reliable physical task execution. An LLM-based agent plans and acts through a tool-based API, while a **separate, independent evaluator** checks task completion from real camera and sensor evidence — rather than trusting the agent's own self-reported success. The system runs on a 6-DOF servo arm with an ESP32-S3 controller and an overhead camera, communicating over Wi-Fi, which means every observation has latency and every command can be delayed or lost.

The project studies two core questions: (1) does closed-loop replanning with independent verification improve task reliability compared to open-loop LLM planning, especially under real-world disturbances like failed grasps or moved objects, and (2) how do network conditions — delay, packet loss, stale frames — affect that reliability. Four system configurations (scripted, open-loop, closed-loop, and closed-loop with independent verification) are compared through controlled trials with physical disturbance injection.

The goal isn't a production-grade robot, but a reproducible, student-scale testbed for studying *execution reliability* in agentic AI — where an agent's confidence and the physical ground truth are allowed to diverge, and the system is built to catch that gap instead of ignoring it.
