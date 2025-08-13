Multi-Agent AI Hospital OPD Assistant
An AI-powered multi-agent chatbot system designed to streamline outpatient department (OPD) operations at hospitals. Built using n8n automation workflows, this project intelligently manages appointment booking, patient guidance, feedback evaluation, and communication to improve hospital efficiency and patient experience.

Overview
This project consists of two AI agents that work collaboratively to handle patient interactions:

Main Agent
Acts as the entry point for patient queries. It detects if the patient requests a direct appointment with a specific doctor or seeks help based on symptoms/medical issues.

Agent 1 (Booking & Tracking Agent)
Responsible for:

Checking doctor's appointment availability

Booking appointments

Tracking patient’s journey to the hospital

Monitoring hospital crowd and traffic conditions

Sending timely notifications and reminders

Agent 2 (Feedback & Doctor Recommendation Agent)
Activated when the patient doesn't specify a doctor but mentions symptoms or medical issues.

Utilizes a vectorized feedback database containing patient feedback linked to doctors

Matches patient issues with the most appropriate doctor

Ensures fair opportunity for junior doctors through balanced recommendations

After confirmation, routes booking to Agent 1

Project Components
File

Description

Ai agent.json

Main AI agent handling patient query routing

Confirmation Agent.json

Handles email confirmations and notifications

Feedback Automation.json

Processes and vectorizes patient feedback data

How It Works
Patient Interaction:

The main agent receives the patient's query.

If a specific doctor is requested, it forwards the conversation to Agent 1.

If no doctor is specified, Agent 2 analyzes patient symptoms against the feedback database to recommend a doctor.

Appointment Booking & Tracking (Agent 1):

Checks the doctor's appointment list for available time slots.

Books the appointment and registers patient details.

Monitors hospital crowd levels and road traffic.

Sends morning reminders and live updates to the patient until arrival.

Feedback Processing (Agent 2):

Converts patient feedback into vector embeddings for similarity search.

Matches patient issues with doctors based on past feedback and expertise.

Balances recommendations to include junior doctors.

Transfers control to Agent 1 for booking.

Email Confirmation:

Upon successful booking, the confirmation agent sends email notifications to patients.

Technologies Used
n8n: Workflow automation platform used to orchestrate AI agents and processes

AI Chatbot Models: For natural language understanding and intent detection

Vector Database: For storing and searching patient feedback embeddings

Email Automation: For booking confirmations and reminders

Getting Started
Prerequisites
n8n installed and running (locally or cloud)

Access to vector database and email SMTP service

JSON workflows (Ai agent.json, Confirmation Agent.json, Feedback Automation.json) imported into n8n

Installation
Clone this repository:

git clone https://github.com/yourusername/multi-agent-hospital-opd.git
cd multi-agent-hospital-opd

Import the n8n workflows from the provided JSON files into your n8n instance.

Configure environment variables and API keys for vector database and email services.

Start the n8n workflow automation.

Usage
Patients can interact with the chatbot via your hospital’s OPD interface (web/app).

The system automatically handles appointment booking and feedback-based doctor recommendations.

Hospital staff can monitor appointments and patient flow through the n8n dashboard.

Future Improvements
Integrate real-time traffic API for enhanced patient routing.

Add multi-language support for chatbot communication.

Expand feedback vectorization with more sophisticated NLP models.

Enable voice-enabled patient interaction.

Contributing
Contributions are welcome! Feel free to submit issues or pull requests.

License
This project is licensed under the MIT License.

Contact
For questions or support, contact Your Name.

Built with ❤️ using n8n and AI technologies to improve hospital OPD experience.
