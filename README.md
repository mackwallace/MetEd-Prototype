# MetEd My Syllabus — Prototype

Prototype for the "My Syllabus" personalized learning plan feature on the MetEd platform.

## Files

| File | Description |
|------|-------------|
| `index.html` | Dashboard with "Get My Learning Plan" CTA and intake modal |
| `learning-plan-results-v1.5.html` | Personalized results page |

## Prototype Flow

1. Dashboard loads at the root URL
2. User clicks "Get My Learning Plan"
3. Full-screen modal with 13-field intake form
4. Loading state (~60 seconds) with progress bar and fun facts
5. Results page with 5 personalized courses (or 1 curriculum)

## Wiring the Cassidy Webhook

Open `index.html` and find the credentials section near the bottom `<script>`:

```javascript
var CASSIDY_WEBHOOK_URL = '';  // paste your Cassidy webhook URL here
var CASSIDY_API_KEY     = '';  // paste your API key here (e.g. 'Bearer sk-cass-...')
```

Leave both empty to run in **simulation mode** (Mike Henry demo data).
Set both to go **live** with real Cassidy responses.

**CORS:** Cassidy must allow requests from this site's domain. Configure the allowed origins in your Cassidy workflow settings.

## Deploying Updates

Push changes to the `main` branch — GitHub Pages rebuilds automatically.
