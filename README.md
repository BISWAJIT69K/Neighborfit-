# 🇮🇳 NeighborFit – Indian Neighborhood Recommendation System

**NeighborFit** is a full-stack web application built to help Indian users discover the most suitable neighborhoods to live in — based on their **budget**, **area type**, **state**, **lifestyle**, and access to nearby **facilities** like gyms, metros, and hospitals.  
It focuses on **neighborhoods**, not properties — helping users make better decisions on *where* to live, especially in unfamiliar cities.

---

## 🎯 Objective

This project addresses a real Indian problem:
> _"Where should I live that fits my budget, lifestyle, and needs — without browsing thousands of listings?"_

Ideal for:
- 🧑‍🎓 Students
- 👨‍💼 Job seekers
- 👨‍👩‍👧‍👦 Families relocating to cities

---

## 🛠 Tech Stack

| Layer       | Tech Used                  |
|-------------|----------------------------|
| Frontend    | HTML, CSS, JavaScript (Vanilla) |
| Backend     | Node.js, Express.js        |
| Data Format | Local JSON Dataset (Indian neighborhoods) |
| Platform    | Replit (Free plan used)    |

---

## 🔧 Features

✅ Select **State**, **Area Type** (Urban/Suburban/Rural)  
✅ Choose **budget range** (e.g. ₹8,000–₹25,000)  
✅ Choose **user type** (Student, Family, Working Professional)  
✅ Optional filters: **Gym**, **Metro**, **Colleges**, **Hospitals**, **Cafes**  
✅ Backend filters matching neighborhoods  
✅ Each suggestion includes a **custom explanation** (reason for match)  
✅ Handles **no match** cases with friendly tips

---

## 🧠 Sample Input (POST to `/api/match`)

```json
{
  "minBudget": 12000,
  "maxBudget": 20000,
  "type": "urban",
  "state": "Karnataka",
  "userType": "working professionals",
  "facilities": ["gym", "metro"]
}
