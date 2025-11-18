> Change Log (2025-11-17): 
   > – Refined Module 02 based on AI critique: added Inputs section and defined Day Block Schema

### **Module 2 — Plan Builder (Options → Days)**
Inputs:
Required: destination, trip dates, party size, budget type/value, daily time window, must‑do activities
Optional (defaults applied if missing): pace (default: medium), mobility constraints, dietary preferences, transport preferences, indoor/outdoor preference, weather notes

Day Block Schema: Each day is divided into canonical slots. A block contains:
  day index
  slot label (morning / midday / afternoon / evening)
  activity title + short description
  estimated duration
  cost band (free / low / moderate / high)
  neighborhood/location
  transport mode hint
  flexibility (fixed / optional)
  tags (e.g., weather‑sensitive, hours‑to‑validate, mobility‑friendly)
  assumptions (e.g., transit time, budget allocation)
  
Workflow: Create a short list of candidate activities (e.g., attractions, restaurants, parks). Each activity includes type, estimated duration, cost range, and distance.

Use a simple loop to build days:
for each day:  
  pick Morning activity (near lodging)   
  pick Midday activity (close by)
  pick Afternoon activity (different theme) 
  pick Evening restaurant or optional event
