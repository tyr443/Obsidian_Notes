# 📊 Python Learning Progress Tracker



---

## ✅ Completed Topics

```dataview
table topic, category, date_learned
from "Python-Learning"
where status = "completed"
sort date_learned asc
```

## 🎯 Learning

```dataview
TABLE topic
FROM "Python-Learning"
WHERE status = "in-progress"
```

## ⏳ Progress

```dataviewjs
// Get all pages in the "Python-Learning" folder
const pages = dv.pages('"Python-Learning"');

// Total number of pages
const total = pages.length;

// Count pages where status is "completed"
const completed = pages.where(p => p.status === "completed").length;

// Calculate progress percentage
const progress = total > 0 ? (completed * 100.0 / total) : 0;

// Display the result rounded to two decimal places
dv.paragraph(`Progress (%): ${progress.toFixed(2)}%`);

```

