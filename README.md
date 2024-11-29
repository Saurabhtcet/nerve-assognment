# Nerve Solutions Strategy Selector

## Project Overview

This is a web application designed to help users explore and filter investment strategies across different market views and dates. The application allows users to:
- Switch between market views (Bullish, Bearish, RangeBound, Volatile)
- Select different dates
- View strategies with their occurrence count

## Features

- **Dynamic View Toggle**: Easily switch between four market views
- **Date Dropdown**: Select from predefined dates
- **Strategy Cards**: 
  - Display strategy names
  - Show strategy count
  - Adaptive labeling (Strategy/Strategies)
- **Empty State Handling**: Shows a message when no strategies are available

## Technology Stack

- **HTML5**: Structural markup
- **CSS3**: Styling and responsiveness
- **Vanilla JavaScript**: Dynamic interactions and data management

## Project Structure

```
nerve-solutions/
│
├── index.html        # Main HTML file containing entire application
├── README.md         # Project documentation
└── screenshot.png    # Optional: Application screenshot
```

## Code Breakdown

### HTML Structure

The HTML provides the basic structure with three main components:
1. View Toggle Buttons
2. Date Dropdown
3. Strategies Container

```html

    Bullish
    Bearish
    RangeBound
    Volatile




```

### CSS Styling

Key styling features:
- Flexbox for responsive layout
- Interactive button states
- Clean, minimal design
- Responsive card and empty state styling

### JavaScript Functionality

#### Key Functions

1. `populateDateDropdown()`: 
   - Dynamically populates the date dropdown
   - Sets the initial selected date

2. `getCurrentStrategies()`: 
   - Retrieves strategies based on selected view and date
   - Filters data from the `strategyArray`

3. `getStrategyCount()`: 
   - Counts occurrences of each strategy
   - Prepares data for rendering strategy cards

4. `renderStrategies()`: 
   - Generates strategy cards or empty state
   - Handles dynamic rendering of strategies

#### Event Listeners

- View Toggle: Changes selected view and updates strategies
- Date Dropdown: Changes selected date and updates strategies

## Data Structure

### `dateArray`
```javascript
const dateArray = [
    '24-Apr-2024',
    '02-May-2024',
    '09-May-2024',
    '31-May-2024',
    '21-Jun-2024'
];
```

### `strategyArray`
A complex nested object containing strategies for each view and date:
```javascript
{
    'View': 'Bullish',
    'Value': {
        '24-Apr-2024': ['Bull Call Spread', 'Bull Put Spread', ...],
        '02-May-2024': ['Bull Call Spread', 'Long Call', ...]
    }
}
```

## How to Run

1. Download the `index.html` file
2. Open directly in a web browser
3. No additional setup or dependencies required

## Potential Improvements

- Add more robust error handling
- Implement local storage to remember user preferences
- Create a more advanced filtering mechanism
- Add tooltips or more detailed strategy information

## License

This project is open-source and free to use.

## Contact

For any questions or suggestions, please reach out to the project maintainer.
