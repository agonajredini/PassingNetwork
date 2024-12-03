# Football Passing Network Visualization

This repository contains a Python script that visualizes a football team's passing network based on match event data. The script processes pass data, analyzes player movements, and creates a passing network visualization on a soccer pitch. Player positions, passing connections, and the frequency of passes are displayed with varying line thickness, using libraries such as `mplsoccer`, `pandas`, and `matplotlib`.

## Features
- Processes pass events from football match data.
- Cleans and merges player data (including jersey numbers and names).
- Analyzes player participation and selects starting players.
- Visualizes player positions, passing connections, and pass frequency on a soccer pitch.
- Customizable visual appearance with pitch color, player names, and jersey numbers.

## Requirements
- `mplsoccer`: for soccer-specific plotting and data processing.
- `pandas`: for data manipulation and analysis.
- `numpy`: for numerical calculations.
- `matplotlib`: for creating visualizations.

You can install the necessary libraries using pip:

```bash
pip install mplsoccer pandas numpy matplotlib
```

## Code Overview
1. **Data Processing**: The script starts by filtering the pass events and merging them with player tactics data (including jersey numbers). It also handles player name replacements and selects only the starting 11 players based on their participation.
   
2. **Data Merging**: Player and pass data are merged to associate player names with the passes they made and received.

3. **Visualization**: The script creates a passing network visualization:
   - Player positions are displayed as scatter points on the pitch.
   - Pass connections between players are shown as lines with thickness based on the number of passes.
   - The pitch, player names, and jersey numbers are customized for clarity.

4. **Customizations**: The color scheme and layout are customizable, with options for pitch colors, line thickness, and annotations.

## Usage Notes
- The code, as written, is designed to work for **Manchester United** games, as the team name is hardcoded into the script.
- To use the script for other games, you need to modify the team selection part of the code. Specifically, you will need to adjust the team name filtering and selection based on the match data you wish to visualize.
- **What Needs to Be Changed**: The necessary modifications to make the code work for any team or match are clearly commented in the code itself. Look for comments that explain where to update team names, match IDs, and any relevant data processing steps.

## How to Use
1. Ensure you have the required libraries installed.
2. Modify the code to load your specific match data. The script currently uses the `Sbopen` parser to load event data for a specific match ID (e.g., 18236).
3. Customize the `name_replacements` dictionary for any additional player name adjustments.
4. Modify the `ateam` and `hteam` variables to reflect the teams in the match you want to analyze.
5. Run the script to generate a passing network visualization for your team.

## Example Output
The output will display a soccer pitch with:
- Players represented by scatter points.
- Pass connections represented by lines, with line thickness proportional to the number of passes between players.
- Player names and jersey numbers annotated next to their positions.

## License
This project is licensed under the MIT License.

## Acknowledgements
- `mplsoccer`: A library for soccer-specific data visualization.
- `matplotlib`: A popular plotting library used for creating visualizations.
- `pandas` and `numpy`: Libraries for data manipulation and analysis.
