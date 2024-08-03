# Task Recommendation System

## Overview

The Task Recommendation System uses a Nearest Neighbors algorithm to recommend tasks based on a given time input. By analyzing task durations and completion statuses, it identifies tasks that are similar to the specified time.

## Installation

To run the Task Recommendation System, you need Python and the following dependencies:

- `pandas`
- `numpy`
- `scikit-learn`

You can install the necessary dependencies using `pip`:

```bash
pip install pandas numpy scikit-learn
```

## Running the Script

1. **Clone or download the repository**: Ensure you have the script file, e.g., `task_recommendation.py`.

2. **Run the script**: Execute the script with Python. You can provide an example time to get task recommendations:

   ```bash
   python task_recommendation.py
   ```

   Alternatively, modify the `task_recommendation_system` function call in the script to test different times:

   ```python
   print(task_recommendation_system('05:00 PM'))
   ```

## Assumptions

- The task times are assumed to be within the same day. The script does not handle tasks spanning multiple days.
- Task durations are calculated using the difference between start and end times without considering breaks or overlapping tasks.
- The time format provided in the input should be in `'%I:%M %p'` format (e.g., `'05:00 PM'`).
- The system assumes that all tasks in the sample dataset are relevant and that the dataset is representative of typical task timings.

## Recommendation Algorithm

The Task Recommendation System uses the Nearest Neighbors algorithm from the `scikit-learn` library.

**How It Works:**
1. **Feature Extraction**: Converts start times to minutes and encodes the completion status as binary (1 for completed, 0 for not completed). Calculates task duration in minutes.
2. **Model Training**: Uses the Nearest Neighbors algorithm to fit a model on the features.
3. **Task Recommendation**: Given a time, converts it to minutes and finds the nearest neighbors based on the features. Recommends tasks similar to the given time.

## Testing and Validation

### Sample Dataset

The script includes a sample dataset with tasks and their attributes for demonstration purposes.

### Validation Metrics

- **Precision**: The fraction of relevant tasks among the recommended tasks.
- **Recall**: The fraction of relevant tasks that were recommended out of all relevant tasks.

The precision and recall metrics help evaluate the accuracy of the task recommendations.

## Areas for Potential Improvement

1. **Time Overlaps**: Handle tasks that span multiple days or overlapping tasks.
2. **Contextual Relevance**: Incorporate additional features such as task priority or type for more nuanced recommendations.
3. **Dynamic Data**: Integrate with a real-time task database to handle dynamically changing task data.
4. **User Feedback**: Implement a feedback mechanism to refine recommendations based on user preferences or historical task completion data.
5. **Scalability**: Optimize the recommendation system to handle larger datasets efficiently.

