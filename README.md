# Property Inspection Report Generator - README

![Screenshot 2025-03-07 121815](https://github.com/user-attachments/assets/d918ecfc-4983-4b71-9578-33818525de1b)

![Screenshot 2025-03-07 121829](https://github.com/user-attachments/assets/a80b7142-7918-4570-8ec7-5632c259aee9)

![Screenshot 2025-03-07 121843](https://github.com/user-attachments/assets/a5b543b5-fbc7-4087-9c84-d03869a8c2df)









## Overview

The **Property Inspection Report Generator** is an AI-powered web application designed to create detailed property inspection reports based on standard checklists and observed issues. It utilizes multiple language models to generate structured, insightful reports, aiding real estate professionals in making informed decisions.

## Features

- Generate structured property inspection reports based on user inputs
- Supports multiple property types, including residential, commercial, industrial, and vacant land
- Utilizes five different LLM models for diverse, high-quality outputs
- Provides a professional and detailed assessment of property conditions
- Easy-to-use web interface with customizable report parameters

## Prerequisites

- Python 3.8+
- FastAPI and its dependencies
- Open WebUI access (https://chat.ivislabs.in) and/or local Ollama installation

## Installation Steps

1. **Set Up Project Directory**
   - Create the main project directory
   - Organize files into templates and static folders for UI and assets

2. **Install Dependencies**
   - Run the following command to install required packages:
     ```sh
     pip install fastapi uvicorn jinja2 httpx
     ```

3. **Configure API Settings**
   - Set up API keys for Open WebUI if using external models
   - Ensure local Ollama is installed and running for fallback model usage

4. **Run the Application**
   - Start the FastAPI application using:
     ```sh
     uvicorn main:app --reload
     ```
   - Open your browser and access the application at `http://localhost:8000`

## Using the Application

### Step 1: Enter Property Details
1. Select the property type (residential, commercial, etc.)
2. Enter property age and past renovations
3. Provide details on observed issues
4. Choose the number of insights required
5. Select the language model for report generation

### Step 2: Generate Report
1. Click on the "Generate Report" button
2. The system processes the inputs and fetches structured insights
3. The report is displayed in an easy-to-read format

### Step 3: Review & Utilize the Report
1. Review the generated report
2. Copy or download the report for documentation purposes
3. Use insights to make informed property-related decisions

## How It Works

1. **User Inputs Data**
   - The user enters property details through the web interface.

2. **Application Processes Request**
   - The system structures the input into a prompt suitable for LLMs.
   - Attempts to use Open WebUI first; falls back to local Ollama if unavailable.

3. **LLMs Generate Report**
   - The AI model analyzes inputs and provides structured property insights.

4. **Report Display**
   - The formatted report is displayed in the UI for user review.

## LLM Models Used & When to Use Them

- **Gemma2:2b** - Best for general-purpose property reports with detailed insights.
- **Qwen2.5:0.5b** - Ideal for quick, concise reports with essential information.
- **DeepSeek-R1:1.5b** - Suitable for in-depth technical property evaluations.
- **DeepSeek-Coder:Latest** - Focuses on structured, logical report generation.
- **Granite Model** - Optimized for real estate and property-specific language generation.

## Troubleshooting

### API Connection Issues
- Ensure Open WebUI is accessible and API keys are correctly configured.
- Check the local Ollama installation for fallback processing.

### Model Availability Issues
- Verify that the selected LLM model is accessible.
- Restart the service to refresh available models.

### Report Generation Errors
- Try adjusting input details for a more structured prompt.
- Switch to a different model for optimized results.

## Customization Options

- Modify prompt templates for different types of property reports.
- Adjust UI design and styling to enhance user experience.
- Integrate additional LLM models for varied report structures.
- Extend report functionalities with additional property assessment parameters.

