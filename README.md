# Spot & Stud Weld Inspection System (YOLO-based)

This is an industrial-grade machine vision project for detecting and inspecting weld points and stud welds on car body components, developed and deployed at **Iran Khodro**.

## Project Summary

- **Location**: Engine compartment inspection station  
- **Purpose**: Automate quality control of welds before paint and assembly  
- **Goal**: Detect missing, misaligned, or defective weld and stud points  
- **Previous method**: Manual visual inspection  
- **Improvement**: Significant reduction in missed defects and improved consistency

## Features

- Uses a **fixed industrial camera and lighting system**
- Inspects multiple weld types:
  - Spot welds
  - Stud welds
  - Tucker fasteners (clips/rivets)
- Performs:
  - Presence/absence detection
  - Edge damage / burr / sealer overflow inspection
  - Misalignment and missing weld point detection (2nd phase)
- Real-time inference using YOLO object detection model

## Workflow

1. PLC halts the vehicle at inspection station
2. Camera captures high-resolution image
3. Image is sent to a Python-based system
4. YOLOv5 model detects and classifies each weld point
5. Detected objects are drawn and results returned for operator or automation system

## Tools & Technologies

- `Python`
- `YOLOv5`
- `OpenCV`
- `snap7` (PLC communication)
- `NumPy`, `Pillow`, etc.

## Sample Output

![Sample Output](./images/weld_inspection_result.jpg)

- Green: OK weld/stud  
- Red: Missing or defective  
- Unique ID for each weld point

## Results

- Increased inspection speed and consistency
- Easily updatable model for new vehicle models or component changes
- Modular Python code integrated with factory PLC via `snap7`

## Author

Industrial Automation & Machine Vision Engineer  
[Z Falaki] — 10+ years in automotive industry  
LinkedIn / Portfolio: [Zobeideh Falaku]
