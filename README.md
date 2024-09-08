### What does VSafeRoute do?

VSafeRoute is a multi-agent AI-based web application designed to improve road safety for cyclists by providing:

- **Safer route suggestions** and real-time hazard alerts.
- **Crash hotspot identification** and prediction of high-risk areas.
- **Real-time user feedback analysis** to dynamically update route safety and highlight hazards like potholes or poor lighting.
- **Data-driven policy recommendations** for city planners to improve cycling infrastructure.

This solution enhances safety, encourages cycling, and empowers both cyclists and policymakers with actionable insights.

### How is it a Multi-Agent AI-based Web Application?

#### **Feedback Processing Agent**

- **Function**: Processes user-reported feedback to dynamically update the system with new hazards or issues reported by cyclists.
- **Model**: Natural Language Processing (NLP) for feedback analysis.
  - Models like **BERT** or **TF-IDF** with a classifier can be used to analyze textual feedback.

##### **User Feedback Data Structure**:

```json
{
  "user_id": "user123",
  "location": { "latitude": -37.5625, "longitude": 143.8503 },
  "issue_type": "Ran off carriageway",
  "description": "The bike lane is too narrow at the intersection and the markings are faded.",
  "severity": 4,
  "time_of_occurrence": "2023-09-01T18:30:00",
  "phone_number": "+61",
  "suggestion": ""
}
```

### **Data Processing Flow**:

1. Tokenize, clean, and categorize free-text feedback using models like **TF-IDF** or **BERT**.
2. Label and categorize issues based on feedback.
3. Map recurring issues and severity levels onto the route map for future predictions and preventive measures.
4. Use categorized data to train models for hazard prediction and route safety scoring.

### **Crash Hotspot Identification Agent**

- **Function**: Uses historical crash data to identify high-risk areas (hotspots).
- **Model**: **DBSCAN** (Density-Based Spatial Clustering of Applications with Noise).
  - DBSCAN detects clusters of crashes without needing predefined regions, making it ideal for identifying arbitrary crash hotspots.

### Benefits of the Concept:

- **Data-Driven Decision Making**: Helps cyclists make safer route choices based on crash data, traffic patterns, and real-time feedback.
- **Crash Hotspot Identification**: AI highlights high-risk areas and suggests alternative routes, reducing accident risk.
- **Feedback Processing**: Collecting real-time hazard reports from cyclists improves route safety dynamically.
- **Evidence-Based Policy Recommendations**: Local governments can make informed infrastructure improvements based on data.
- **Increased User Participation**: Engaging cyclists in reporting issues creates a community-driven safety network.
- **Improved Health and Wellbeing**: Promoting cycling through safer routes enhances public health by encouraging active transportation.
