GitHub Application Modernization Workshop user guide

To avoid challenges caused by differences in individual local computer environments, we will use GitHub Codespaces throughout the entire process.

## 🛠️ Phase 1: Preparation (Required Before the Lab)
Before starting the environment, please make sure you have completed the following setup:
GitHub Account Permissions
Ensure your account has GitHub Copilot Business, Copilot Pro, or higher-level access.
Local Software Installation
Install Visual Studio Code.
In the VS Code Extensions Marketplace, search for and install the GitHub Codespaces extension.
Network Environment
It is recommended to maintain a stable network connection during the lab.
If you experience disconnections while using Wi-Fi, please try switching to a mobile hotspot.
## 🏗️ Phase 2: Launch the Lab Environment
We will start a standardized cloud-based container environment that comes preinstalled with JDK 8, Maven 3.6+, and Docker.
Fork the repository
https://github.com/yym2020/Copilot-App-Modernization-Java-Lab
to your GitHub account. Do not change the repository name.
Click the <> Code button and switch to the Codespaces tab.

Key step: Click … (More options) → New with options…
On the configuration page:
Branch: Select main.
Dev Container Configuration: Make sure to select Java App Modernization Lab.
Region: Choose the region closest to you (for example, Southeast Asia or East US).
Machine Type: Select 2-core.

Click Create codespace。
## Phase 3: Connect to Local VS Code (Recommended)
Although the lab can run in a browser, using local VS Code provides a better Copilot experience.
Wait for the cloud environment to initialize (approximately 3–5 minutes).
After the environment starts, click the “Codespaces” status bar in the lower-left corner.
Select “Open in VS Code Desktop.”

In the locally opened VS Code window, confirm that the lower-left corner shows
Codespaces: <name>.

In the local VS Code window, when prompted for the default configuration, select “No” as shown in the diagram.

## Phase 4: Environment Validation and Execution
After the environment starts, it will automatically run the initialization scripts.
Please check the following in the VS Code terminal:
Open the Terminal window in VS Code.


Verify version information.
Run the following commands to confirm that the environment is set up correctly:
java -version   (should display 1.8.x)
mvn -version    (should display 3.6.x or later)

Run the initial application.
In the terminal, navigate to the project directory and build the application:
./scripts/startapp.sh

Access the application.
After the terminal indicates that the application has started successfully, locate the corresponding web application’s locally mapped URL in the VS Code Ports panel.

Click to access the Asset Manager application.

## Phase 5: Start Application Modernization (By Copilot App Modernization extension- AI agent)
You are now ready to use GitHub Copilot App Modernization to refactor the codebase!
Click the GitHub Copilot App Modernization icon in the left sidebar, then click Start Assessment to begin evaluating the repository.

View the assessment process

After approximately 5 minutes, review the assessment results.

Upgrade Java Runtime & Framework (approximately 10–15 minutes)


After the upgrade is complete, review the upgrade report:

## Phase 6: Customized Assessment Report- OPTIONAL ITEM
The data files for the App Modernization assessment report are saved by default in the following directory:
./.github/appmod/appcat

You can generate new customized reports based on the default report data for customer presentations.
The repository already contains prompt files for report customization as well as sample custom-generated report files.

Add the assessment-generated report data files report.json and result.json, along with the custom report prompt file report-prompt-sample.md, to the Copilot Chat conversation context, and then enter the appropriate instructions.





