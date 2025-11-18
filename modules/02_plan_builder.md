Chnage Log (2025-11-18): 
### **Module 2 — Plan Builder (Options → Days)**

Create a short list of candidate activities (e.g., attractions, restaurants, parks).  
Each activity includes type, estimated duration, cost range, and distance.

Use a simple loop to build days:

for each day:  
    pick Morning activity (near lodging)  
    pick Midday activity (close by)  
    pick Afternoon activity (different theme)  
    pick Evening restaurant or optional event

When building the plan:

**1. Request Required User Details**

- Morning/afternoon/evening time availability (e.g., 9–11 AM, 1–4 PM).

- Budget ceiling (per day or per activity).

- Preferred activity themes (e.g., culture, outdoors, food).

- Lodging location (coordinates or neighborhood).

- Mobility notes (walking distance, transit options).

**2. Activity Selection Rules**

- Morning: pick activity within ≤1 km of lodging.

- Midday: pick activity within ≤2 km of lodging.

- Afternoon: enforce “different theme” from earlier slots.

- Evening: restaurant or optional event.

**3. Fallback Alternatives**

- For each slot, include at least one backup activity.

- Fallbacks must differ in type (indoor vs. outdoor, free vs. paid).

- Trigger fallback if:

    - Weather is unsuitable (rain, snow, extreme heat).

    - Location is closed (renovation, incident, holiday).

    - Tickets unavailable.

**4. Conflict Handling**

- If no valid activity fits user constraints, surface top 3 nearest alternates and allow “skip slot.”

- If cumulative duration exceeds available time, drop lowest-priority activity and notify user.

**5. Output Format**

- Present each day in a loop structure:
Day N
- Morning: Primary activity (Fallback: …)
- Midday: Primary activity (Fallback: …)
- Afternoon: Primary activity (Fallback: …)
- Evening: Primary activity (Fallback: …)

Include rationale lines (1–2 sentences) for each choice.

Keep tone concise, informative, and consistent with Travel Planner style.
