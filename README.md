# Experiment 1: EDA in IPL Dataset
### Name : Rithik Ram S
### Reg No : 212224230229
## Aim:
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

## Algorithm / Procedure:


### Step 1.Import Libraries
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
### Step 2.Load Dataset
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
### Step 3.Matches per Season (Univariate Analysis)
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
### Step 4.Top Winning Teams (Univariate Analysis)
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
### Step 5.Toss Decisions (Univariate Analysis)
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
### Step 6.Top Venues (Univariate Analysis)
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
### Step 7.Draw Insights
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.
  
  ## Program
  
### Basic info about dataset:
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
matches = pd.read_csv("matches.csv")
print("Dataset Shape:", matches.shape)  
print(matches.head())

```
### Matches per season:
```python
 season_counts = matches['season'].value_counts().sort_index()
 print("\nMatches per season:\n", season_counts)
```
### Matches per season plotted:
```python
plt.figure(figsize=(8,4))
sns.barplot(x=season_counts.index, y=season_counts.values, palette="viridis")
plt.title("Number of Matches per Season")
plt.xlabel("Season")
plt.ylabel("Matches")
plt.show()
```

###  Most successful teams:
```python
team_wins = matches['winner'].value_counts()
print("\nTop Winning Teams:\n", team_wins.head(5))

 plt.figure(figsize=(8,4))
 sns.barplot(x=team_wins.head(5).index, y=team_wins.head(5).values, palette="magma")
 plt.title("Top 5 Winning Teams")
 plt.xlabel("Team")
 plt.ylabel("Wins")
 plt.show()
```

###  Toss decisions (bat vs field)
```python
 toss_decision = matches['toss_decision'].value_counts()
 print("\nToss Decisions:\n", toss_decision)

 plt.figure(figsize=(6,4))
 sns.barplot(x=toss_decision.index, y=toss_decision.values, palette="Set2")
 plt.title("Toss Decisions (Bat or Field)")
 plt.show()
```

### Venues hosting most matches:
```python
 venue_counts = matches['venue'].value_counts().head(5)
 print("\nTop Venues:\n", venue_counts)

 plt.figure(figsize=(8,4))
 sns.barplot(y=venue_counts.index, x=venue_counts.values, palette="coolwarm")
 plt.title("Top 5 Venues by Matches Hosted")
 plt.xlabel("Matches Hosted")
 plt.ylabel("Venue")
 plt.show()
```

## Output


### Basic info about dataset:
 <img width="1067" height="860" alt="image" src="https://github.com/user-attachments/assets/a34aa70c-ff3d-48dd-b4d6-0bb4aafe7002" />

### Matches per season:
<img width="1199" height="544" alt="image" src="https://github.com/user-attachments/assets/5414a96d-9a17-4e57-871e-64fa7fb351ee" />

### Matches per season plotted:

<img width="960" height="589" alt="image" src="https://github.com/user-attachments/assets/57e7e11b-7e2d-436b-b5c8-e5ceca8375b9" />

###  Most successful teams:

<img width="610" height="248" alt="image" src="https://github.com/user-attachments/assets/bc657cd9-9278-43df-aa24-ecaa5ba8bcbd" />

<img width="1093" height="789" alt="image" src="https://github.com/user-attachments/assets/bc3e3c10-a648-45fa-a5a4-4fa9454ca097" />



###  Toss decisions (bat vs field)

<img width="610" height="187" alt="image" src="https://github.com/user-attachments/assets/31b1fa02-18ea-4d93-ab13-4cd5244aed99" />

<img width="841" height="602" alt="image" src="https://github.com/user-attachments/assets/6cba4af6-15bc-4cb0-a200-08162f986ff1" />


### Venues hosting most matches:

<img width="663" height="257" alt="image" src="https://github.com/user-attachments/assets/2b210523-a695-45e2-8f5a-1259e043284c" />

<img width="1324" height="567" alt="image" src="https://github.com/user-attachments/assets/e1a016f8-ceb4-49a1-9e32-3d64a1a44d51" />




 ## Result:
  Thus experiment is executed successfully




