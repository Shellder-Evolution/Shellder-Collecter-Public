# Shellder Collection Tool

## Description
The CAPTCHA Collection Tool is a user-friendly application designed to help collect and label CAPTCHA data. It features an intuitive GUI and automatically uploads collected data to a public GitHub repository. This tool is ideal for creating datasets for AI models.

---

## Features
- Collect and save CAPTCHA images and labels.
- Automatically upload data to a public GitHub repository.
- Simple and intuitive GUI for starting/stopping collection and viewing logs.
- Configurable via a YAML configuration file.

---

## How It Works
1. **Start the Tool**: Launch the application and click the `Start` button to begin collecting CAPTCHA data.
 You must still select by hand, make sure you only select your captcha. 
 The tool shows you your screenshot with the captcha captured in a window. When you confirmed this is right it only uploads the captcha.
2. **Automatic Data Handling**:
   - Images and labels are saved locally with unique filenames.
   - Data is automatically uploaded to a configured GitHub repository.
3. **Logs**: The application displays logs in the GUI to show the progress and status of collection and uploads.
4. **Stop the Tool**: Click the `Close and Upload` button to halt data collection and upload the images to a central point.

---

## Configuration
The tool uses a `config.yml` file for settings. Below is an example configuration:

```yaml
repository:
  upload_enabled: true                  # Set to true to enable uploads, false to disable

data:
  folder: "./data"                      # Local folder to store images and labels

logging:
  enabled: true                         # Enable or disable logging
  log_file: "collector.log"             # File to save logs (optional) 
  ```