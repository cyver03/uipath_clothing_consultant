# Robot 1 Clothing Consultant

A UiPath automation that checks tomorrow's weather for a city and recommends suitable clothing.

## What It Does

1. Prompts the user for a city.
2. Opens Google in Microsoft Edge.
3. Searches for tomorrow's weather in that city in degrees Celsius.
4. Reads the temperature and weather condition from the search results.
5. Displays an outfit recommendation in a message box.

The workflow also adds an umbrella reminder when the weather contains `rain`, `shower`, or `thunderstorm`.

## Temperature Recommendations

| Temperature | Recommendation |
| --- | --- |
| Below 15°C | Wear a duck down jacket. |
| 15°C to 33°C | Bring a light jacket if desired. |
| Above 33°C | Wear sunglasses. |

## Requirements

- UiPath Studio 26.0 or later
- Windows target runtime
- Microsoft Edge
- An internet connection
- Access to Google Search

The project uses these UiPath packages:

- `UiPath.System.Activities` 26.6.3
- `UiPath.UIAutomation.Activities` 26.10.3

## Run the Project

1. Open `Robot 1 Clothing Consultant/project.uiproj` in UiPath Studio.
2. Restore the project dependencies if prompted.
3. Open `Main.xaml` and run the workflow.
4. Enter a city when prompted.
5. Review the weather and clothing recommendation in the output message box.

## Project Structure

```text
Robot 1 Clothing Consultant/
├── Main.xaml          # Main automation workflow
├── project.json       # UiPath project configuration and dependencies
├── project.uiproj     # UiPath Studio project file
└── entry-points.json  # Process entry-point definition
```

## Notes

The workflow relies on Google and Microsoft Edge UI selectors, so changes to Google's page layout, browser configuration, or network availability may require selector updates in `Main.xaml`. The temperature value is converted directly to an integer, so the workflow expects Google to return a whole-number Celsius temperature.
