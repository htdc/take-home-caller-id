# HotDoc Caller ID

## START HERE

This repo is part of a take home project for candidates for a Security role. Please see START_HERE.md for more instructions!

## What is this project?

The Caller ID feature allows Receptionists and Practice Managers at HotDoc Practices to see who is calling when the phone rings. The phone number is also used to match with potential patients in the practice's own medical software. If a matching patient is found, it also shows relevant information about the patient, including name and address, upcoming appointments, and allows quick shortcuts for creating and updating appointments for the patient.

## Components

There are 4 main components involved in the Caller ID feature, briefly listed here:

- This repo (The "Caller ID service")

Runs on a server somewhere in the cloud, in charge of accepting incoming Webhooks, and publishing events to the HotDoc Sidebar

- The HotDoc Sidebar:

An installed program that runs on a computer within a clinic. For Caller ID, it subscribes to events from the Caller ID service, and when an incoming call event is received, looks up potential matching patients from the practice's own medical software.
[Support content here](https://support.hotdoc.com.au/hc/en-gb/articles/204145710-How-to-open-the-HotDoc-Sidebar)

- The HotDoc Dashboard

The web app used by Clinics to configure HotDoc. For Caller ID, it can be used to generate a config file to be used to configure the Clinic's phone systems.
[Support content here](https://support.hotdoc.com.au/hc/en-gb/articles/204145740-Opening-the-HotDoc-Dashboard)

- The Clinic's Phone System

Reponsible for receiving phone calls, and, once configured, sends out Webhook requests to the Caller ID service when the phone rings.

## Diagram
![image](https://user-images.githubusercontent.com/5941208/139188485-f591f49a-a71b-4611-b3a7-991da97cc677.png)
