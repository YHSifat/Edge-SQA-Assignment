# Edge SQA Assignment - Parabank User Registration and Login Test

This project contains an automated test for the Parabank website that handles user registration and login functionality using CSV data.

## Prerequisites

- Visual Studio (2019 or later recommended)
- .NET Framework or .NET Core
- Chrome browser installed
- ChromeDriver compatible with your Chrome version

## Setup Instructions

1. Create a new Console Application project in Visual Studio:

   - Launch Visual Studio
   - Select "Create a new project"
   - Choose "Console App (.NET Framework)" or "Console App (.NET Core)"
   - Name your project and click "Create"

2. Install Required NuGet Packages:

   - Right-click on your project in Solution Explorer
   - Select "Manage NuGet Packages"
   - Search for and install the following packages:
     - `Selenium.WebDriver`
     - `Selenium.WebDriver.ChromeDriver` (make sure to select the version compatible with your Chrome browser)
     - `ExtentReports`
     - `CsvHelper`

3. Configure the Project:

   - Copy the provided `code.cs` file into your project
   - Replace the Program.cs content with the provided code
   - Place the `User_Registration_Data.csv` file in your project's root directory

4. Update File Paths:
   - Open the `code.cs` file
   - Update the report file path in line 22: `string reportFilePath = $@"D:\sqa\{dateTime}.html";`
   - Update the CSV file path in line 27: `using (var reader = new StreamReader(@"D:\sqa\User_Registration_Data.csv"))`
   - Ensure both paths point to valid locations on your system

## Running the Tests

1. Build the solution by pressing Ctrl+Shift+B or selecting "Build Solution" from the Build menu
2. Run the application by pressing F5 or clicking the "Start" button
3. The test will:
   - Launch a Chrome browser
   - Navigate to the Parabank website
   - Register users with data from the CSV file
   - Log out each user after registration
   - Log in with the registered credentials
   - Validate successful login
   - Generate an HTML report with test results

## Test Report

After running the test, an HTML report will be generated at the location specified in `reportFilePath`. This report contains detailed information about each test step and its outcome.

## Troubleshooting

- Make sure ChromeDriver version matches your Chrome browser version
- Verify that all NuGet packages are installed and compatible
- Ensure the CSV file path and report file path are correctly configured
- Check that the CSV file is properly formatted with the expected column headers

## Notes

This test suite was developed by Yusuf Hasan from the Department of CSE at Jagannath University.
