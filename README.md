# test-psych-experiment
This program is a test to verify Pavlovia's operation.

## Overview
A simple Stroop task experiment implemented using jsPsych v7.1.2 with Pavlovia integration. The experiment includes:
- Welcome page with instructions (in Japanese)
- 3 Stroop task trials
- Thanks page
- Pavlovia data collection and session management

## Pavlovia Integration

This experiment uses the official Pavlovia plugin for jsPsych v7.1.2. The integration includes:

- **pavlovia_init**: Initializes the Pavlovia session at the start of the experiment
- **pavlovia_finish**: Saves data and closes the Pavlovia session at the end of the experiment
- **config.json**: Configuration file containing experiment settings for Pavlovia

### Configuration

The `config.json` file should be configured with your Pavlovia experiment details:
- `experiment.fullpath`: Your Pavlovia experiment path (e.g., "username/experiment-name")
- `experiment.name`: The name of your experiment
- `pavlovia.URL`: Pavlovia server URL (https://pavlovia.org)

## Usage

### Local Testing
1. Start a local web server:
```bash
python3 -m http.server 8080
```

2. Open your browser and navigate to:
```
http://localhost:8080/index.html
```

### Deployment to Pavlovia
1. Update the `config.json` file with your experiment details:
   - Set `experiment.fullpath` to your Pavlovia project path
   - Set `experiment.name` to your experiment name
2. Upload all files to your Pavlovia project repository:
   - `index.html` - Main experiment file
   - `config.json` - Pavlovia configuration
3. Set your experiment to "RUNNING" status on Pavlovia dashboard
4. Data will be automatically saved to Pavlovia when participants complete the experiment

### Local Testing (Pilot Mode)
When testing locally or in pilot mode, the experiment will offer a CSV file download instead of uploading to Pavlovia.

### Keyboard Controls
- **R** key: Red color
- **B** key: Blue color  
- **G** key: Green color

## Files
- `index.html` - Main experiment file with Pavlovia integration
- `config.json` - Pavlovia configuration file

## Dependencies
All dependencies are loaded from Pavlovia's CDN:
- jsPsych v7.1.2 (core library)
- jspsych-html-keyboard-response plugin
- jspsych-html-button-response plugin
- jspsych-7-pavlovia-2022.1.1 (official Pavlovia integration plugin)
