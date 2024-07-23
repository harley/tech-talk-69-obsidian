##### user
based on the following habit data tracked in each daily notes in Daily folder, help me use dataview to generate a table displaying data
- Wakeup:: 6:30 AM
- Exercise:: 30 minutes of stretching.
- WordCount:: 800 words (including presentation notes).
- HoursOfSleep:: 6 hours.
- Reading:: 30 minutes of "On Writing".
- Meditation:: 20 minutes to center myself before the talk.
- WaterIntake:: 2 liters.

##### assistant
```lookup
{"hypothetical_1":"Daily Folder > Daily Notes > Habit Tracking > Daily Habit Data: | Date       | Wakeup     | Exercise                     | WordCount | HoursOfSleep | Reading                | Meditation              | WaterIntake | |------------|------------|------------------------------|-----------|--------------|------------------------|-------------------------|-------------| | 2023-10-01 | 6:30 AM    | 30 minutes of stretching     | 800       | 6 hours      | 30 minutes of 'On Writing' | 20 minutes to center myself | 2 liters    | | 2023-10-02 | 6:30 AM    | 30 minutes of stretching     | 800       | 6 hours      | 30 minutes of 'On Writing' | 20 minutes to center myself | 2 liters    | | 2023-10-03 | 6:30 AM    | 30 minutes of stretching     | 800       | 6 hours      | 30 minutes of 'On Writing' | 20 minutes to center myself | 2 liters    |","hypothetical_2":"Daily Folder > Daily Notes > Habit Tracking > Weekly Summary: | Week       | Average Wakeup | Average Exercise | Average WordCount | Average HoursOfSleep | Average Reading | Average Meditation | Average WaterIntake | |------------|----------------|------------------|-------------------|---------------------|----------------|-------------------|---------------------| | Week 1    | 6:30 AM       | 30 minutes       | 800               | 6 hours             | 30 minutes      | 20 minutes        | 2 liters            | | Week 2    | 6:30 AM       | 30 minutes       | 800               | 6 hours             | 30 minutes      | 20 minutes        | 2 liters            |","hypothetical_3":"Daily Folder > Daily Notes > Habit Tracking > Monthly Overview: | Month      | Total Wakeup | Total Exercise | Total WordCount | Total HoursOfSleep | Total Reading | Total Meditation | Total WaterIntake | |------------|--------------|----------------|------------------|---------------------|---------------|------------------|--------------------| | October    | 6:30 AM     | 30 minutes      | 8000            | 180 hours           | 600 minutes    | 600 minutes       | 60 liters          |"}
```

##### system
```sc-context
Daily/2024-07-24.md
Daily/2024-07-23.md
Daily/2024-07-25.md
Task 1 - Set up Obsidian.md
```

##### assistant
Based on your notes, you can use the following Dataview query to generate a table displaying the habit data tracked in your daily notes:

```markdown
```dataview
table 
    date as "Date", 
    Wakeup as "Wakeup Time", 
    Exercise as "Exercise", 
    WordCount as "Word Count", 
    HoursOfSleep as "Hours of Sleep", 
    Reading as "Reading Time", 
    Meditation as "Meditation Time", 
    WaterIntake as "Water Intake"
from "Daily"
sort date asc
```
```

This query will create a table with the specified columns, displaying the data from your daily notes in chronological order. Each row will represent a different day's habits, allowing you to easily review your tracked activities.