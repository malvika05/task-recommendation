# Task Recommendation System

## Overview

The Task Recommendation System uses a Nearest Neighbors algorithm to recommend tasks based on a given time input. The system analyzes task durations and completion statuses to find similar tasks that might be relevant at the specified time.

## Features

- **Time Conversion**: Converts task start and end times to minutes for easier manipulation.
- **Duration Calculation**: Calculates the duration of each task in minutes.
- **Feature Encoding**: Encodes completion status as a binary feature (1 for completed, 0 for not completed).
- **Nearest Neighbors Model**: Recommends tasks similar to a given time based on start time, duration, and completion status.

## Setup

### Prerequisites

Ensure you have Python installed along with the following libraries:
- `pandas`
- `numpy`
- `scikit-learn`

You can install the required libraries using pip:

```bash
pip install pandas numpy scikit-learn
```



## Usage

1. **Run the script**: Execute the Python file to test the task recommendation system.
   
   ```bash
   python task_recommendation.py
   ```

2. **Provide Input Time**: Modify the `task_recommendation_system` function call with your desired time in the format `'%I:%M %p'` (e.g., `'05:00 PM'`).

3. **View Recommendations**: The system will print a list of recommended tasks based on the provided time.

## Example

To get recommendations for tasks around `'05:00 PM'`, the script will output tasks that are similar to this time based on the nearest neighbors algorithm.

```python
print(task_recommendation_system('05:00 PM'))
```

Output example:

```
['Client call', 'Documentation update', 'Performance analysis']
```

