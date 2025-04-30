--

# Project Name  
**HealthCopilotAssist**

---

## Description  
**HealthCopilotAssist** is an AI-powered virtual assistant built using Microsoft Copilot Studio and OpenAI integration, designed to streamline patient care and hospital resource management. It enables real-time symptom-based doctor matching, ambulance triage, and seamless data intake from hospitals — all through natural language interaction.

Built with scalability and real-world usability in mind, this assistant is ideal for healthcare providers, emergency response teams, and patient helpdesk systems.

---

## Key Features  

### 🤖 Natural Language Understanding:
- **Symptom-Based Doctor Finder:** Patients can enter symptoms like *“chest pain”* or *“stomach ache”*, and Copilot maps them to the right doctors using specialty, experience, and rating.
- **Conversational Interface:** Understands and responds in everyday language, reducing friction for users.

### 🚑 Ambulance Availability & Routing:
- **Live Ambulance Check:** Patients can ask for available ambulances based on their location.
- **ETA Integration with Bing Maps API:** System suggests the fastest ambulance with live traffic-based ETA and provides direct contact.

### 🏥 Hospital Data Upload Portal:
- **Unified Interface for Hospitals:** Hospitals can upload doctor and ambulance availability via Excel sheets or Copilot prompts.
- **Data Sync with Dataverse:** Updates are stored in Dataverse tables and used in real-time matching.

---

## Industry Use Cases  

### Patient-Facing:
- **Example:** A patient with high fever types “I feel weak and hot” → Copilot suggests 3 doctors in General Medicine with availability, ratings, and hospital details.

### Emergency Services:
- **Example:** User types “I have chest pain at Koramangala” → Copilot calls OpenAI to assess risk, pulls nearby ambulances from Dataverse, calculates ETA with Bing Maps.

### Hospital Staff Interaction:
- **Example:** A hospital admin uploads the latest doctor and ambulance shift availability using Copilot interface.

---

## Technical Capabilities  

### 🧠 AI and Copilot Integration:
- Uses OpenAI for:
  - Symptom triage
  - Emergency escalation decision-making
  - Response generation for doctor recommendations

### 💾 Data Management:
- Built on **Microsoft Dataverse** with tables for:
  - Doctors (name, department, rating, availability)
  - Ambulances (location, status, contact)
  - Logs (availability updates, patient interactions)

### 🔄 Automation & APIs:
- Optional Power Automate flows for:
  - Fetching real-time traffic/ETA from Google Maps
  - Sending alerts or notifications
- Optional Azure Functions for backend calculations

---

## Workflow Diagram  
`HealthCopilotWorkflow.png`  
_(Include visual showing: User ➝ Copilot ➝ OpenAI + Dataverse + Maps API ➝ Output)_

---

## Setup Instructions  
1. **Dataverse Tables**: Create tables for `Doctors`, `AmbulanceAvailability`, `Hospitals`.
2. **Copilot Topics**:
   - “Find a Doctor”
   - “Need an Ambulance”
   - “Upload Hospital Data”
3. **OpenAI Integration**:
   - Connect via Azure OpenAI or custom HTTP connector.
   - Use structured prompts to match symptoms → departments.
4. **(Optional) Power Automate**:
   - Set up Bing Maps API flow.
   - Trigger from Copilot to fetch ETA.
5. **Generative Answers**:
   - Enable GPT-based responses for dynamic user interaction.

---

## Conclusion  
**HealthCopilotAssist** empowers patients and hospital staff with real-time, intelligent decision-making support — from symptom recognition to ambulance routing and doctor selection. Built with extensibility and accuracy at its core, it transforms traditional hospital systems into conversational, AI-assisted solutions ready for modern healthcare challenges.

---
