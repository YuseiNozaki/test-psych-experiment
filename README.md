# test-psych-experiment
This program is a test to verify Pavlovia's operation.

## Overview
A simple Stroop task experiment implemented using jsPsych v8. The experiment includes:
- Welcome page with instructions (in Japanese)
- 3 Stroop task trials
- Thanks page

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
Simply upload the `index.html` file to your Pavlovia project. All dependencies are loaded from CDN.

### Keyboard Controls
- **R** key: Red color
- **B** key: Blue color  
- **G** key: Green color

## Files
- `index.html` - Main experiment file (standalone, all dependencies loaded from CDN)

## Dependencies
All dependencies are loaded from unpkg.com CDN:
- jsPsych v8.0.0
- @jspsych/plugin-html-keyboard-response v2.0.0
- @jspsych/plugin-html-button-response v2.0.0
