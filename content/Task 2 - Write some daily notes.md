
1. Create a **Daily** folder
2. Create a [[DayTemplate]] note
3. Type `Cmd + ,` to go to Settings (or use the UI) - set "New file location" and "Template file location" as follow ![[configure-daily-notes-core-plugin.png]]
4. Create a new day with `Cmd + P` then type "today" again to open Today's note
5. You should see a cooler template than an empty file. Copy the following content to be the same as [[2024-07-23]] 
6. Pretend we have created daily notes for many days, by adding more files in the same Daily folder [[2024-07-24]] and [[2024-07-25]]. You should have files that look like this: ![[daily-notes-folder.png]]
7. Go to [[2024-07-23]] and type `Cmd + P`  and type "daily" and navigate "next day" and "previous day" to get the hang of the Daily Notes core plugin.![[daily-shortcuts.png]]
8. Voila! See Bonus section below for how we can make sense of habit tracking data thanks to the metadata `key:: value` format.


> [!tldr] I used an AI plugin to generate the above template using OpenAI gpt-4o-mini
> You can check out that chat in [[generate daily notes]]

### Bonus

1. Install Dataview plugin by going to **Settings** --> **Community Plugins** --> **Browse** -> search "Dataview" --> **Install** -> **Enable** ![[install-dataview.png]]
2. Create a new "Habit Tracking Dashboard" note and paste the following script in it. See it in action at [[Habit Tracking Dashboard]]

```
```dataview
table 
    Wakeup as "Wakeup Time", 
    Exercise as "Exercise", 
    WordCount as "Word Count", 
    HoursOfSleep as "Hours of Sleep", 
    Reading as "Reading Time", 
    Meditation as "Meditation Time", 
    WaterIntake as "Water Intake"
from "Daily"
sort date desc
```





> [!tldr] I also used AI to  generate the above dataview query
> See chat in [[generate habit tracker]]
