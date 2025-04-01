# Dayak Kenyah Translator & MC Engine Plus

## Project Description

**Dayak Kenyah Translator & MC Engine Plus** is an advanced web application running on an ESP32 that facilitates translation between Indonesian and Dayak Kenyah. In addition to a real-time Translator and a Multiple Choice Engine (MC Engine), this project now includes a third module: the Fill-in Answer Engine. The new Fill-in Answer Engine allows users to receive answers for fill-in questions based on the context of the input, with the flexibility to choose the language of both the question and the answer independently.

This project is designed to operate on resource-constrained devices using a lightweight partial matching algorithm, ensuring fast response times and low power consumption. The system is particularly tailored for local language translation and educational purposes, making it a cost-effective solution compared to cloud-based or machine learning–driven competitors.

## README

### Introduction

The **Dayak Kenyah Translator & MC Engine Plus** project provides an innovative solution for language translation and automated question answering. Built on the ESP32 platform, it leverages a custom vocabulary (over 500 words/phrases) to support:
- **Translator**: Converts text between Indonesian and Dayak Kenyah in real time.
- **Multiple Choice Engine (MC Engine)**: Processes multiple choice questions by extracting keywords and matching them with provided options.
- **Fill-in Answer Engine**: Answers fill-in questions with the option for users to choose the input language and desired output language (Indonesian or Dayak), offering flexibility and improved accuracy.

### How to Use

#### 1. ESP32 Setup
- **Hardware**: Connect an ESP32 development board to your computer.
- **Software**: Use the Arduino IDE or PlatformIO.
- **Configuration**: Update the WiFi credentials in the source code and upload the firmware to the ESP32 board.

#### 2. Accessing the Web Application
- Open a modern web browser (e.g., Chrome, Firefox).
- Navigate to the IP address assigned to your ESP32.
- The web interface displays three distinct panels:
  - **Translator**
  - **Multiple Choice Engine**
  - **Fill-in Answer Engine**

#### 3. Using the Translator
- Enter Indonesian text into the Translator input box.
- The translation to Dayak Kenyah (or vice versa, based on the swap button) appears in real time.

#### 4. Using the Multiple Choice Engine (MC Engine)
- Enter a question (which can be multi-word) and the answer options separated by commas.
- Select the desired language pairing (e.g., "Question in Indonesian (Answer in Dayak)" or "Question in Dayak (Answer in Indonesian)").
- Click "Submit MC" to see the answer derived from the input using tokenization and refined partial matching.

#### 5. Using the Fill-in Answer Engine
- Select the language of the question and the desired language of the answer using two drop-down menus.
- Input the fill-in question.
- Click "Submit Fill-In" to receive the answer.
- The system will translate the question if the question language and output language differ. If they are the same, the question is returned as the answer.

### Required Hardware

- **ESP32 Development Board**
- **USB Cable** for programming the ESP32
- **Optional Accessories**: Breadboard, jumper wires, and other prototyping components as needed

### Software & Libraries

- **Arduino IDE or PlatformIO**: For writing and uploading the firmware to the ESP32.
- **WiFi.h**: For managing the ESP32's WiFi connection.
- **WebServer.h**: To implement a simple HTTP server on the ESP32.
- **ArduinoJson.h**: For parsing and deserializing the JSON dictionary containing the vocabulary.
- **Font Awesome (CDN)**: To supply icons for the web interface.
- **Google Fonts (Inter)**: For modern, legible typography.

### Competitor Comparison

#### Traditional Keyword Search Engines (Competitors)
- **Basic Keyword Matching**: Many traditional translation systems use straightforward keyword searches that simply look for exact or near-exact matches in a dictionary.
- **Limited Contextual Analysis**: These systems often do not handle multi-word phrases or context very well, leading to inaccuracies when a question is ambiguous or contains idiomatic expressions.
- **Static Dictionaries**: Competitors typically rely on static dictionaries without advanced processing, which can result in incorrect translations when partial matches occur.

#### Dayak Kenyah Translator & MC Engine Plus (This Project)
- **Lightweight & Efficient**: Uses a custom partial matching algorithm with tokenization that is highly optimized for low-resource environments like the ESP32.
- **Real-Time Performance**: Provides fast, real-time translation and question answering without the need for heavy cloud processing.
- **Local Focus**: Specifically tailored to translate between Indonesian and Dayak Kenyah with a curated vocabulary, making it more relevant for local language needs.
- **Cost-Effective & Offline Capability**: Can be deployed on inexpensive hardware with minimal infrastructure requirements, ideal for areas with limited connectivity.

### Comparison with the Previous Engine

#### Previous Engine
- **Features**: 
  - Translator (Indonesian ↔ Dayak Kenyah)
  - Multiple Choice Engine for answering MC questions
- **Limitations**:
  - Did not support fill-in answer questions
  - Less flexible in output language selection (jawaban otomatis tergantung pada bahasa soal)
  - Limited by only two features, making it less versatile untuk berbagai tipe pertanyaan

#### Dayak Kenyah Translator & MC Engine Plus (Current Engine)
- **New Feature**: 
  - **Fill-in Answer Engine**: Now supports answering fill-in questions with independent control over the language of the question and the answer.
- **Improvements**:
  - **Flexibility**: Users can choose whether they want the answer in Indonesian or Dayak, regardless of the language of the question.
  - **Enhanced Accuracy**: The refined partial matching algorithm minimizes incorrect translations (e.g., menghindari pencocokan "apa" dengan "apan").
  - **Broader Use Cases**: Now covers three distinct types of user input, making it more versatile for educational and practical applications.
  - **User-Controlled Output**: The new dropdown selections allow users to explicitly set both the question language and the desired answer language.

### Conclusion

**Dayak Kenyah Translator & MC Engine Plus** provides a comprehensive, efficient, and flexible solution for local language translation and question answering. Its lightweight architecture is optimized for resource-limited devices like the ESP32, and its user-friendly web interface delivers fast, real-time results. Compared to both cloud-based, machine learning competitors and our previous engine (which supported only two features), this enhanced version offers greater versatility, improved accuracy, and a more tailored approach for local language needs.
