Voice Perception Study, Pilot

Online listening task for a speech and voice perception research project. Participants listen to short audio clips and rate the speaker on a set of trait scales.

What's in this repo

index.html is the task itself, a single page, no build step needed. audio/ holds the 9 audio clips used in the pilot, the 8 real trials plus 1 practice clip.

How the site works

The task moves through a series of screens, in this order.

Consent. A brief description, a checkbox to agree, then a Continue button that stays disabled until the box is checked.

Demographics. Age, native language, hearing, headphones, and gender. Continue enables once every field is filled. A Back button here returns to Consent.

Instructions. Explains the rating scales, 1 to 7, from "Not at all" to "Extremely", and lets the participant know a practice clip comes first. A Back button here returns to Demographics.

Practice trial. One clip that isn't scored, marked with an orange banner saying so, so people can see how a trial works before the real ones start.

Transition screen. Shows once, right after the practice trial and before the real trials begin, with a Begin button.

9 real trials. 8 scored clips plus 1 attention check trial, inserted at a random spot (never first or last). There's no Back button once trials start, and that's deliberate: we want each rating to reflect a fresh first impression, not something revised after comparing it to an earlier clip.

Thank you screen. Responses get sent automatically before this screen confirms anything. A Close window button shows up once saving succeeds. If the browser won't let a script close the tab (fairly normal for tabs that weren't opened by a script in the first place), it just asks the person to close it manually instead.

How one trial actually behaves

Only the audio player shows up at first, just a big play button. Once the clip finishes, the six rating scales fade into view, they're hidden until then, so nobody can rate before listening. Next stays disabled until all six scales have an answer. Progress is shown as a small row of dots up top, not a number or percentage, kept simple on purpose.

What data gets collected

For each participant: their demographic answers, plus per trial data, which clip they heard and their six ratings on it. No names, emails, or anything identifying gets collected. A random ID gets generated in the browser each session, just so one person's rows can be grouped together later.

Where the responses go

Responses get sent automatically to a private Google Sheet, through a Google Apps Script Web App. Nobody has to download or manually submit anything.

Hosting

This runs as a static site through GitHub Pages, straight from this repo's root.

Status

This is a pilot version, meant to check the task mechanics and stimulus set before scaling up to the full study.
