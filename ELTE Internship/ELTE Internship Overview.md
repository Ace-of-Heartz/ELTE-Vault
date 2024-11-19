# Requirements
- 1 page summary 
- 8 slide presentation
- 15 page detailed document

- weekly summary uploaded to Teams 
# Ongoing Projects 


## Description:
![[CAE_téma_ötletek.pdf]]
## Projects:
[[ELTE Internship/Sonar Simulation]] #BSc #Graphics 

## Calendar:

```dataviewjs // PS. remove backslash \ at the very beginning!

dv.span("**Daily Calendar**") /* optional ⏹️💤⚡⚠🧩↑↓⏳📔💾📁📝🔄📝🔀⌨️🕸️📅🔍✨ */
const dailyCalendar  = {
	colors: {    // (optional) defaults to green
		blue:        ["#8cb9ff", "#69a3ff", "#428bff", "#1872ff", "#0058e2"], // first entry is considered default if supplied
		green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
		red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
		orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
		pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
		orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"],
		aqua:        ["#00cccc", "#009999", "#006666", "#003333", "#00ffff"]
	},
	showCurrentDayBorder: true, // (optional) defaults to true
	defaultEntryIntensity: 4,   // (optional) defaults to 4
	intensityScaleStart: 0,    // (optional) defaults to lowest value passed to entries.intensity
	intensityScaleEnd: 12,     // (optional) defaults to highest value passed to entries.intensity
	entries: [],                // (required) populated in the DataviewJS loop below
}



//DataviewJS loop
for (let page of dv.pages("#DailySummary AND -#TEMPLATE")) {
	//dv.span("<br>" + page.file.name) // uncomment for troubleshooting
	dailyCalendar.entries.push({
		date: page.file.name,     // (required) Format YYYY-MM-DD
		intensity: page.overallTime, // (required) the data you want to track, will map color intensities automatically
		color: "aqua",          // (optional) Reference from *calendarData.colors*. If no color is supplied; colors[0] is used
		content: await dv.span(`[🔗](${page.file.name})`),
	})
}





renderHeatmapCalendar(this.container, dailyCalendar)
```
```dataviewjs // PS. remove backslash \ at the very beginning!

dv.span("**Meeting Calendar**") /* optional ⏹️💤⚡⚠🧩↑↓⏳📔💾📁📝🔄📝🔀⌨️🕸️📅🔍✨ */
const meetingCalendar ={
	colors: {    // (optional) defaults to green
		blue:        ["#8cb9ff", "#69a3ff", "#428bff", "#1872ff", "#0058e2"], // first entry is considered default if supplied
		green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
		red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
		orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
		pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
		orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"],
		aqua:        ["#00cccc", "#009999", "#006666", "#003333", "#00ffff"]
	},
	showCurrentDayBorder: true, // (optional) defaults to true
	defaultEntryIntensity: 4,   // (optional) defaults to 4
	intensityScaleStart: 0,    // (optional) defaults to lowest value passed to entries.intensity
	intensityScaleEnd: 12,     // (optional) defaults to highest value passed to entries.intensity
	entries: [],                // (required) populated in the DataviewJS loop below
}

for (let page of dv.pages("#Meeting AND -#TEMPLATE")) {
	//dv.span("<br>" + page.file.name)
	meetingCalendar.entries.push({
		date: page.file.name,
		intensity: 12,
		color: "red",
		content: await dv.span(`[🔗](${page.file.name})`),
	})
}


renderHeatmapCalendar(this.container, meetingCalendar)
```

## Daily Summaries:
```dataview
LIST 
FROM #DailySummary AND #ELTE AND #Internship AND -#TEMPLATE
```
## Meeting Summaries:
```dataview
LIST 
FROM #Meeting AND #ELTE AND #Internship AND -#TEMPLATE
```
## Links
### Daily Summaries:
- [[ELTE/ELTE Internship/Daily Summaries/2024-07-09|2024-07-09]]
- [[2024-07-10]]
- [[2024-07-12]]
- [[ELTE/ELTE Internship/Daily Summaries/2024-07-14|2024-07-14]]
### Meeting Summaries:
- [[2024-07-04]]
- [[ELTE/ELTE Internship/Meeting Summaries/2024-07-09|2024-07-09]]
- [[2024-07-11]]
- [[2024-07-17]]
- [[2024-07-22]]